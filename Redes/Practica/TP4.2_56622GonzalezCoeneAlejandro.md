![[Pasted image 20240922210958.png]]<br><br><br><br>

<center>
Carrera:
</center>
<center>
<span style="font-size: 30px;">Licenciatura en Sistemas de Información</span>
</center>

<br><br><br><br><br><br>

<center><span style="font-size: 30px;">Trabajo Práctico</span></center>
<center><span style="font-size: 30px;">TP 4.2  - Sockets</span></center>


<br><br><br><br>
<center><span style="font-size: 20px;">Asignatura:</span></center>
<center>Redes de Datos</center>

<br><br>

<center>Equipo Docente</center>
<center>Mgter Leopoldo José Ríos</center>

<br><center><span style="font-size: 20px;">Alumno:</span></center>
<center><span style="font-size: 20px;">Alejandro Rafael, Gonzalez Coene
</span></center><br><br><br><br><br><br>
<center>2024</center>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

repositorio: https://github.com/alejandro7177/socket_chat

# server.py
Script encargado del socket para el servidor anfitrión que estará escuchado todas las peticiones

```python
server = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
server.bind((HOST, PORT))
print("Iniciando el servidor...")
receive_connections()
```

al ejecutar el script se inicializa el server creando un socket para el server y asignando le host y el puerto en este caso es localhost:12345 y ejecuta receive_connection

```python
def receive_connections():
	global user_id_counter
	server.listen()
	print(f"Servidor escuchando en {HOST}:{PORT}")
	while True:
		client, address = server.accept()
		print(f"Conectado con {address}")#informa por consola los nuevo clientes
		client_id = user_id_counter
		user_id_counter += 1
		client_info[client] = (client_id, "") # El nombre se establecerá después
		client.sendall(f"ID:{client_id}".encode('utf-8'))
		clients.append(client)

		#crea un hilo para el nuevo usuario
		thread = threading.Thread(target=handle_client, args=(client,))
		thread.start()
```

- El servidor escucha conexiones entrantes en un puerto específico.
- Cuando un cliente se conecta, el servidor lo acepta y le asigna un ID único.
- La información del cliente (ID, nombre vacío) se almacena.
- El servidor envía al cliente su ID para que el cliente pueda identificarlo.
- El cliente se añade a la lista de clientes conectados.
- Se crea un nuevo hilo para manejar la interacción con el cliente. El hilo ejecuta una función que se encargará de recibir mensajes y responder al cliente sin bloquear el servidor para manejar nuevas conexiones.

```python
def handle_client(client):
	while True:
		try:
			message = client.recv(1024).decode('utf-8')
			if message:
				if message.startswith("NAME:"):
					# Recibir el nombre del cliente
					client_name = message[5:]
					client_id = client_info[client][0]
					client_info[client] = (client_id, client_name)
				
					print(f"Cliente {client_id} estableció su nombre a {client_name}")
					send_user_list()
				else:
					broadcast(message, client)
			
			else:
				client.close()
				clients.remove(client)
				client_info.pop(client, None)
				send_user_list()
				breaK
		except:
			client.close()
			clients.remove(client)
			client_info.pop(client, None)
			send_user_list()
			break
```
- La función escucha continuamente los mensajes de un cliente.
- Si el mensaje contiene `"NAME:"`, el servidor actualiza el nombre del cliente y notifica a los demás.
- Si el mensaje es normal, se reenvía a los otros clientes.
- Si el mensaje está vacío o se produce un error, el cliente se desconecta, y el servidor actualiza la lista de usuarios conectados.
- Utiliza un enfoque robusto que maneja desconexiones o errores de red sin bloquear el resto del sistema.
```python
def broadcast(message, source_client=None):
	"""Función para enviar mensajes a todos los clientes excepto al remitente."""
	for client in clients:
		if client != source_client:
			try:
				client.sendall(message.encode('utf-8'))
			except:
				client.close()
				clients.remove(client)
				client_info.pop(client, None)
				send_user_list()
```
- **Difusión del mensaje**: La función toma un mensaje y lo envía a todos los clientes, excepto al cliente que lo envió.
- **Gestión de errores**: Si hay un problema al enviar el mensaje a algún cliente, la conexión con ese cliente se cierra, el cliente se elimina de la lista de clientes conectados, y se actualiza la información global de usuarios.
- **Manejo eficiente**: El servidor maneja automáticamente las desconexiones y garantiza que los clientes restantes siempre tengan la información actualizada sobre quién sigue conectado.

# chat_client.py
Script para el conectarse al server como cliente y comunicarse con el resto de clientes

Variables y libreria
```python
import socket
import threading
HOST = 'localhost'
PORT = 12345
client_socket = None
messages = []
client_id = None
client_name = None # Nombre de usuario
connected_users = [] # Lista de usuarios conectados
```


```python
def connect_to_server():
"""Conecta al cliente con el servidor y comienza el hilo de recepción."""
	global client_socket
	try:
		client_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
		client_socket.connect((HOST, PORT))
		threading.Thread(target=receive_messages, daemon=True).start()
	except Exception as e:
		print(f"Error al conectar al servidor: {e}")
```

- La función intenta establecer una conexión entre el cliente y el servidor utilizando un socket.
- Si la conexión se establece correctamente, se inicia un nuevo hilo que ejecuta la función `receive_messages`, permitiendo que el cliente escuche mensajes del servidor en segundo plano.
- Si algo falla durante el proceso de conexión, se captura la excepción y se informa del error al usuario.
```python
def receive_messages():
	"""Hilo para recibir mensajes del servidor."""
	global client_socket
	global client_id
	global connected_users
	while True:
		try:
			message = client_socket.recv(1024).decode('utf-8')	
			if message:	
				if message.startswith("ID:"):
					# Recibir el ID asignado por el servidor
					client_id = message[3:]
					print(f"Tu ID es: {client_id}")
					# Enviar el nombre de usuario al servidor
					client_socket.sendall(f"NAME:{client_name}".encode('utf-8')		
				elif message.startswith("USERS:"):
					# Recibir la lista de usuarios conectados
					users_data = message[6:].split("&&")
					connected_users.clear()
					for user_data in users_data:
						if user_data:
							uid, uname = user_data.split("||")
							connected_users.append((uid, uname))	
				else:	
				messages.append(message)
			else:
				break
		except Exception as e:
			print(f"Error al recibir mensajes: {e}")
			break
```

- **Recepción de mensajes**: La función escucha continuamente los mensajes que llegan del servidor.
- **Asignación de ID**: Si el servidor envía un mensaje con el ID del cliente, este se guarda en la variable `client_id` y el cliente responde enviando su nombre de usuario.
- **Gestión de usuarios conectados**: Si el servidor envía una lista de usuarios conectados, se actualiza la lista `connected_users` en el cliente.
- **Manejo de mensajes**: Si el mensaje recibido es un mensaje de chat normal, se añade a la lista de mensajes para que otros hilos o funciones del cliente puedan procesarlos.
- **Manejo de desconexiones**: Si el servidor envía un mensaje vacío o se produce un error, la conexión se cierra y el hilo termina.
```python
def send_message(message):
    """Envía un mensaje al servidor."""
    # Usamos la variable global 'client_socket' para acceder al socket del cliente
    global client_socket
    # Verificamos si el socket está establecido (no es None o desconectado)
    if client_socket:
        try:
            # Intentamos enviar el mensaje al servidor codificado en UTF-8
            client_socket.sendall(message.encode('utf-8'))
        except Exception as e:
            # Si ocurre un error durante el envío, lo capturamos e imprimimos el mensaje de error
            print(f"Error al enviar mensaje: {e}")

```
- **Función clave**: Envía un mensaje al servidor si la conexión está activa.
- **Gestión de errores**: Si ocurre un problema al enviar el mensaje (como la desconexión del servidor), el error se captura y se notifica en la consola.
- **Codificación de mensajes**: Los mensajes se codifican en UTF-8 antes de ser enviados, lo que es un estándar en las comunicaciones de red para asegurar la correcta transmisión de caracteres.

# Interfaz
# app.py

Este código es una aplicación de chat en tiempo real implementada en **Streamlit**, que permite a los usuarios conectarse a un servidor de chat, ver otros usuarios conectados y enviar mensajes. El código utiliza varios módulos, incluido `chat_client`, que maneja la conexión y comunicación con el servidor
### Librerias
```python
import random
import streamlit as st
from streamlit_chat import message as mensaje
import chat_client
from streamlit_autorefresh import st_autorefresh
```

- **Ingreso de usuario**: El usuario ingresa su nombre, que luego se utiliza para conectarse al servidor mediante el módulo `chat_client`.
- **Visualización de información**: Una vez conectado, se muestra el ID del cliente y los usuarios conectados.
- **Recepción de mensajes**: Los mensajes recibidos se muestran en la interfaz y se actualizan automáticamente cada 2 segundos gracias a la función `st_autorefresh`.
- **Envío de mensajes**: El usuario puede escribir mensajes en el formulario de texto, que luego son enviados al servidor y añadidos a la interfaz de chat.
### Codigo fuente
```python
st.title("Aplicación de Chat en Tiempo Real")
    
    Establece el título de la aplicación en la interfaz de Streamlit.
```
2. **Inicialización del nombre de usuario**:
```python
if 'username' not in st.session_state:     st.session_state.username = ''
```
3. **Función principal `main()`**: Aquí ocurre toda la lógica de la interfaz del chat.
    - **Auto-refresh**:
        
```python     
st_autorefresh(interval=2000, key="chat_refresh")
```
Refresca la página automáticamente cada 2 segundos para obtener actualizaciones en tiempo real, como nuevos mensajes o usuarios conectados.
    - **Ingreso del nombre de usuario**: Si el nombre de usuario no ha sido ingresado, se muestra un campo de texto para ingresar el nombre y, cuando se proporciona, se llama a `chat_client.connect_to_server()` para conectar al servidor.
```python
if not st.session_state.username:     
	st.session_state.username = st.text_input("Ingresa tu nombre de usuario")     
if st.session_state.username:         
	chat_client.client_name = st.session_state.username            chat_client.connect_to_server() 
	```       
- **Mostrar ID y nombre de usuario**: Si el cliente ya está conectado al servidor, se muestra el ID del usuario y el nombre.
```python  
if chat_client.client_id is not None:
	st.write(f"Tu ID de usuario es: {chat_client.client_id}")                        st.write(f"Tu nombre de usuario es: {chat_client.client_name}")
```    
- **Mostrar lista de usuarios conectados**: Utiliza `chat_client.connected_users`, que es una lista de tuplas `(ID, nombre)` que representan a los usuarios conectados.
```python
st.subheader("Usuarios Conectados:") 
for uid, uname in chat_client.connected_users:     
	st.write(f"ID: {uid}, Nombre: {uname}")
```
- **Mostrar mensajes recibidos**: Muestra todos los mensajes recibidos en el chat en tiempo real. Se utilizan diferentes estilos de "avatar" según si el mensaje es del propio usuario o de otros.
```python
for msg in chat_client.messages:
    parts = msg.split("||")
    if len(parts) == 3:
        sender_id, sender_name, content = parts
    elif len(parts) == 2:
        sender_id, content = parts
        sender_name = "Desconocido"
    else:
        sender_id = "Desconocido"
        sender_name = "Desconocido"
        content = msg

    if sender_id == chat_client.client_id:
        mensaje(
            message=f"{sender_name}: {content}",
            is_user=True,
            avatar_style="lorelei"
        )
    else:
        mensaje(
            message=f"{sender_name}: {content}",
            is_user=False,
            avatar_style="bottts"
        )

```
 Si el mensaje está en el formato `"ID||Nombre||Mensaje"`, se extraen estos tres componentes. Si solo tiene `"ID||Mensaje"`, se asigna "Desconocido" como nombre del remitente.
    - `is_user=True`: Aplica un estilo de mensaje distinto para los mensajes del propio usuario.
    - **Formulario para enviar mensajes**: Utiliza un formulario para enviar mensajes. Cuando se presiona el botón "Enviar", el mensaje se envía al servidor usando `chat_client.send_message()` y también se añade a la lista de mensajes local para actualizar la interfaz inmediatamente.
```python
with st.form(key='message_form', clear_on_submit=True):
    message = st.text_input("Escribe tu mensaje", key="message_input")
    submit_button = st.form_submit_button(label='Enviar')

    if submit_button and message:
        full_message = f"{chat_client.client_id}||{chat_client.client_name}||{message}"
        chat_client.send_message(full_message)
        chat_client.messages.append(full_message)

```

### Ejemplos del chat
#### Nombre de usuario
![[Pasted image 20240922202122.png]]

#### Mostrar usuarios conectados con su id
![[Pasted image 20240922202213.png]]
### Server logs
![[Pasted image 20240922202327.png]]

#### Envio de mensaje

![[Pasted image 20240922202445.png]]
Segundo usuario de la misma interfaz generado con client
![[Pasted image 20240922202942.png]]
![[Pasted image 20240922203017.png]]
# 2. coneccion con otro usuario con c\#
## Codigo fuente de inplementeción en c\#
```c#
using System;
using System.Net.Sockets;
using System.Text;
using System.Threading;

namespace ChatClient
{
    class Client
    {
        static TcpClient clientSocket = new TcpClient();
        static NetworkStream stream = default(NetworkStream);
        static string clientId = "";
        static string clientName = "";
        static bool isConnected = false;

        static void Main(string[] args)
        {
            Console.Write("Ingresa tu nombre de usuario: ");
            clientName = Console.ReadLine();

            try
            {
                clientSocket.Connect("127.0.0.1", 12345);
                stream = clientSocket.GetStream();
                isConnected = true;

                Thread ctThread = new Thread(GetMessage);
                ctThread.Start();

                while (isConnected)
                {
                    string message = Console.ReadLine();
                    if (!string.IsNullOrEmpty(message))
                    {
                        string fullMessage = $"{clientId}||{clientName}||{message}";
                        byte[] outStream = Encoding.UTF8.GetBytes(fullMessage);
                        stream.Write(outStream, 0, outStream.Length);
                        stream.Flush();
                    }
                }
            }
            catch (Exception ex)
            {
                Console.WriteLine("Error al conectar con el servidor: " + ex.Message);
            }
            finally
            {
                if (clientSocket != null && clientSocket.Connected)
                {
                    clientSocket.Close();
                }
            }
        }

        static void GetMessage()
        {
            try
            {
                byte[] bytesFrom = new byte[1024];
                string dataFromServer = "";

                while (isConnected)
                {
                    int bytesRead = stream.Read(bytesFrom, 0, bytesFrom.Length);
                    if (bytesRead > 0)
                    {
                        dataFromServer = Encoding.UTF8.GetString(bytesFrom, 0, bytesRead);

                        if (dataFromServer.StartsWith("ID:"))
                        {
                            clientId = dataFromServer.Substring(3);
                            Console.WriteLine("Tu ID es: " + clientId);

                            string nameMessage = "NAME:" + clientName;
                            byte[] nameBytes = Encoding.UTF8.GetBytes(nameMessage);
                            stream.Write(nameBytes, 0, nameBytes.Length);
                            stream.Flush();
                        }
                        else if (dataFromServer.StartsWith("USERS:"))
                        {
                            Console.WriteLine("Usuarios Conectados:");
                            string usersData = dataFromServer.Substring(6);
                            string[] users = usersData.Split(new string[] { "&&" }, StringSplitOptions.RemoveEmptyEntries);
                            foreach (string user in users)
                            {
                                string[] userInfo = user.Split(new string[] { "||" }, StringSplitOptions.None);
                                if (userInfo.Length == 2)
                                {
                                    string uid = userInfo[0];
                                    string uname = userInfo[1];
                                    Console.WriteLine("ID: {0}, Nombre: {1}", uid, uname);
                                }
                            }
                        }
                        else
                        {
                            Console.WriteLine(dataFromServer);
                        }
                    }
                    else
                    {
                        Console.WriteLine("El servidor ha cerrado la conexión.");
                        isConnected = false;
                    }
                }
            }
            catch (Exception ex)
            {
                Console.WriteLine("Error al recibir datos: " + ex.Message);
                isConnected = false;
            }
        }
    }
}

```

![[Pasted image 20240922202638.png]]

![[Pasted image 20240922202747.png]]
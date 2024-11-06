![[Pasted image 20240922210958.png]]<br><br><br><br>

<center>
Carrera:
</center>
<center>
<span style="font-size: 30px;">Licenciatura en Sistemas de Información</span>
</center>

<br><br><br><br><br><br>

<center><span style="font-size: 30px;">Trabajo Práctico</span></center>
<center><span style="font-size: 30px;">TP 4.2  - Ruteo Estático y RIP</span></center>


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

_***Ejercicio 1***_
1. Realizar la configuración en los router utilizando ruteo estático. Cargar las rutas necesarias para lograr conectividad entre distintas redes.
   Router R1
```bash
   ip show route
   ```
   ![[Pasted image 20241005211353.png]]

 Router R2
 ![[Pasted image 20241005211505.png]]

Router R3
![[Pasted image 20241005211712.png]]

2. Verificar la conectividad entre los hosts del escenario. Incluir en documento pruebas realizadas.

Conectividad desde area Mesa de entrada a DATACENTER
Desde P1 a Server IIS 2
![[Pasted image 20241005212037.png]]

Conectividad desde area Mesa de entrada a Administracion
Desde P1 a PC2
![[Pasted image 20241005213349.png]]

Conectividad desde Administracion a DATACENTER
Desde PC2 a Server IIS 2
![[Pasted image 20241005213543.png]]

3. ¿Cuántas redes están conectadas directamente a R1, al R2 y al R3?
Existen 3 redes conectadas a R1, y 2 conectadas a R2 y otras 2 R3.

4. Describa la cantidad de rutas estáticas que debe tener cargado cada router para poder llegar a las redes que no están conectadas directamente
Se necesita por lo menos 2 rutas estáticas por router para poder llegar a las redes que no están conectadas directamente.

5. ¿Qué ventajas y/o desventajas considera que se presentan en el escenario con la implementación del protocolo de enrutamiento estático?
A medida que se añade una nueva red, es necesario ajustar la configuración de cada router para poder conectarse a ella, lo que se convierte en una desventaja a medida que aumentan las conexiones.

_**Ejercicio 2**_

1. Añadir una interfaz sería adicional en R2 y R3, e interconectar ambos router. Realizar las configuraciones del protocolo de enrutamiento RIP necesarias.
![[Pasted image 20241005221912.png]]
![[Pasted image 20241005221925.png]]
![[Pasted image 20241005221935.png]]

3. . Utilizando traceroute verifique las trazas desde PC0 hacia Server IIS 1. Posteriormente apagar la interfaz Se1/0 de R3 y vuelva a ejecutar un traceroute entre PC0 y Server IIS 1. Explicar los resultados obtenidos. Emitir conclusiones comparativas respecto del protocolo de enrutamiento estático.

**![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXecuzcaGs1wTmwZYRToSY1qdKq01TeczSBMRlMCpBLgLDN__xlb4knZ4bokBnnDSLG3kGv-9jhBV-xgnPuavVG78JrlwI0dmhedpBDazbpaOo3ZVjVJehUebk4qvPdn1l2Wa17IVmeU-BDtR_VNSl9u4-dF5QCjJOGf_e3gFw?key=AqOTv36lCUOoX_kDn4m-GQ)**
En el primer caso, la interfaz **Se1/0** está activa, mientras que en el segundo se encuentra desactivada, lo que provoca que se utilice una ruta diferente para alcanzar el host de destino. El enrutamiento estático requiere una configuración manual de las rutas en los dispositivos de red, lo cual es útil en redes pequeñas, pero en entornos más complejos, un protocolo como **RIP** ofrece una mejor adaptación y flexibilidad

3. **En caso de que se necesite acceder desde Administración a Server IIS 2, a través de la red 172.20.0.0/16 independientemente del protocolo dinámico RIP implementado. ¿Es posible aplicarlo? Indicar justificación.**

Si es posible aplicarlo ya que se encuentran conectados mediante conexión directa vía la pasarela 172.20.0.0.
![[Pasted image 20241005222203.png]]

![[Pasted image 20241005222307.png]]
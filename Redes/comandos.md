# comandos.

conectar por ssh <usuario>@<ip_mv>

Asignar permisos de sudo 

- entrar desde la cuenta de un sudo (redes por ej)
- usermod -aG sudo <nombre_de_usuario>
- groups <nombre_de_usuario>

Crear un usuario, asignar contraseña y dar permisos

Crear usuario: Es necesario ser usuario ROOT para crear un usuario

Comando: 

- useradd -m <Nombre_Usuario>
- passwd <Nombre_Usuario>
- chmod -R 700 /home/<Nombre_Usuario>

Crear Host Virtual 

- mkdir -p /var/www/redes.
- chown -R www-data: /var/www/<Directory_Name>
- cd /etc/apache2/sites-available
- nano <Directory_Name>.conf (cp <Stable_Directory>.conf <Directory_Name>.conf)
- nano /var/www/<Directory_Name>/index.html
- nano /etc/hosts
- a2ensite 57093
- systemctl reload apache2

EXTRA:

Packet Tracer
DHCP por Router:

Router# enable

Router# configure terminal

Enter configuration commands, one per line.  End with CNTL/Z.

Router(config)#
ip dhcp pool red0

network 192.168.0.0 255.255.255.0

dns-server 192.168.0.3

default-route 192.168.0.1    (gateway)exit

Maquina Virtual
habilitar apache
1-2) crear .conf en /etc/apache2/sites-available/con el siguiente formato(puede variar)
.conf para apache <VirtualHost *:80>    ServerAdmin admin@redes2024.com.ar    DocumentRoot /var/www/sitio1.com/public_html/    ErrorLog ${APACHE_LOG_DIR}/error.log    CustomLog ${APACHE_LOG_DIR}/access.log combined
    <Location /administracion.html>        AuthType Basic        AuthName "Por favor, ingresar la contraseña"        AuthUserFile /etc/apache2/.htpasswd        Require valid-user    </Location></VirtualHost>

crear html en /var/www/ 

<!DOCTYPE html><html lang="es"><head>    <meta charset="UTF-8">    <meta name="viewport" content="width=device-width, initial-scale=1.0">    <title>Página Básica</title></head><body>    <header>        <h1>Bienvenido a mi página web</h1>    </header>    <footer>        <p>&copy; 2024 Mi Sitio Web. Todos los derechos reservados.</p>    </footer></body></html>

sudo a2ensitesudo systemctl restart apache2
3) prestar atencion al documentroot, revisar que termine en / 
4) modificar el ports.conf en /etc/apache2/
5)chown -R www-data:www-data /carpetas
sudo ufw allow sshsudo ufw allow 80/tcp
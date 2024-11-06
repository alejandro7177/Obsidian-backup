Reiniciar el cache DNS
```bash
sudo systemctl restart dnsmasq
```

Mostrar la cache local
```bash
sudo nano /etc/dnsmasq.conf
```

Ver el DNS
```bash
nmcli dev show | grep 'IP4.DNS'
```

add_user
```bash
sudo adduser USER_NAME
```

dar permisos
```bash
sudo chmod 755 NAME_DIR
```
Aca modificaremos las variables
#Variables
Ctrl + H
`56622_ = 56622`
`56622`

Apache
```bash
sudo mkdir -p /var/www/html/56622/public
```

añadir un html
```bash
sudo nano /var/www/html/56622/public/index.html
```

dar permisos a apache
```bash
sudo chown -R www-data: /var/www/html/56622/
```

crear archivo de configuracion
```bash
sudo nano /etc/apache2/sites-available/56622.conf
```

```
<VirtualHost *:80>
        ServerAdmin admin@56622
        ServerName 56622
        ServerAlias www.56622 

        DocumentRoot /var/www/html/56622/public

        #Logs
        ErrorLog ${APACHE_LOG_DIR}/redes_error.log
        CustomLog ${APACHE_LOG_DIR}/redes_access.log combined

        <Directory /var/www/html/56622/public>
                AllowOverride All
                Require all granted
        </Directory>
</VirtualHost> 
```

habilitar los host virtuales
```bash
sudo a2ensite 56622
```

ver error de sintaxis
```bash
sudo apachectl configtest
```

habilitar servername desde localhost
```bash
sudo nano /etc/apache2/apache2.conf
```

```bash
Servername localhost
```

Reiniciar apache2
```bash
sudo systemctl restart apache2
```

Definir dentro de host
```bash
sudo nano /etc/hosts
```

```
127.0.0.2       56622
127.0.0.2       www.56622
```

cambiar de puerto una pagina
```bash
sudo nano /etc/apache2/ports.conf
```

```
lister NUM_PORT
```

Crear un User
```bash
htpasswd -c /etc/apache2/.htpasswd USER_NAME
```

crear gruop auth
```bash
a2enmod authz_groupfile
```

configurar en conf
```bash
<VirtualHost *:80>
        ServerAdmin admin@56622
        ServerName 56622
        ServerAlias www.56622

        DocumentRoot /var/www/html/56622/public

        #Logs
        ErrorLog ${APACHE_LOG_DIR}/56622_error.log
        CustomLog ${APACHE_LOG_DIR}/56622_access.log combined

        <Directory /var/www/html/56622/public>
                AuthUserFile /etc/apache2/.htpasswd
                AuthGroupFile /dev/null
                AuthName "texto a mostrar ingrese la pass:"
                AuthType Basic
                Require valid-user
        </Directory>
</VirtualHost> 
```

pagina simple
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Página Simple : 56622</title>
</head>
<body>

    <h1>Bienvenido a Mi Página Simple: 56622</h1>
    <p>Esta es una página web simple en HTML.</p>

</body>
</html>
```

**_packertracer_**
enable
config t
ip dhcp pool NOMBRE_RED
network 192.168.1.0 255.255.255.0
default-router 192.168.1.1
dns-server 192.168.0.253
ip dhcp excluded-address 192.168.1.1 192.168.1.9

```mail
redesdedatos@comunidad.unne.edu.ar
```

ISCSI

ACCESS POINT
trabaja solo con la capa de enlace
no trabaja con la capa ip

convertir lo del ethernet a todo a cable

Router hogar
separa nuestra red de la de nuestro proveedor

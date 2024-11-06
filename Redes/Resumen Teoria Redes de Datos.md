# TEMA 1

Redes LAN -> Local Area Networking
Redes WAN -> Wide Area Networking

Jerarquia de redes IPS
Estructura de INTERNET
IPS TIER 1 -> IPS TIER 2 -> GOOGLE o otros Service
IPS Regional -> IXP
IPS Acceso 

ISP -> Internet Service Provedor

IXP -> Internet eXxchanges Points -> sirve para las interconexiones entre los IPS
IXPs CABASE -> Camara Argentina de internet

Hay varios IXP en toda la Argentina para las interconexiones

Dispositivos de Hardware y software para integración de redes

**Modelo ISO OSI**
Aplication
Presentation
session
transporte
network
link
physical

**Protocolo stack**
Aplication
transporte 
network
link
physical

Modelo RFC
es un papers de la ingenieria de internet
Request for Coments

# Tema 2

## Capa de aplicacion
se encarga de la comunicacion de la aplicaciones dentro de un servicio terminal
***Define:***
- la sintaxis
- tipos de mensajes
- semantica de los campos
- las reglas

Protocolos de la capa de aplicacion son:
- Cliente - Servidor: Donde un servidor esta activo constantemente para responder a las peticiones y el servidor tiene una ip fija, y el servidor si tiene muchas peticiones no va a poder responder a todas en un unico host
- P2P: Donde no se necesita un servidor sino que es de a pares donde los componentes de los pares pueden ser tanto una computadora como un netbook y son mas economicas ya que no necesitan un servidor dedicado ejemplo utorrent
Protocolos en general
mail -> SMTP
File -> FTP, TFTP
acceso remoto -> SSH

TCP -> Protocolo de la capa de transporte
_**transmission Control Protocol**_

TCP seguro es SSL Secure Socket Layer
no es un protocolo en si es una mejora de TCP


### DNS
Designet name service
existe una jerarquia de DNS
.com .ar
.edu .gob
.unne.edu .afit.edu

los dns no tiene todos los nombre de los host

### HTTP
Hiper Text Transfer Protocol 

Primero el cliente hace una conexion TCP (una conexion de control) para acceeder a una interfaz socket 

no mantiene ninguna informacion por lo tan es un protocolo sin memoria

Servidores cache -> servers proxy: Sirven de intermediario para traquear todas las solicitudes https y respuestas https

HTTP define la estructura de los mensajes y como el cliente y el servidor se comunican

hay distinta respuestas 
200 OK -> salio todo bien
403 -> cambio la url de destino redireccionamient
400 -> error genenrico
500 -> Server internal error

(RTT, Round-Trip Tim) Tiempo que tarda y se espera q vuelva una respuesta http
## Almacenamiento Arquitecturas

SAN -> Storage Area Network : son varias parte de almacenamientos que tiene un hipervisor como interfaz donde todos los storage cuenta como uno mas grade

NAS -> Network Atached Storage : Donde todos los dispositivos estan conectado al storache y el crecimiento es limitado ya que para agregar un nuevo storage abria q agregar mas conexiones a todos los dispositivos

Tipos de sistemas de archivos 

Estructura por registro: se toma una parte del disco y guarda todo en un buffe y va guardando en forma de registros periodicamente

bitacora: lleva el registro antes de realizarlo esto hay algunos en linux como lo son ext3 en linux
virtuales: los cuales sirven como intermediarios para luego pasar al sistema de archivos del sistema operativo ya que son una capa separada q sirve como interfaz entre el sistema operativo y el sistema de archivos
	
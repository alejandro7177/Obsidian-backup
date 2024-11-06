![[Red_de_datagramas.png]]
- Un paquete se transmite desde un origen a un destino pasa a través de una serie de routers. 
- Cada router utiliza la dirección de destino del paquete para reenviar dicho paquete.
- Específicamente, cada router tiene una tabla de reenvío que asigna direcciones de destino a interfaces de enlace 
- Cuando un paquete llega a un router, éste utiliza la dirección de destino del paquete para buscar la interfaz del enlace de salida apropiado en la tabla de reenvío. 
- Después, el router reenvía intencionadamente el paquete a esa interfaz del enlace de salida.

## Componentes Basicos de un Router
- Puertos de entrada
- Entramado de conmutación: conecta los puertos de salida con los de entrada
- Puertos de salida
- Procesador de enrrutamiento

## Entidad autoritaria global
Las IP son designada por la ICANN el papel de esta organización es la de asignar las direcciones IP y gestionar los servidores raíz DNS y asignar nombres de dominio

## Ruteo
El ruteo es el hecho de pasar mensajes entre routers que tienen protocolos compatibles entre si
### Estáticas
el administrador las agrega manualmente al router
- Las rutas son establecidas por el administrador manualmente
- Propenso a errores
- Si se cambia la topología requiere cambios manuales en los routers
- Sirve cuando se tiene una red sencilla
- No tiene problemas de seguridad ni de incompatibilidad
- No implica costo de procesamiento extra
- Mayor Control
- Esquema NO escalable y NO tolerante a fallos
### Dinámicas
Son aprendidas por medio de protocolos de ruteo y ajustes automáticos

Un grafico $G= (N,E)$ es un conjunto N de nodos y una coleccion $E$ de aristas, donde cada arista es una pareja de nodos
Para cualquier arista tiene un valor que representa su costo
Para cualquier arista $(x,y)$ de $E$ designamos $c(x,y)$ como el costo de las aristas entre nodos $x$ e $y$ 
![[Modelo_grafo_de_una_red_de_computadoras.png]]

**El problema del costo mínimo está claro:** hallar una ruta entre el origen y el destino que tenga el costo mínimo

## Algoritmo de enrutamiento global
Calcular la ruta minima entre un origen y un destino utilizando el conocimiento global de la red. En la práctica, los algoritmos con información de estado global a menudo se denominan algoritmos de estado de enlaces (LS, Link-State)

## Algoritmo de enrutamiento descentralizado
El calculo de la ruta minima entre un origen y un destino se realiza de forma iterativa y distribuida. Ejemplo de algoritmo de enrutamiento descentralizado se denomina algoritmo de vector distancia (DV, Distance-Vector)

### IGP (Interior Gateway Protocols) trabajan en el mismo AS 
- RIP (Routing Internet Protocol) , v1, v2 (estándar IETF) 
- IGRP e EIGRP (-Enhanced- Interior Gateway Routing Protocol) (propietarios de cisco)
- OSPF (Open Shortest Path First) , v2 , v3 (estándar IETF)
- IS-IS (Intermediate System to Intermediate System) (estándar de la ISO) 
### EGP (Exterior Gateway Protocols), trabajan entre diferentes AS
- GGP (Gateway to Gateway Protocol) (antecesor)
- EGP (Exterior Gateway Protocol) (estándar IETF, en desuso)
- BGP (Border Gateway Protocol) (estándar IETF)



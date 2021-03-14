# PRACTICA 1 REDES DE COMPUTADORAS
# UNIVERSIDAD SAN CARLOS DE GUATEMALA
# CESAR ALEJANDRO SAZO QUISQUINAY 201513858
# HEIDY LISSETH MENDOZA CARDONA   201503811
# J


## Emphasis

*This text will be italic*  


## Lists

### CONFIGURACION VPN   
* Red Vpn
![This is a alt text.](/Imagenes/vpn_.png "This is a sample image.")

* Configuracion de la VPN

Primero abrimos la consola de la MV y luego colocamos el siguiente comando.

* wget https://cubaelectronica.com/OpenVPN/openvpn-install.sh && sudo bash openvpn-install.sh


Luego Colocamos el ip externo de la mv.

Colocamos el protocolo UDP.

Hacemos que la vpn escuche el puerto 1194.

![This is a alt text.](/Imagenes/vpn1.png "This is a sample image.")


Colocamos que queremos utilizar la VPN de Google.

![This is a alt text.](/Imagenes/vpn2.png "This is a sample image.")

Luego esperamos que cree el cliente  escribiendo una llave.

![This is a alt text.](/Imagenes/vpn3.png "This is a sample image.")


Si queremos crear otro cliente basta con colocar 

* sudo bash openvpn-install.sh


### CONFIGURACION TOPOLOGIA 1
* TOPOLOGIA1
![This is a alt text.](/Imagenes/topologia1.PNG "This is a sample image.")



Se configuran las ip de las vpc

* INFORMATICA
![This is a alt text.](/Imagenes/Informatica2.PNG "INFORMATICA")
* VENTAS
![This is a alt text.](/Imagenes/Ventas2.PNG "VENTAS")
* CONTABILIDAD1
![This is a alt text.](/Imagenes/contabilidad1.PNG "CONTABILIDAD")

Se configuran las ip de las maquinas virtuales 
* CONTABILIDAD2
#
![This is a alt text.](/Imagenes/contabilidad2.PNG "CONTABILIDAD")
* INFORMATICA1
#
![This is a alt text.](/Imagenes/informatica1.PNG "This is a sample image.")
* VENTAS1
#
![This is a alt text.](/Imagenes/ventas1.PNG "This is a sample image.")

Luego se configuran los Switches
  Se colocan en modo troncal los puertos que tienen conexiones con otro switch y 
  a los otros se les coloca la vlan correspondiente al departamento
* SWICHT1
#
![This is a alt text.](/Imagenes/switch1.PNG "This is a sample image.")
* SWITCH2
#
![This is a alt text.](/Imagenes/switch2.PNG "This is a sample image.")
* SWITCH3
#
![This is a alt text.](/Imagenes/switch3.PNG "This is a sample image.")
* SWITCH4
#
![This is a alt text.](/Imagenes/switch4.PNG "This is a sample image.")

Por ultimo se configura la nube agregando un UDP tunnel con la ip y los
puertos del servidor

* CLOUD
#
![This is a alt text.](/Imagenes/cloud.PNG "CLOUD")


Para comprobar que la configuración de la red fue exitosa se realiza ping entre
las maquinas virtuales y las vpc
* PING INFORMATICA DE LA MAQUINA VIRTUAL A LA VPC 
#
![This is a alt text.](/Imagenes/pinginfo1-info2.PNG "This is a sample image.")
* PING INFORMATICA DE LA VPC A LA MAQUINA VIRTUAL
![This is a alt text.](/Imagenes/pinfinfo2-info1.PNG "This is a sample image.")
* PING CONTABILIDAD DE LA VPC A LA MAQUINA VIRTUAL
#
![This is a alt text.](/Imagenes/pingconta1-conta2.PNG "This is a sample image.")
* PING CONTABILIDAD DE LA MAQUINA VIRTUAL A LA VPC
#
![This is a alt text.](/Imagenes/pingconta2-conta1.PNG "This is a sample image.")

* PING VENTAS DE LA MAQUINA VIRTUAL A LA VPC
![This is a alt text.](/Imagenes/pingventas1-ventas2.PNG "This is a sample image.")
* PING VENTAS DE LA VPC A LA MAQUINA VIRTUAL
![This is a alt text.](/Imagenes/pingventas2-ventas1.PNG "This is a sample image.")

Para conectar con la Topología 2 se utiliza la vpn, se utilizó el cliente 2
* VPN
#
![This is a alt text.](/Imagenes/vpn.PNG "This is a sample image.")


### CONFIGURACION TOPOLOGIA 2

* TOPOLOGIA2
![This is a alt text.](/Imagenes/topo2.png "This is a sample image.")



* Configuracion de la Nuve:







* switch 1 

* configuracion de los  puertos del switch 1 como modo troncal

* puerto 1 
![This is a alt text.](/Imagenes/st1.png "This is a sample image.")

* puerto 2
![This is a alt text.](/Imagenes/st2.png "This is a sample image.")




* switch 2 

* puerto 0  a modo troncal
![This is a alt text.](/Imagenes/s1.png "This is a sample image.")

* puerto 1 con vlan 30
![This is a alt text.](/Imagenes/s2.png "This is a sample image.")


* puerto 2 con vlan 10
![This is a alt text.](/Imagenes/s3.png "This is a sample image.")



* switch 3

* puerto 0 a modo troncal 
![This is a alt text.](/Imagenes/s4.png "This is a sample image.")

* puerto 1 a vlan 20 
![This is a alt text.](/Imagenes/s5.png "This is a sample image.")


  

* CONFIGURACION DE LAS DIRECCIONES IP DE LOS SERVIDORES
![This is a alt text.](/Imagenes/s6.png "This is a sample image.")

* Servidor Ventas configuracion ip 



* Servidor Contabilidad Configuracion ip 



* servidor informatica configuracion ip 






### PING ENTRE MAQUINAS 

* Ventas
* Ping Vlan Ventas en diferentes equipos 
![This is a alt text.](/Imagenes/pingventas.png "This is a sample image.")

* muestra de la pagina del server Ventas
![This is a alt text.](/Imagenes/pingventasp.png "This is a sample image.")




* Contabilidad
* Ping Vlan Contabilidad en diferentes equipos 
![This is a alt text.](/Imagenes/pingconta.png "This is a sample image.")

* muestra de la pagina del server Contabilidad
![This is a alt text.](/Imagenes/pingcontap.png "This is a sample image.")






* Informatica 
* Ping Vlan Informatica en diferentes equipos 
![This is a alt text.](/Imagenes/pinginfor.png "This is a sample image.")

* muestra de la pagina del server Informatica
![This is a alt text.](/Imagenes/pinginforp.png "This is a sample image.")











### CONFIGURACION DE CADA SERVIDOR

* INSTALANDO APACHE 

* actualizamos paquetes
![This is a alt text.](/Imagenes/apache1.png "This is a sample image.")

* actualizamos dependencias 
![This is a alt text.](/Imagenes/apache2.png "This is a sample image.")

* instalamos apache
![This is a alt text.](/Imagenes/apache3.png "This is a sample image.")

* actualizamos las herramientas de apache 
![This is a alt text.](/Imagenes/apache4.png "This is a sample image.")

* Iniciamos el Servicio de apache 

![This is a alt text.](/Imagenes/apache5.png "This is a sample image.")

* miramos el status de apache 
![This is a alt text.](/Imagenes/apache6.png "This is a sample image.")


* Modificamos las paginas que trae apache por defecto.
![This is a alt text.](/Imagenes/apache7.png "This is a sample image.")


* Realizamos estos pasos con cada servidor


### PAGINAS DE SERVIDORES

* Pagina de Ventas
![This is a alt text.](/Imagenes/pagina3.png "This is a sample image.")



* Pagina de Contabilidad
![This is a alt text.](/Imagenes/pagina1.png "This is a sample image.")


* Pagina de Informatica
![This is a alt text.](/Imagenes/pagina2.png "This is a sample image.")




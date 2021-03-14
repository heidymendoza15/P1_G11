# PRACTICA 1 REDES DE COMPUTADORAS
# UNIVERSIDAD SAN CARLOS DE GUATEMALA
# CESAR ALEJANDRO SAZO QUISQUINAY 201513858
# HEIDY LISSETH MENDOZA CARDONA   201503811


## Emphasis

*This text will be italic*  


## Lists

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

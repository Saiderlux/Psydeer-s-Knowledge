El conjunto de protocolos **TCP/IP** es un grupo de protocolos que permiten la comunicación entre dos computadoras. Se encarga de gestionar los errores en la transmisión y de administrar el enrutamiento y la entrega de datos.

---

## Capas del Modelo TCP/IP

El modelo TCP/IP está compuesto por las siguientes capas:

- **Capa de aplicación**: Es la capa más cercana al usuario y define los protocolos que utilizan las aplicaciones para proporcionar servicios.
    
- **Capa de transporte**: Establece los canales básicos para la transferencia de datos entre dos puntos. Puede incluir mecanismos de seguridad y protocolos para la segmentación de paquetes, el control de errores y el flujo de los mismos.
    
- **Capa de internet**: Se encarga de la estructura de los paquetes de datos que circulan por la red y cómo enviarlos. Identifica los equipos en la red a través de una dirección IP y se encarga del direccionamiento de los datagramas para que lleguen a su destino.
    
- **Capa de acceso a la red**: Define el acceso físico de los equipos a la red y los protocolos que intervienen. También define la topología física y cómo se mueven los paquetes entre las interfaces de la capa de internet.
    

---

## Protocolos clave

- **TCP (Transmission Control Protocol)**: Este es uno de los principales protocolos de la capa de transporte. Es responsable de establecer y permitir la conexión entre dos equipos, asegurando el intercambio de datos entre ellos. Agrupa los datos en **datagramas** y les añade su propio encabezado para garantizar un transporte correcto.
    
- **IP (Internet Protocol)**: Es parte de la capa de internet y se encarga de proporcionar una dirección IP a todos los equipos conectados a una red. Aunque es uno de los protocolos más importantes de internet, no garantiza la entrega ni el orden de los paquetes de datos.
    

## Comunicación entre clientes y servidores

Las aplicaciones TCP/IP operan bajo el modelo **cliente/servidor**. En este modelo, los servidores esperan y procesan las solicitudes de los programas cliente. Los clientes abren un **socket** para comunicarse con los servidores, que es una conexión TCP entre las dos máquinas.

Los servidores escuchan las solicitudes de conexión en **puertos** específicos, que son referencias numéricas que indican el programa de servidor de destino. Por ejemplo, los servidores web escuchan en el puerto 80, mientras que los servidores SMTP lo hacen en el puerto 25.
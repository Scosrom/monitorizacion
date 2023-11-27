# Redes

```
 tcpdump -n -i eno1 net 172.26.0.0/16
```

Este comando utiliza tcpdump, una herramienta de línea de comandos en sistemas Unix y Linux que permite capturar y mostrar el tráfico de red en tiempo real. Aquí está la explicación de los parámetros utilizados en el comando:

**-n**: Indica a tcpdump que no realice la resolución inversa de direcciones IP a nombres de host. Esto significa que las direcciones IP se mostrarán numéricamente en lugar de intentar convertirlas en nombres de dominio.

**-i eno1**: Especifica la interfaz de red que tcpdump debe utilizar para capturar el tráfico. En este caso, la interfaz es eno1. Puedes reemplazar eno1 con el nombre de la interfaz que estás utilizando en tu sistema.

**net 172.26.0.0/16**: Define un filtro para capturar el tráfico de red que pertenece a la red 172.26.0.0 con una máscara de subred de 16 bits (lo que significa que incluirá todas las direcciones IP desde 172.26.0.0 hasta 172.26.255.255). Este filtro asegura que solo se capture el tráfico que pertenece a esa red específica.


```
tcptrack -i eno1
```
El comando tcptrack es otra herramienta útil para monitorear la actividad de red en sistemas Unix y Linux. En este caso, estás utilizando tcptrack para seguir la actividad TCP en la interfaz de red eno1. Aquí está la explicación del comando:

**-i eno1**: Especifica la interfaz de red que tcptrack debe monitorear. En este caso, la interfaz es eno1. Puedes reemplazar eno1 con el nombre de la interfaz que estás utilizando en tu sistema.
tcptrack visualiza la actividad TCP en tiempo real, mostrando información sobre las conexiones TCP establecidas, las tasas de transferencia, las direcciones IP y los puertos involucrados, entre otros detalles. Este tipo de herramienta es útil para obtener una visión rápida de qué conexiones TCP están activas en tu sistema en un momento dado.

```
sudo apt-get install tcptrack
```


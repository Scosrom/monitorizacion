<h1 align="center">🚦   Monitorización  🚦 </h1>

<p align="center">
  <img src="https://github.com/Scosrom/monitorizacion/assets/114906778/9f996f9a-9351-4f89-b220-05b1e5924d21" alt="Descripción de la imagen">
</p>


<h2> Introducción </h2>

La monitorización es un aspecto crítico en la gestión de sistemas y redes. Proporciona información en tiempo real sobre el rendimiento, la disponibilidad y el estado de los recursos. Este documento abordará diversas herramientas y enfoques utilizados en el ámbito de la monitorización.

## Índice

1. Herramientas Propias del sistema
   
**PROCESOS**

 -  1.1. top
     
 -  1.2  Atop
     
 -  1.3  htop

**DISCOS**


     
**REDES**

  - 3.1  Tcpdump

  - 3.2  Tcptrack

  - 3.3 iptraf

  - 3.4 netstat
   
2 . Sistemas de monitorización
     
  - 2.1  Prometheus
     
  - 2.2  Exporters
     
  - 2.3  Grafana
   
<h2> Contenidos  </h2>

### 📊 **Procesos** 📈

#### 1. [Herramientas propias del sistema](herramientas.md)

En esta sección, se presentan algunas herramientas propias del sistema que son útiles para la monitorización.

   - [1.1. top](top.md)
     
   - [1.2. atop](atop.md)

   - [1.3. htop](htop.md)
     
     
---

### 💽 **Discos** 💾

  - [2.1. df](discosh.md)

Descripción: El comando df muestra información sobre el espacio disponible y utilizado en los sistemas de archivos montados. Proporciona detalles sobre la capacidad, el espacio utilizado, el espacio libre y el tipo de sistema de archivos.

  - [2.2. du](discosh.md)

Descripción: La utilidad du se utiliza para estimar el espacio utilizado por directorios y archivos en un sistema de archivos. Permite identificar qué directorios o archivos están ocupando más espacio.

  - [2.3. iostat](discosh.md)

Descripción: El comando iostat muestra estadísticas de entrada/salida del sistema, incluyendo información sobre el rendimiento de los discos. Proporciona datos sobre la tasa de transferencia, el tiempo de respuesta y la actividad de lectura/escritura.

  - [2.4. lsof](discosh.md)

Descripción: lsof (List Open Files) muestra una lista de archivos abiertos por procesos en el sistema. Es útil para identificar qué procesos tienen archivos abiertos en dispositivos de almacenamiento.

  - [2.6. blkid](discosh.md)

Descripción: El comando blkid muestra información sobre los dispositivos de bloque, como UUID (Identificador Único Universal) y el tipo de sistema de archivos. Es útil para identificar discos y particiones.

  - [2.7. fdisk](discosh.md)

Descripción: fdisk es una herramienta para la manipulación de tablas de particiones en discos. Se utiliza para crear, modificar y eliminar particiones en discos duros.


---

### 🌐 **Redes** 🌏

#### 1. [Herramientas propias del sistema]

   - [1.1 tcpdump](tcpdump.md)
   
Descripcion:  Es una potente herramienta de línea de comandos para la captura y análisis de paquetes en una red. Permite ver el tráfico en tiempo real o guardar la captura en un archivo para su posterior análisis.

   - [1.2 tcptrak](tcptrack.md)
   
Descripcion: Es una herramienta que muestra información en tiempo real sobre las conexiones TCP activas en una red. Proporciona una interfaz de usuario simple y colorida que muestra las conexiones en curso, su estado, la cantidad de datos transferidos y más.

   - [1.3 iptraf](iptraf.md)

Descripcion: Es una herramienta de monitoreo de red basada en texto que muestra información detallada sobre el tráfico IP en tiempo real. 

  - PUERTOS:

  - [netstat](netstat.md)
   
   - [Comandos](redes.md)
---

#### 2. [Sistemas de monitorización](herramientas.md)

En esta sección, se exploran herramientas clave para la monitorización de sistemas.

   - [2.1. Prometheus](prom.md)
     
Descripción: Prometheus es un sistema de monitorización y alerta de código abierto diseñado para gestionar entornos altamente dinámicos. Puede recopilar métricas de diversas fuentes, almacenarlas y permitir consultas y alertas basadas en esas métricas

   - [2.2. Exporters](exporters.md)

Descripción: Los Exporters en Prometheus son componentes adicionales que recopilan métricas específicas de sistemas y servicios y las exponen en un formato que Prometheus puede entender. Estos son esenciales para la integración de Prometheus con diferentes tecnologías.
   
   - [2.3. Grafana](graf.md)

Descripción: Grafana es una plataforma de análisis y visualización que se integra bien con sistemas de monitorización como Prometheus

   - [2.4. Script instalacion](pg.sh)

   - [2.5 Script Apache_exporter](ae.sh)

<h2 align="center">  Referencias  </h2>

1. [Nagios Documentación](https://assets.nagios.com/downloads/nagioscore/docs/nagioscore/4/en/)
2. [Prometheus Documentación](https://prometheus.io/docs/introduction/overview/)

<h2 align="center"> Licencia  </h2>

![licencia](/img/88x31.png)

<h1 align="center">🚦   Monitorización  🚦 </h1>

<p align="center">
  <img src="https://github.com/Scosrom/monitorizacion/assets/114906778/9f996f9a-9351-4f89-b220-05b1e5924d21" alt="Descripción de la imagen">
</p>


<h2> Introducción </h2>

La monitorización es un aspecto crítico en la gestión de sistemas y redes. Proporciona información en tiempo real sobre el rendimiento, la disponibilidad y el estado de los recursos. Este documento abordará diversas herramientas y enfoques utilizados en el ámbito de la monitorización.

## Índice

### 1. Herramientas Propias del sistema
   
  **PROCESOS**

 -  1.1. top
     
 -  1.2  Atop
     
 -  1.3  htop

  **DISCOS**

  - 2.1. df

  - 2.2. du

  - 2.3. iostat

  - 2.4. lsof

  - 2.6. blkid

  - 2.7. fdisk

  **REDES**

  - 3.1  Tcpdump

  - 3.2  Tcptrack

  - 3.3 iptraf

  - 3.4 netstat
   
### 2 . Sistemas de monitorización
     
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

  - [2.2. du](discosh.md)

  - [2.3. iostat](discosh.md)

  - [2.4. lsof](discosh.md)

  - [2.6. blkid](discosh.md)

  - [2.7. fdisk](discosh.md)


---

### 🌐 **Redes** 🌏

  - [3.1 tcpdump](redes.md)
   
  - [3.2 tcptrak](redes.md)
   
  - [3.3 iptraf](redes.md)

  - [3.4 netstat](redes.md)
   
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

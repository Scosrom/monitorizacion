# Atop


atop es una herramienta de monitoreo del sistema en tiempo real en sistemas basados en Unix, como Linux. Proporciona información detallada sobre el uso del sistema, la carga de trabajo y la actividad de los procesos. A diferencia de top, atop también almacena datos históricos, lo que permite revisar la actividad del sistema en el pasado.

| Opción         | Descripción                                   |
| --------------- | --------------------------------------------- |
| `-a`            | Muestra la actividad de todos los procesos, no solo de los activos  |
| `-d`            | Cambia el intervalo de actualización          |
| `-n`            | Especifica el número de actualizaciones antes de salir  |
| `-u`            | Filtra los procesos por un usuario específico  |
| `c`             | Cambia la visualización de procesos           |
| `d`             | Cambia la visualización de discos             |
| `n`             | Cambia la visualización de red                |
| `q`             | Sale de la aplicación                        |


## Características

- Guarda estadísticas del sistema.
- Empieza a tomar datos, desde el momento que se instala.

- Servicio: systemctl status atop
- Fichero: /etc/default/atop

- /var/log/atop_fecha
- atop -r /var/log/atop_fecha

### 1. instalación:

Puedes instalar atop en muchos sistemas Linux utilizando el gestor de paquetes de tu distribución. Por ejemplo, en sistemas basados en Debian/Ubuntu, puedes usar:

```
sudo apt-get install atop

```


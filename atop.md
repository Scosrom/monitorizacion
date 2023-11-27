# Atop

![atop](/img/atop.png)

atop es una herramienta de monitoreo del sistema en tiempo real en sistemas basados en Unix, como Linux. Proporciona información detallada sobre el uso del sistema, la carga de trabajo y la actividad de los procesos. A diferencia de top, atop también almacena datos históricos, lo que permite revisar la actividad del sistema en el pasado.

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

### 2. Ejecución:

Después de la instalación, puedes ejecutar atop simplemente escribiendo el comando en la terminal.

```
atop

```

### 3. Interfaz

atop tiene una interfaz de línea de comandos similar a top, pero con características adicionales. La pantalla principal muestra la carga del sistema, el uso de CPU, memoria, procesos activos y más

### 4. Navegación

Puedes navegar por las diferentes secciones utilizando las teclas de dirección y otras teclas de función

## Archivos utilizados por 'atop':

1. Registro Binario:

atop mantiene un registro binario en el sistema. Por lo general, se almacena en el directorio /var/log/atop/. Este registro contiene datos históricos sobre el uso del sistema.

2. Configuración:

El archivo de configuración principal de atop es /etc/default/atop. Puedes ajustar la configuración según tus necesidades.

## Comandos útiles en 'atop':

1. Cambiar la Vista:

Puedes cambiar entre las diferentes vistas presionando las teclas correspondientes (por ejemplo, c para la vista de CPU, m para la vista de memoria).

2. Ver Historial:

Utiliza las teclas t y T para avanzar y retroceder en el tiempo para ver el historial.

3. Filtrar Procesos:

Puedes filtrar procesos específicos presionando la tecla F y proporcionando un criterio de filtrado.

4. Guardar y Salir:

Para salir de atop y guardar los datos históricos, simplemente presiona la tecla q.

### Visualización del Registro Binario:

1. atop -r archivo_registro:

Puedes revisar los datos históricos utilizando el comando atop -r seguido del nombre del archivo de registro binario

```
atop -r /var/log/atop/atop_20230101

```

2. Generar informes:

También puedes generar informes en formato ASCII o HTML a partir de los datos históricos.

```
atop -r /var/log/atop/atop_20220101 -P -w informe.html

```

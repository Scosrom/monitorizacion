# top

![image](https://github.com/Scosrom/monitorizacion/assets/114906778/72338e0c-ba0d-42dc-878f-40dd5f5f517d)



El comando top es una herramienta de línea de comandos en sistemas Unix/Linux que proporciona información en tiempo real sobre el rendimiento del sistema y la actividad de los procesos. Permite a los usuarios monitorear de manera interactiva diversos aspectos del sistema, incluyendo la carga de la CPU, el uso de memoria, las estadísticas de la red y la lista de procesos en ejecución.

<code>PID (Process ID): </code> Identificador único para cada proceso en ejecución.

<code>USER:</code> El nombre del usuario que inició el proceso.

<code>PR (Priority):</code> La prioridad del proceso.

<code>NI (Nice value):</code> El valor de "niceness" del proceso, que afecta su prioridad.

<code>VIRT (Virtual Memory):</code> La cantidad total de memoria virtual utilizada por el proceso.

<code>RES (Resident Memory):</code> La cantidad de memoria física (RAM) utilizada por el proceso.

<code> SHR (Shared Memory):</code> La cantidad de memoria compartida utilizada por el proceso.

<code>S (%CPU):</code> El porcentaje de uso de la CPU por parte del proceso.

<code>MEM (%MEM):</code> El porcentaje de memoria RAM utilizada por el proceso.

<code>TIME+:</code> El tiempo total de CPU que ha consumido el proceso desde su inicio.

<code>COMMAND:</code> El comando o la ruta del ejecutable que inició el proceso.

| Opción         | Descripción                                   |
| --------------- | --------------------------------------------- |
| `-d`            | Especifica el intervalo de actualización en segundos  |
| `-u`            | Filtra los procesos por un usuario específico  |
| `-p`            | Muestra los procesos con IDs específicos      |
| `Shift + E`     | Cambia la unidad de medida de CPU a porcentaje de tiempo en lugar de por núcleo  |
| `Shift + M`     | Ordena la lista de procesos por uso de memoria  |
| `Shift + P`     | Ordena la lista de procesos por uso de CPU      |

# Comando `top` en Linux

```bash
# Uso Básico
top

# Opciones Comunes
## Ordenar por CPU
top -o %CPU

## Ordenar por memoria
top -o %MEM

## Filtrar por usuario
top -u nombre_usuario

## Cambiar intervalo de actualización
top -d segundos

## Mostrar ayuda
top -h

# Interacción en la Interfaz
## Kill proceso
# Presiona 'k', ingresa el PID y presiona Enter

## Cambiar unidades de memoria
# Presiona 'e' para cambiar entre unidades (KB, MB, GB)

## Mostrar/Ocultar columnas
# Presiona 'f' para agregar o quitar columnas

# Ejemplos Adicionales
## Top 5 procesos por CPU
top -o %CPU -n 5

## Mostrar procesos de usuario y actualizar cada 2 segundos
top -u nombre_usuario -d 2


<img src="https://github.com/Scosrom/monitorizacion/assets/114906778/6b9aa87a-8589-44ef-af17-6e0178949595" width="600" height="600">

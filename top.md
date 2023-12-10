# top

![image](https://github.com/Scosrom/monitorizacion/assets/114906778/a2ab92f3-ae9f-478f-bfab-abeee75e0120)


El comando top es una herramienta de línea de comandos en sistemas Unix/Linux que proporciona información en tiempo real sobre el rendimiento del sistema y la actividad de los procesos. Permite a los usuarios monitorear de manera interactiva diversos aspectos del sistema, incluyendo la carga de la CPU, el uso de memoria, las estadísticas de la red y la lista de procesos en ejecución.

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

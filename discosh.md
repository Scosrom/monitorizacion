# df

Descripción: El comando df muestra información sobre el espacio disponible y utilizado en los sistemas de archivos montados. Proporciona detalles sobre la capacidad, el espacio utilizado, el espacio libre y el tipo de sistema de archivos.

| Opción | Descripción                   |
|--------|-------------------------------|
| -h     | Muestra tamaños en formato legible para humanos.     |
| -T     | Muestra el tipo de sistema de archivos.              |
| -i     | Muestra el uso de inodos (número de archivos).      |
| -a     | Muestra información de todos los sistemas de archivos, no solo los montados. |

---

# du

Descripción: La utilidad du se utiliza para estimar el espacio utilizado por directorios y archivos en un sistema de archivos. Permite identificar qué directorios o archivos están ocupando más espacio.

| Opción | Descripción                        |
|--------|------------------------------------|
| -h     | Muestra tamaños en formato legible para humanos.     |
| -s     | Muestra solo el total de cada argumento.              |
| -c     | Muestra el total acumulado al final.                   |
| -k     | Muestra tamaños en kilobytes.                         |

---

# iostat

Descripción: El comando iostat muestra estadísticas de entrada/salida del sistema, incluyendo información sobre el rendimiento de los discos. Proporciona datos sobre la tasa de transferencia, el tiempo de respuesta y la actividad de lectura/escritura.


| Opción | Descripción                      |
|--------|----------------------------------|
| -c     | Muestra resúmenes de CPU.        |
| -d     | Muestra resúmenes de dispositivos de bloques.        |
| -h     | Muestra tamaños en formato legible para humanos.     |
| -t     | Muestra el tiempo en cada línea.                      |

---

# lsof

Descripción: lsof (List Open Files) muestra una lista de archivos abiertos por procesos en el sistema. Es útil para identificar qué procesos tienen archivos abiertos en dispositivos de almacenamiento.

| Opción | Descripción                   |
|--------|-------------------------------|
| -i     | Filtra por conexiones de red. |
| -u     | Filtra por usuarios.          |
| -p     | Filtra por PID.               |
| -c     | Filtra por nombre de comando. |

# blkid

| Opción | Descripción                   |
|--------|-------------------------------|
| -o     | Especifica el formato de salida. Puede ser list, value, o full. |
| -p     | Evita escanear particiones.    |

Descripción: El comando blkid muestra información sobre los dispositivos de bloque, como UUID (Identificador Único Universal) y el tipo de sistema de archivos. Es útil para identificar discos y particiones.

# fdisk

Descripción: fdisk es una herramienta para la manipulación de tablas de particiones en discos. Se utiliza para crear, modificar y eliminar particiones en discos duros.

| Opción | Descripción                   |
|--------|-------------------------------|
| -l     | Lista las particiones del sistema. |
| -u     | Muestra la tabla de particiones en sectores (en lugar de cilindros).          |
| -p     | Muestra la tabla de particiones en formato fácilmente procesable. |
| -n     | Añade una nueva partición.                                               |
| -d     | Elimina una partición.                                                    |
| -t     | Cambia el tipo de una partición.                                          |
| -w     | Escribe la tabla de particiones en el disco y sale.                        |
| -q     | Sale sin guardar cambios.                                                  |

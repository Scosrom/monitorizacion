## Instalación de Grafana
Por defecto, en los repositorios de Debian no viene el paquete de Grafana, por lo que tendremos que añadir el repositorio manualmente. Para este tutorial usaremos el repositorio OSS. Primero deberemos de tener algunos paquetes instalados y las llaves para el repositorio:

```
apt install apt-transport-https software-properties-common wget
wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -
```

Luego crearemos el fichero del repositorio:

```
# nano /etc/apt/sources.list.d/grafana.list
```

Y añadimos el siguiente contenido:

```
deb https://packages.grafana.com/oss/deb stable main
```
Guardamos el fichero y actualizamos repositorios:

```
# apt update
```

Finalmente, instalamos el paquete:

```
# apt install grafana
```

Tras instalarle, iniciamos el servicio y lo añadimos al arranque:

```
# systemctl start grafana-server
# systemctl enable grafana-server
```
Una vez el servicio está levantado, podemos iniciar sesión desde el navegador accediendo al puerto 3000. El usuario y contraseña por defecto es admin y luego nos pedirá de cambiarlo.


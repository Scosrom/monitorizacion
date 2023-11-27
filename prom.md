# Instalar Prometheus en GNU/Linux

Para descargar la última aplicación, lo que haremos será descargar la última versión disponible en la pagina de Github de Prometheus. Para cuando se escribe este tutorial, la última versión es la v2.39.1:

```
 wget https://github.com/prometheus/prometheus/releases/download/v2.39.1/prometheus-2.39.1.linux-amd64.tar.gz
 ```
Una vez descargado, procedemos a descomprimir el binario:

``` 
# tar -xzf prometheus-*linux-amd64.tar.gz
# mv prometheus-*linux-amd64 prometheus
# mkdir -p /var/lib/prometheus
# mkdir -p /etc/prometheus
# cp prometheus/prometheus.yml /etc/prometheus
# mv prometheus/prometheus prometheus/promtool /usr/local/bin/
# mv prometheus/consoles/ prometheus/console_libraries/ /etc/prometheus/
```

### Configurar usuario

El servicio de Prometheus debe ser ejecutado bajo un usuario, como que éste no existe en nuestro sistema, lo deberemos de crear:

``` 
# groupadd --system prometheus
# useradd -s /sbin/nologin --system -g prometheus prometheus

```

Configuramos los permisos del binario de Prometheus con el nuevo usuario:

```
# chown prometheus:prometheus /etc/prometheus
# chown prometheus:prometheus /var/lib/prometheus
# chown -R prometheus:prometheus /etc/prometheus/consoles
# chown -R prometheus:prometheus /etc/prometheus/console_libraries
```

Configurar servicio con SystemD
Para poder gestionar Prometheus como un servicio, tenemos que crear el siguiente fichero y añadir el contenido:

```
# nano /etc/systemd/system/prometheus.service
```

```
[Unit]
Description=Prometheus Server
Wants=network-online.target
After=network-online.target

[Service]
User=prometheus
Group=prometheus
Type=simple
ExecStart= /usr/local/bin/prometheus \
--config.file /etc/prometheus/prometheus.yml \
--storage.tsdb.path /var/lib/prometheus/ \
--web.console.templates=/etc/prometheus/consoles \
--web.console.libraries=/etc/prometheus/console_libraries

[Install]
WantedBy=multi-user.target
```

Iniciamos el servicio que acabamos de agregar:

```
# systemctl daemon-reload
# systemctl start prometheus.service
# systemctl enable prometheus.service
```

Tras iniciar el servicio, podremos acceder a Prometheus por el puerto 9090.


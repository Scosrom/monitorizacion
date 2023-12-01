# Instalar Prometheus en GNU/Linux


![0_Pn1vXqSDvpl1sJkh](https://github.com/Scosrom/monitorizacion/assets/114906778/e9d72303-e764-43e7-a77e-1010e7980faa)



## **Crear y configurar usuario y directorios Prometheus**

### **Creación de un Usuario para Prometheus.**

```
useradd --no-create-home --shell /bin/false prometheus
```

Explicacion de los Parámetros: 

* --no-create-home: Esta opción indica al sistema que no debe crear automáticamente un directorio de inicio para el nuevo usuario.

* --shell /bin/false: El usuario "prometheus" no podrá iniciar sesión de manera interactiva.

### **Crear directorio donde vamos a Instalar Prometheus**

```
mkdir /etc/prometheus
```
### **Crear el directorio de /var de prometheus**

```
mkdir /var/lib/prometheus
```

### **Indicamos que el Usuario prometheus sea el propietario de ambos archivos**

```
chown prometheus:prometheus /etc/prometheus/
chown prometheus:prometheus /var/lib/prometheus/
```

## Instalar Prometheus

#### Descargar prometheus

```
apt install curl
curl -LO https://github.com/prometheus/prometheus/releases/download/v2.48.0/prometheus-2.48.0.linux-amd64.tar.gz
```

#### Descomprimir prometheus

```
tar xvf prometheus-2.48.0.linux-amd64.tar.gz
```

#### Copiar prometheus a los directorios de binarios:

```
sudo cp prometheus-2.48.0.linux-amd64/prometheus /usr/local/bin/
sudo cp prometheus-2.48.0.linux-amd64/promtool /usr/local/bin/
sudo chown prometheus:prometheus /usr/local/bin/prometheus
sudo chown prometheus:prometheus /usr/local/bin/promtool
sudo cp -r prometheus-2.48.0.linux-amd64/consoles /etc/prometheus
sudo cp -r prometheus-2.48.0.linux-amd64/console_libraries /etc/prometheus
sudo chown -R prometheus:prometheus /etc/prometheus/consoles
sudo chown -R prometheus:prometheus /etc/prometheus/console_libraries
rm -rf prometheus-2.48.0.linux-amd64.tar.gz prometheus-2.48.0.linux-amd64
```

#### Editar el fichero prometheus

```
nano /etc/prometheus/prometheus.yml
```
y tenemos que pegar lo siguiente:

```
global:
 scrape_interval: 15s

scrape_configs:
 - job_name: "prometheus"
   scrape_interval: 5s
   static_configs:
   - targets: ['localhost:9090']
```

#### Cambiar el propietario del archivo de configuración prometheus.yml a prometheus:

```
chown prometheus:prometheus /etc/prometheus/prometheus.yml
```

### Crear el servicio Prometheus

```
nano /etc/systemd/system/prometheus.service
```
y pegamos lo siguiente

```
[Unit]
Description=Prometheus
Wants=network-online.target
After=network-online.target

[Service]
User=prometheus
Group=prometheus
Type=simple
ExecStart=/usr/local/bin/prometheus \
--config.file /etc/prometheus/prometheus.yml \
--storage.tsdb.path /var/lib/prometheus/ \
--web.console.templates=/etc/prometheus/consoles \
--web.console.libraries=/etc/prometheus/console_libraries

[Install]
WantedBy=multi-user.target
```

#### Arrancar y habilitar el servicio de Prometheus

```
systemctl daemon-reload
systemctl start prometheus
systemctl status prometheus
systemctl enable prometheus
````

# Instalar NODE EXPORTER

![2f21780a8e4946a855e026ddd6576856](https://github.com/Scosrom/monitorizacion/assets/114906778/a14b6b2c-76b1-410a-a6f6-1d7f21f682aa)


### Crear usuario node exporter

```
sudo useradd --no-create-home --shell /bin/false node_exporter
```
 

### Descargar node exporter

```
curl -LO https://github.com/prometheus/node_exporter/releases/download/v1.1.2/node_exporter-1.1.2.linux-amd64.tar.gz
```
 

 

### Descomprimir y copiar binario

```
tar xvf node_exporter-1.1.2.linux-amd64.tar.gz
sudo cp node_exporter-1.1.2.linux-amd64/node_exporter /usr/local/bin
sudo chown node_exporter:node_exporter /usr/local/bin/node_exporter
rm -rf node_exporter-1.1.2.linux-amd64.tar.gz node_exporter-1.1.2.linux-amd64
```

 

### Crear servicio node exporter

```
nano /etc/systemd/system/node_exporter.service
```
 
```
[Unit]

Description=Node Exporter
Wants=network-online.target
After=network-online.target

[Service]

User=node_exporter
Group=node_exporter
Type=simple
ExecStart=/usr/local/bin/node_exporter

 [Install]

WantedBy=multi-user.target
```
  

### Arrancar/Habilitar servicio node exporter

```
sudo systemctl daemon-reload
sudo systemctl start node_exporter
sudo systemctl status node_exporter
sudo systemctl enable node_exporter
```

* localhost:9100/metrics

## Configurar Prometheus con los Exporters

### Editar configuracion de Prometheus

```
sudo nano /etc/prometheus/prometheus.yml
```
```
- job_name: 'node_exporter'
  scrape_interval: 5s
  scrape_timeout: 4s
  static_configs:
    - targets: ['192.168.1.166:9100']
```
 

### Reiniciar servicio prometheus

```
sudo systemctl restart prometheus
sudo systemctl status prometheus
```

* Podemos configurar cualquier exporters de esta forma.

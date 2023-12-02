# Grafana
![image](https://github.com/Scosrom/monitorizacion/assets/114906778/6d80a7e9-8d12-42b7-a598-08aa943f141d)

## Instalar Grafana

### Instalar las dependencias de Grafana:

```
 sudo apt install -y apt-transport-https
 sudo apt install -y software-properties-common wget
```

 

### Instalar repositorio de Grafana:

```
wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -

sudo add-apt-repository "deb https://packages.grafana.com/oss/deb stable main"

sudo apt update
```



### Instalar Grafana:

```
sudo apt install grafana
```
 

### Iniciar/Habilitar servicio Grafana:

```
sudo systemctl daemon-reload
sudo systemctl enable grafana-server
sudo systemctl start grafana-server
sudo systemctl status grafana-server
```


* El usuario y contraseña por defecto de grafana es admin/admin.


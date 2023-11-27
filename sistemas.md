# 2. Sistemas de monitorización

![sistemas](/img/Prometeus-VS-nagios-VS-pandora.png)
## 2.1 Nagios

Nagios es una herramienta de monitorización de código abierto que supervisa hosts y servicios en una red. Ofrece alertas y notificaciones en tiempo real.

```
define host {
    use     linux-server
    host_name   example-host
    alias       Example Host
    address     192.168.1.1
}

```
## 2.2 Prometheus

Prometheus es una plataforma de monitorización y alerta diseñada para ambientes dinámicos. Se basa en la recopilación de métricas y consultas en lenguaje PromQL.

```
rate(http_requests_total{job="api"}[5m])

```
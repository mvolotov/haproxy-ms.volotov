# rebrain_haproxy
Финальное задание по haproxy

В рамках задания было настроено два haproxy сервера, маршрутизирующие трафик в docker контейнеры.
Настроен кластерный IP адрес с помощью keepalived. 

Prometheus и grafana установлены на master ноде. NodeExporter и Haproxy Exporter, установлены на каждой из нод.
Prometheus забирает статистику с Master ноды (localhost) и Backup ноды (89.169.138.53). Так было сделано, чтобы в графане разделить статистику по haproxy, вместо того, чтобы опрашивать активную ноду, по кластерному IP адресу.

### Скриншоты из дашборда Haproxy в grafana
![Master нода haproxy](/grafana_screenshot/Haproxy_master.PNG?raw=true "Master нода")
![Backup нода haproxy](/grafana_screenshot/Haproxy_backup.PNG?raw=true "Backup нода")
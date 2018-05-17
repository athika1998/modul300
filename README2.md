
Modul 300 - Docker DE
=============================

Definition Docker
------------------
Docker ist eine Virtualiserung ohne Virtualisierung. Docker ist eine Container Technologie. Ein Container fasst eine einzelne Anwendung mitsamt aller Abhängigkeiten wie Bibliotheken, Hilfsprogrammen und statischer Daten in einer Image-Datei zusammen, ohne aber ein komplettes Betriebssystem zu beinhalten. Daher lassen sich Container mit einer leichtgewichtigen Virtualisierung vergleichen.

### Installation Docker
#### Aufsetzen repository
Führe die folgende Schritte aus, um Docker zu installieren:
1. Apt Package Index updaten:
```sh
sudo apt-get update
```
2. Installiere die Pakete, welche erlauben Repositorys über HTTPS zu verwenden:
```sh
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common
```
3. Füge Docker's offizieller GPG Key hinzu:
```sh
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```
Überprüfe, ob du den Key  mit dem Fingerprint 9DC8 5822 9FC7 DD38 854A E2D8 8D81 803C 0EBF CD88 hast
```sh
sudo apt-key fingerprint 0EBFCD88

pub   4096R/0EBFCD88 2017-02-22
      Key fingerprint = 9DC8 5822 9FC7 DD38 854A  E2D8 8D81 803C 0EBF CD88
uid                  Docker Release (CE deb) <docker@docker.com>
sub   4096R/F273FCD8 2017-02-22
```
4. Erstelle ein Repository mit:
```sh
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```
#### Installation Docker
1. Installiere Docker wie folgt:
```sh
sudo apt-get update
sudo apt-get install docker-ce
```
2. Überprüfe die Docker Installation mit:
```sh
sudo docker run hello-world
```

### Dockerfile und Start Container
1. Erstelle das Dockerfile im Verzeichnis
2. Erstelle ein Image mit dem Dockerfile, starte und überprüfe es
```sh
docker build -t apache2

docker run --rm -d --name apache2 apache2

docker exec -t mysql bash
```
3. Zeige den aktiven Container an
```sh
docker ps
```
## Webserver Testen
Es gibt zwei Arten, um zu schauen ob der Dienst läuft:
```sh
docker-machine ip default

curl http://192.168.99.100:8080
```
oder über einem Browser:
IP:8080

## Firewall Regeln nachschauen
```sh
docker-machine ip default

curl http://192.168.99.100:8080
```
## Monitoring
Über CMD:
```sh
docker stats
```
Mit Cadvisor:
```sh
docker run -d --name cadvisor -v /:/rootfs:ro -v /var/run:/var/run:rw -v /sys:/sys:ro -v /var/lib/docker/:/var/lib/docker:ro -p 8080:8080 webserver/cadvisor
```
### Docker User erstellen
Erstelle ein User mit dem folgendem Befehl:
```sh
RUN groupadd -r User_Group && useradd -r -g User_group xyz
```
Mit diesem Befehl loggt man sich ein:
```sh
RUN groupadd -r User_Group && useradd -r -g User_group xyz
```





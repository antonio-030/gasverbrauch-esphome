<h1 align="center">Hi 👋, Ich bin Antonio-030</h1>
<h3 align="center">"Vereinfachen Sie Ihre Smart Home-Automatisierung mit Home-Assistant und ESPHome"</h3>

<p align="left"> <img src="https://komarev.com/ghpvc/?username=antonio-030&label=Profile%20views&color=0e75b6&style=flat" alt="antonio-030" /> </p>

- 📫 So erreichen Sie mich ctoni030@proton.me


<h3 align="left">Sprachen and Tools:</h3>
<p align="left"> <a href="https://developer.android.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/android/android-original-wordmark.svg" alt="android" width="40" height="40"/> </a> <a href="https://www.arduino.cc/" target="_blank" rel="noreferrer"> <img src="https://cdn.worldvectorlogo.com/logos/arduino-1.svg" alt="arduino" width="40" height="40"/> </a> <a href="https://www.w3schools.com/cpp/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg" alt="cplusplus" width="40" height="40"/> </a> <a href="https://www.w3schools.com/css/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="css3" width="40" height="40"/> </a> <a href="https://dart.dev" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/dartlang/dartlang-icon.svg" alt="dart" width="40" height="40"/> </a> <a href="https://www.djangoproject.com/" target="_blank" rel="noreferrer"> <img src="https://cdn.worldvectorlogo.com/logos/django.svg" alt="django" width="40" height="40"/> </a> <a href="https://www.docker.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original-wordmark.svg" alt="docker" width="40" height="40"/> </a> <a href="https://flutter.dev" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/flutterio/flutterio-icon.svg" alt="flutter" width="40" height="40"/> </a> <a href="https://grafana.com" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/grafana/grafana-icon.svg" alt="grafana" width="40" height="40"/> </a> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="40" height="40"/> </a> <a href="https://www.linux.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" alt="linux" width="40" height="40"/> </a> <a href="https://mariadb.org/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/mariadb/mariadb-icon.svg" alt="mariadb" width="40" height="40"/> </a> <a href="https://www.mysql.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="mysql" width="40" height="40"/> </a> <a href="https://www.nginx.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nginx/nginx-original.svg" alt="nginx" width="40" height="40"/> </a> <a href="https://nodejs.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" alt="nodejs" width="40" height="40"/> </a> <a href="https://www.photoshop.com/en" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/photoshop/photoshop-line.svg" alt="photoshop" width="40" height="40"/> </a> <a href="https://www.php.net" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/php/php-original.svg" alt="php" width="40" height="40"/> </a> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> <a href="https://redis.io" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/redis/redis-original-wordmark.svg" alt="redis" width="40" height="40"/> </a> </p>

# gaszähler-auslesen-esphome
Gasverbrauch in ESPHome und Home Assistant 

1. Besorge dir einen Reed-Kontakt-Sensor und einen WeMos D1 Mini ESP8266.

![Wemos-D1!](/bilder/wemos-d1-mini-esp8266.jpg)

![Wemos-D1!](/bilder/reed-kontakt.jpg)

2.Verbinde den Reed-Kontakt-Sensor mit dem WeMos D1 Mini ESP8266 nach dem Schaltplan. In der Regel sind die Anschlüsse `D1 mit GND`, zu verbinden.

![reedkontakt!](/bilder/reedkontakt_Steckplatine.jpg)

3. Installieren Sie [ESPHome](https://esphome.io/guides/getting_started_hassio.html) in Home-Assistant und fügen sie denn Code am Ende Ihrer YAML-Konfigurationsdateien hinzu.  

ESPHome ist eine Open-Source-Software, die es ermöglicht, ESP8266 und ESP32-basierte Geräte in Home-Assistant einzubinden. ESPHome bietet eine einfache Methode, um die Firmware auf diesen Geräten zu erstellen und zu konfigurieren und ermöglicht die Verwendung von YAML-Konfigurationsdateien, um die Einrichtung von Sensoren, Aktoren und automatischen Regeln zu vereinfachen. Mit ESPHome können Sie auch die MQTT-Protokoll, das OTA-Firmware-Update und die Integration von Home-Assistant integrieren.

4. Erstelle ein neues Gerät und wähle den WeMos D1 Mini ESP8266 als Gerät aus.

![esphome!](/bilder/esphome-newDevice.jpg)

![esphome!](/bilder/esphome-create.jpg)


5. Füge einen Reed-Kontakt-Sensor hinzu und konfiguriere ihn mit den richtigen Pins für die Verbindung zum WeMos D1 Mini ESP8266.

6. Kompiliere und flashe das Projekt auf den WeMos D1 Mini ESP8266.

7. Stelle sicher, dass der WeMos D1 Mini ESP8266 mit dem WLAN verbunden ist und in der ESPhome-App sichtbar ist.

8. Überprüfe die Echtzeitdaten unter LOGS und stelle sicher, dass der Reed-Kontakt-Sensor in ESPhome erfolgreich registriert wurde.


[def]: antonio-030/gasverbrauch-esphome/bilder/esphome-newDevice.jpg

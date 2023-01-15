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

3. Installieren Sie [ESPHome](https://esphome.io/guides/getting_started_hassio.html) in Home-Assistant.  

ESPHome ist eine Open-Source-Software, die es ermöglicht, ESP8266 und ESP32-basierte Geräte in Home-Assistant einzubinden. ESPHome bietet eine einfache Methode, um die Firmware auf diesen Geräten zu erstellen und zu konfigurieren und ermöglicht die Verwendung von YAML-Konfigurationsdateien, um die Einrichtung von Sensoren, Aktoren und automatischen Regeln zu vereinfachen. Mit ESPHome können Sie auch die MQTT-Protokoll, das OTA-Firmware-Update und die Integration von Home-Assistant integrieren.

4. Erstelle ein neues Gerät und wähle den ESP8266 als Gerät aus.

![esphome!](/bilder/esphome-newDevice.jpg)

![esphome!](/bilder/esphome-create.jpg)


5. Füge einen Reed-Kontakt-Sensor hinzu und konfiguriere ihn mit den richtigen Pins für die Verbindung zum WeMos D1 Mini ESP8266.

Fügen sie denn code am Ende Ihrer YAML-Konfigurationsdateien hinzu.  
```yaml
captive_portal:
globals:
  - id: total_pulses
    type: int
    restore_value: false
    initial_value: '0'  # hier kann der Gaszählerstand initialisiert werden
  
binary_sensor:
  - platform: gpio
    id: internal_pulse_counter
    pin:
      number: GPIO5
      mode: INPUT_PULLUP
    name: "Live-Impuls"
    filters:
      - delayed_on: 10ms
    on_press:
      then:
        - lambda: id(total_pulses) += 1;
        - output.turn_off: led  # optional: für eine LED, die den Gaszählerpuls visualisiert
    on_release:
      then:
        - output.turn_on: led  # optional: für eine LED, die den Gaszählerpuls visualisiert

sensor:
  - platform: template
    name: "Gasverbrauch"
    device_class: gas
    unit_of_measurement: "m³"
    state_class: "total_increasing"
    icon: "mdi:fire"
    accuracy_decimals: 2
    lambda: |-
      return id(total_pulses) * 0.01;
    
           
# Optional: Diese LED soll blinken, sobald ein Signal vom Gaszähler erkannt wird
output:
  - platform: gpio
    pin: GPIO0
    id: 'led'	
```  
Dieser Code besteht aus 3 Hauptteilen:

    Definition einer globalen Variable: Eine globale Variable mit dem Namen "total_pulses" wird definiert. Sie hat den Typ Integer und wird mit dem Wert 0 initialisiert. Sie wird nicht automatisch auf einen früheren Wert zurückgesetzt, wenn das System neu gestartet wird.

    Einrichtung eines Binärsensors: Ein Binärsensor wird auf dem GPIO-Pin 5 eingerichtet. Der Sensor überwacht den Pin auf Impulssignale. Wenn ein Impuls erkannt wird, wird die Variable "total_pulses" um 1 erhöht. Es wird auch eine optionale LED-Steuerung eingerichtet, die die LED ein- und ausschaltet, wenn ein Impuls erkannt wird, um diesen visuell darzustellen.

    Einrichtung eines Templatesensors: Ein Sensor wird eingerichtet, der die Variable "total_pulses" verwendet, um den Gesamtgasverbrauch in Kubikmetern zu berechnen. Der Sensor hat eine Klasse "total_increasing" und ein Icon "mdi:fire", die Berechnung wird mit 2 Nachkommastellen dargestellt und wird in der Home Assistant Benutzeroberfläche angezeigt.

    Der Template-Sensor hat einen Namen "Gasverbrauch", eine Klasse "gas", eine Einheit "m³" und eine Klasse "total_increasing", was bedeutet, dass der Wert des Sensors sich mit der Zeit erhöhen wird. Der Sensor hat auch ein Icon "mdi:fire", welches eine Feuer-Grafik darstellt und die Berechnung wird mit 2 Nachkommastellen dargestellt. Die Berechnung des Gasverbrauchs erfolgt durch die Verwendung der lambda-Funktion, die die Variable "total_pulses" multipliziert mit 0.01, was bedeutet, dass jeder Impuls, der erfasst wird, als 0.01 Kubikmeter Gasverbrauch interpretiert wird.

In der Zusammenfassung, der Code zählt die Impulse die von einem Gaszähler kommen und speichert diese in einer globalen Variable. Diese Variable wird dann verwendet um den Gasverbrauch in Kubikmetern zu berechnen und anzuzeigen. Es gibt auch eine optionale LED-Steuerung, die die LED ein- und ausschaltet, wenn ein Impuls erkannt wird, um diesen visuell darzustellen.

6. Kompiliere und flashe das Projekt auf den WeMos D1 Mini ESP8266.

7. Stelle sicher, dass der WeMos D1 Mini ESP8266 mit dem WLAN verbunden ist und in der ESPhome-App sichtbar ist.

8. Überprüfe die Echtzeitdaten unter LOGS und stelle sicher, dass der Reed-Kontakt-Sensor in ESPhome erfolgreich registriert wurde.

![esphome-logsGas!](/bilder/esphome-logsGas.jpg)


[def]: antonio-030/gasverbrauch-esphome/bilder/esphome-newDevice.jpg

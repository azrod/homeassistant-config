# Configuration Home Assistant 

[![Home Assistant Version](https://img.shields.io/badge/HomeAssistant%20Version-v0.105.4-green?style=for-the-badge)](https://github.com/home-assistant/home-assistant/releases/tag/0.105.4) [![Build Status](https://img.shields.io/endpoint.svg?url=https%3A%2F%2Factions-badge.atrox.dev%2Fazrod%2Fhomeassistant-config%2Fbadge%3Fref%3Dmaster&style=for-the-badge)](https://actions-badge.atrox.dev/azrod/homeassistant-config/goto?ref=master)


## Equipements
### Matériels
* [Orange pi plus 2e](http://www.orangepi.org/orangepiplus2e/) (x2)
* Raspberry Pi 1 (x1)

### Contrôleurs 
* Zigbee - [Zigate USB](https://zigate.fr/produit/zigate-ttl/)
* Zwave - [EVERSPRING SA413](https://www.espace-domotique.fr/fr/transmetteur/everspring-controleur-usb-z-wave-plus-everspring-sa413-1-1043.html)
* 433Mhz - [Rflink](http://www.rflink.nl/) et [DIY PCB](https://github.com/azrod/diy-rflink-pcb) 
* Infrarouge - [Xiaomi IR remote](https://fr.gearbest.com/smart-home/pp_229556.html)
* Bluetooth - [Clé Bluetooth]

### Eclairages 
* Tradfri Couleur 600lm<sup>Zigbee</sup> (x3) [Ikea](https://www.ikea.com/fr/fr/p/tradfri-ampoule-led-e27-600-lumen-sans-fil-a-variateur-dintensite-spectre-blanc-colore-opalin-00408612/)
* Tradfri Blanc 1000lm<sup>Zigbee</sup> (x3)  [Ikea](https://www.ikea.com/fr/fr/p/tradfri-ampoule-led-e27-1000-lumen-sans-fil-a-variateur-dintensite-spectre-blanc-opalin-60408483/)
* [Sonoff Basic R2](https://sonoff.tech/product/wifi-diy-smart-switches/basicr2) avec [Esphome](https://esphome.io/)<sup>[WiFi]</sup>
* [Fibaro Dimmer 2](https://www.fibaro.com/fr/products/dimmer-2/) pour piloter un interrupteur mural<sup>[ZWave]</sup>
* [Qubino Flush Dimmer](https://qubino.com/products/flush-dimmer/) pour piloter un interrupteur mural<sup>[Zwave]</sup>
* [StripLed RGBW](https://www.amazon.fr/gp/product/B07BNKHRCF?pf_rd_p=3369e5a6-6989-43dc-ad01-b2b5ee1dcd12&pf_rd_r=28ZA91ZJ6R9EH1S5PVSF) Bande LED RGBW <sup>[WiFi]</sup> - Flashé sur ESPHOME [DIY](https://everythingsmarthome.co.uk/howto/diy-philips-hue-led-strips-installing-esphome-on-magic-home-rgbw-controllers/)

### Télécommandes 
* [Xiaomi Mijia Switch](https://fr.aliexpress.com/item/32825685057.html) <sup>[Zigbee]</sup> (x2)
* [Télécommande Sonoff 433](https://sonoff.tech/product/accessories/rm433) <sup>[433Mhz]</sup>

### Alarme 
* [Securitas Direct] - Utilisation d'un [custom component](https://github.com/segalion/securitasdirect) qui s'appuie sur l'API mobile de MyVerisure 

### Capteurs
#### Ouvertures
* [Xiaomi mijia Door sensor](https://fr.aliexpress.com/item/32829391822.html) <sup>[Zigbee]</sup> (x2)

#### Température / Humidité / Pression
* [Xiaomi mijia sensor](https://fr.aliexpress.com/item/32714410866.html) <sup>[Zigbee]</sup> (x8) - Capteur Température et humidité
* [Xiaomi aqara sensor](https://fr.aliexpress.com/item/32714410866.html) <sup>[Zigbee]</sup> (x1) - Capteur Température, humidité et pression
* Oregon Scientific <sup>[433Mhz]</sup> - Capteur Température, humidité avec une plage de fonctionnement important (congélateur)
* [DIY Station météo](https://www.instructables.com/id/Solar-Powered-WiFi-Weather-Station-V20/)<sup>[Wifi]</sup> - Portage de la partie logiciel sur Esphome

#### Présences
* [Xiaomi mijia IR sensor](https://fr.aliexpress.com/item/32828696729.html) <sup>[Zigbee]</sup> (x4)

#### Fuites 
* [Xiaomi Aqara weather](https://fr.gearbest.com/smart-home/pp_229556.html) <sup>[Zigbee]</sup> (x2)

### Prises connectées 
* [Sonoff Basic R2](https://sonoff.tech/product/wifi-diy-smart-switches/basicr2) avec [Esphome](https://esphome.io/) <sup>[WiFi]</sup>
* [Sonof R20](https://sonoff.tech/product/wifi-smart-plugs/s20) avec [Esphome](https://esphome.io/) <sup>[WiFi]</sup>

### Aspirateur 
* [Xiaomi Mi Robot Vaccum S50](https://fr.aliexpress.com/item/32850707934.html) <sup>[WiFi]</sup>

### TeleInfo 
* [WirelessTeleInfo](https://github.com/Domochip/WirelessTeleInfo) <sup>[Wifi]</sup> DIY

## Tracking des avions - FlighRadar 

J'ai installé une antenne TV de type DVB-T pour pouvoir suivre l'activité aérienne civile au dessus de chez moi. ([Antenne - Amazon](https://www.amazon.fr/gp/product/B013Q94CT6/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&amp;psc=1&_encoding=UTF8&tag=azrod0d-21&linkCode=ur2&linkId=f952cf91e04350a5fe42c3dac0a421a0&camp=1642&creative=6746)). Afin de partager avec la communauté je transmet les informations au site [FlightRadar](https://www.flightradar24.com/) qui permet d'avoir un compte premium sur le site. FlightRadar fournis un soft pour transmettre les données [FR24Feed](https://www.flightradar24.com/share-your-data) et s'appuie sur le soft dump1090 pour pouvoir lire et décoder les informations de l'antenne. Installé sur un RaspberryPI 1 c'est un bon moyen pour utiliser ce vieux RaspberryPI. 

Dump1090 fournis une page web avec des informations en Json pour récupérer les informations sur le tracking en temps réel. Voici l'intégration dans lovelace. 

![dump1090](mdimg/dump1090-lovelace.png)

Tous les fichiers de configuration pour HomeAssistant sont dsponible dans `packages/fr24.yaml`


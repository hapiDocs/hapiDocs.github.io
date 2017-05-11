## Overview
All modules (Smart or Dumb) have the capability to automatically detect and connect to one another without user configuration or intervention. To accomplish this, the HAPI platform uses a zero-configuration networking implementation called Avahi. Similar to Apple's Bonjour, Avahi allows modules to dynamically name themselves and discover neighboring modules.

## Technical Description
All modules in a HAPI implementation use Avahi. For Smart Modules, the original Raspian images are modified to include the avahi daemon. When a module boots, it automatically runs this daemon. When a Smart Module starts, to attempts to contact the MQTT broker, "mqttbroker.local". This machine is acts as the communications hub for all HAPI-based facilities. If the Smart Module's search for the MQTT broker is not successful, it changes it's own name to "mqttbroker.local" and becomes the communications hub for the site.

## Further Information
Wikipedia entry for [Avahi](https://en.wikipedia.org/wiki/Avahi_(software))


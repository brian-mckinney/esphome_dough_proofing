# ESPHome Based Dough Proofing Chamber

## Description
An automated dough proofing chamber, based on [ESPHome](https://esphome.io/) and integrated into [Home Assistant](https://www.home-assistant.io/).  This solution uses some 12v heating pads connected to an esp32 along with a DHT22 temperature sensor.  The heating pads will turn on and off depending on the temperature inside the chamber in order to maintain the target temperature (default 80°F).  The target temperature can be controlled independently from the home assistant app.

## Components
- ESP32 Microcontroller ( [Amazon](https://www.amazon.com/gp/product/B08SK2Z6KD) ) ( [AliExpress](https://www.aliexpress.us/item/3256806025765385.html) )
- ESP32 Breakout Board ( [Amazon](https://www.amazon.com/gp/product/B0BYS6THLF) )
- Heating Pads ( [Amazon](https://www.amazon.com/gp/product/B0CF5CSLC7) )
- PD Trigger Board ( [Amazon](https://www.amazon.com/gp/product/B0D14D8PQZ) ) ( [AliExpress](https://www.aliexpress.us/item/3256805992876765.html) )
- Buck Converter ( [Amazon](https://www.amazon.com/HiLetgo-Super-Converter-Module-Adjustable/dp/B00LODGDYE) ) ( [AliExpress](https://www.aliexpress.us/item/3256806038357827.html) )
- 5v Relay Module ( [Amazon](https://www.amazon.com/DIYables-Arduino-ESP8266-Raspberry-Channel/dp/B0B1ZHXXXD) ) ( [AliExpress](https://www.aliexpress.us/item/3256806923028324.html) )
- Insulated Cooler Bag ( [Sam's Club](https://www.samsclub.com/p/mm-insulated-shopper/prod21450107) ) ( [Amazon](https://www.amazon.com/CIVJET-Insulated-Reusable-Shopping-Delivery/dp/B0C5Q9RJM8) )

## Assembly
The project started with an insulated cooler bag bought from Sam's Club.  The heating pads are attached at various points to the inside of the bag and the wires are held in place with heat resistant tape.  There is an outside pocket on this particular bag, so I ran the cables through the wall (cut a small hole with a hobby knife) and situated the controller in the side pocket.

### Inside view
<img src="https://github.com/user-attachments/assets/e8bea11b-7934-4c0c-a2e9-93617edf86f8" alt="alt text" width="300" height="400">

### Controller
The core of the controller is an ESP32 microcontroller.  The heating pads are connected to a relay module, which is controlled by the esp32 to turn the heating pads on or off.
Since the heating pads are 12v and the esp32 requires 5v, I went with a usbc PD power solution.  The PD trigger board provides 12v power, which is split between the heating pads (using a relay module for control) and buck converter which changes the voltage to 5v to power the esp32 and the relay. <br><br>
<img src="https://github.com/user-attachments/assets/42f73760-2885-48af-bd7f-504a67a03315" alt="alt text" width="400" height="400">

## Home Assistant
TODO

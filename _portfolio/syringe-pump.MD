---
title: "DIY Syringe Pump"
excerpt: "A DIY syringe pump fit for 10-20 mL syringes with flow rate capability from 1 uL/min to 10 mL/min."
header:
  image: /assets/img/pump-cad.png
  teaser: /assets/img/syringe-pump.png
gallery:
  - image_path: assets/img/pump-cad.png
  - image_path: assets/img/pump-wiring.png
  - image_path: assets/img/syringe-pump.png
   
---

# Features

* **Syringe Compatibility**: Using a novel V-shaped cutout, syringes sized between 10-20 mL are able to slide in comfortably.
* **Large Range of Flow Rates**: This syringe pump uses microstepping capabilities to be able to pump liquid at flow rates as low as 1 uL/min and as high as 10 mL/min!
* **LED Indicator & Automatic Stopping**: An LED light sits outaside of the casing to indicate if the pump is on and running, paused, or out of liquid. When the syringe runs out of liqud, the motor will automatically stop due to the momentary switch button that in integrated into the pump system.

## Instructions for Use
1. Ensure that the power supply is connected to the syringe pump. The LED light should be blue.
2. Place the syringe in the supports with the tip that outputs liquid at the far right end.
3. Adjust the flow rate in the Arduino code at line 18.
4. Input the size of syringe into the Arduino code at line 19.
5. To begin dispensing liquid from the syringe, press the red power button to be lowered. This is placed at the bottom left of the front panel of the enclosure. The LED light should be green during liquid dispense.
6. To pause the liquid dispense, press the power button again so it is raised. The LED light should show blue.
7. To continue dispensing the liquid, press the power button again so it stays lowered.
8. Once all liquid possible has been dispensed, the LED will turn red and the actuation will stop.


| Off-the Shelf Parts                | Quantity |
|------------------------------------|----------|
| F688-2RS Flanged Ball Bearing      | 2        |
| TR 8x8x250 mm Lead Screw           | 1        |
| TR 8x250 mm Linear Rod             | 1        |
| LM8UU Linear Bearing               | 1        |
| 8 mm Lead Screw Lock Collar        | 2        |
| M4-0.7 x 3 mm                      | 2        |
| 8 mm Linear Rod Clamp              | 2        |
| M3-0.5 x 8 mm                      | 2        |
| M3-0.5 x 6 mm                      | 4        |
| M3-0.5 x 10 mm                     | 4        |
| M5-0.8 x 8 mm                      | 6        |
| M5 T-Nut                           | 6        |
| 5mm to 8mm Coupler                 | 1        |
| NEMA 17 Stepper Motor              | 1        |
| 20 x 40 x 300 mm Aluminum Extrusion| 1        |
| TR 8x8 Lead Screw Nut              | 1        |
| LED Light                          | 1        |
| Arduino Microcontroller            | 1        |
| Breadboard                         | 1        |
| 12V/24V Power Supply               | 1        |
| Latching Button                    | 1        |
| Momentary Switch Button            | 6        |



| CAD Modeled Parts                     | Quantity |
|---------------------------------------|----------|
| Motor Mounting Plate                  | 2        |
| Carriage                              | 1        |
| Motor Mounting Plate w/ Flange Cutouts| 1        |
| Motor Mounting Plate w/ Hub Setting   | 1        |
| Housing                               | 1        |
| Labeled Front Plate                   | 1        |


# Arduino Code
[Syringe Pump Arduino Code - PDF](https://github.com/alice-heiden/alice-heiden.github.io/assets/img/pump-arduino-code.pdf)


# CAD Model
<iframe src="https://myhub.autodesk360.com/ue2df0af5/shares/public/SH35dfcQT936092f0e437224cd558fdcdc2f?mode=embed" width="800" height="600" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

{% include gallery caption="DIY Syringe Pump Gallery" %}

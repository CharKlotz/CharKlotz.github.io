---
title: Module's Selected Major Components
---

## Module's Selected Major Components

The following sections are the selected major components necessary for the human interfacing function for our team's rover. 

### Power Management

* LM2575 - 3.3 volt switching regulator provided in class

[link to product](https://www.digikey.com/en/products/detail/evvo/LM2575S-3-3-EV/24370070)


### No Sensor
### No Actuator
### Screen
OLED Provided in class is perfect for the final project as an SMD part is not required for the screen.

[link to similar product](https://www.digikey.com/en/products/detail/winstar-display/WEA012864DWPP3N00003/20533255)

With all that, the only thing needed to be chosen for my subsystem ended up being the buttons (Other than capacitors and diodes, which I pretty much picked the first smallish SMD part I saw on Amazon since I forgot them in my original purchase sheet.)

-----------
## Buttons
*Table 1: Button component selection*

| **Component**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](pushbuttonFinal.jpg)<br> Small push button from amazon<br>$0.22/each<br>[link to product](https://www.amazon.com/dp/B07HCF49KC?ref=ppx_yo2ov_dt_b_fed_asin_title)                 | \* TBD<br>\* TBD<br>\* TBD                                               | \* TBD<br>\* TBD. | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](pushbuttonchoice1.jpg)<br> XC1259TR-ND surface mount crystal<br>$1/each<br>[link to product](http://www.digikey.com/product-detail/en/ECS-40.3-S-5PX-TR/XC1259TR-ND/827366)                 | \* Inexpensive[^1]<br>\* Compatible with PSoC<br>\* Meets surface mount constraint of project                                               | \* Requires external components and support circuitry for interface<br>\* Needs special PCB layout. | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](pushbuttonchoice2.jpg)<br> XC1259TR-ND surface mount crystal<br>$1/each<br>[link to product](http://www.digikey.com/product-detail/en/ECS-40.3-S-5PX-TR/XC1259TR-ND/827366)                 | \* Inexpensive[^1]<br>\* Compatible with PSoC<br>\* Meets surface mount constraint of project                                               | \* Requires external components and support circuitry for interface<br>\* Needs special PCB layout. |

**Rationale:** A clock oscillator is easier ....

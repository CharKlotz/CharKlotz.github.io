---
title: Component Selection Example
---

*Table 1: Light Sensor Selection*

**Light Sensor Module**

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](image1.png)<br>Option 1.<br> 1528-161-ND Photoresistor<br>$0.95/each<br>[link to product](https://www.digikey.com/en/products/detail/adafruit-industries-llc/161/7244927)                 | \* Inexpensive<br>\* Simple<br>                                               | \* Slow Response<br>\* Output is nonlinear |
| ![](image2.png)<br>\* Option 2. <br>\* 475-BPW34-ND Photodiode <br>\* $1.14/each <br>\* [Link to product](https://www.digikey.com/en/products/detail/ams-osram-usa-inc/BPW34/607274) | \* Fast Output <br>\* Linear Output <br> \* Low Cost | * Slight temperature drift <br>\* Slow shipping speed                                                         |
| ![](image3.png)<br>\* Option 3. <br>\* 365-1918-ND Phototransistor <br>\* $1.76/each <br>\* [Link to product](https://www.digikey.com/en/products/detail/tt-electronics-optek-technology/OPB200/1636789) | \* Simple interface <br>\* High default output gain <br> | * More expensive <br>\* Slow response time                                                         |

**Choice:** Option 2: 475-BPW34-ND Photodiode

**Decision Making Process:** A photodiode is preferred because it provides a linear and accurate response to light. It will require an external amplifier circuit, but its predictable behavior will make it more reliable than other options for our use case. This sensor will make it easy to take ambient light readings of the room to be pushed out to the individual lighting subsystem, to help fulfill our project needs.

**Other Components:** The rest of the components used will be the ones provided already in class, such as the LM7805 Voltage Regulator or MCP6004 OP-Amp.
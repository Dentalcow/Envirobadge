30/11/2025 - Brainstorming and Component Sourcing - 4:30pm to 6:30pm - 2 Hours
Brainstormed the basic idea and shopped around for the E-ink display I could base the project around. 

E-ink display choice 1:
https://www.aliexpress.com/item/1005006291142235.html
https://github.com/WeActStudio/WeActStudio.EpaperModule

E-ink display choice 2:
https://www.waveshare.com/1.54inch-e-paper-g.htm?sku=30475
https://www.waveshare.com/wiki/1.54inch_e-Paper_Module_(G)

Choice 1 offers a cheaper aliexpress price point, but choice 2 from waveshare is better documented and has black, white, yellow and red coloured pixels.

The next step was to decide the sensor suite for my enviromental tracker. To start, I needed to find a Temperature-Humidity-Pressure combo sensor.

After a bit of searching, I decided on the BME688 from Bosch, which can do Temperature, Humidity, Pressure and basic "AI" gas detection. 

https://jlcpcb.com/partdetail/BoschSensortec-BME688/C3664478

For the co2 sensing, I decided to go with the SCD40-D-R2 mostly because of its availablility on JLC's website.

https://jlcpcb.com/partdetail/Sensirion-SCD40_DR2/C3659421

I decided at this point that I wanted to include a small microphone for basic noise level sensing.

https://jlcpcb.com/partdetail/TDKInvenSense-ICS43434/C5656610

The final part I needed to fully decide on before starting to create a rough schematic was the microcontroller. I ended up choosing the Seeed XIAO ESP32-C3 as it is small, energy efficient, has plenty of IO and would allow me to use BLE to download data off it. 

30/11/2025 - Schematic Mockup - 6:45pm to 

After collecting footprints and files for all the currently selected parts, I began to connect parts together. It was at this point that I ran into my first issue, the microphone outputs an i2s stream which isn't supported by the C3 microcontroller. This led to the decision of switching to an analogue microphone.

https://jlcpcb.com/partdetail/TDKInvenSense-INMP404ACEZR7/C3171789

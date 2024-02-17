# Door_Security_System
Door security system made with an Arduino Uno. More Information in README.


Arduino Uno, RFID sensor, Jumper wires (male to male, female to male), two RFID cards, buzzer, resistors(10KOhm, 220 Ohm), RGB 5mm Diffused LED, button, LCD Display Module 1602 16x02 IIC/I2C, Breadboad (optional for prototype).

RFID sensor and cards - https://www.amazon.com/HiLetgo-3pcs-RFID-Kit-Raspberry/dp/B07VLDSYRW/ref=sr_1_3?dib=eyJ2IjoiMSJ9.qeu57IuNLc58iF6P02Z6jrXFirYQrJxdbEJkPZ07hQdLCkCiRf5lDkao8ZYlS9Y-sl5I8NuiOkV_ERw33fD9KUSFTX0jfEF3BQwt3L456lvS8rTYOtT_j4PJnyXKXkbNDQ3GE_2I3_7dgS1jagGaWsLOKfO36AETxxSDo-MGOZmx28gMGt02WU2C0Y8Cie76S6Q7DIxYiwee-t81gCRa2_rQSJfKq-3iFlcrJtl7xYs.fFxtkF7EC_ygDjckZtwEA5q7NkgWds-nYqRuBUjpuTY&dib_tag=se&keywords=RFID+Sensor&qid=1708169729&sr=8-3

Jumper wires - https://www.amazon.com/Elegoo-EL-CP-004-Multicolored-Breadboard-arduino/dp/B01EV70C78/ref=sr_1_3?dib=eyJ2IjoiMSJ9.hN9xWohZ0eiut9PloEXT2-Muw3wl-m-QeSlHHYd8tRg2ODJgq-9QGkBqnm0cHh-EPz6fefgKjQX1P5gmulLXlAFxPUhYrqRttkCRt2QcDKyAoeiT8mWC_-nk9c0lAPqycwcfltZ_tiCjCDgmxODs8t7yC2mT2z0p5QpmF7x_-DB7mWHVvuD_TYW5ed3NAMKff62Qays0-xcEDaVvwehVTDepUh-z6Gl97MvD5oL1b9A.xiaGksLxRe4bViZDzcXWCblvEm_blQ12Tzv-EaAx-gY&dib_tag=se&keywords=jumper+wires&qid=1708170204&sr=8-3

LCD display - https://www.amazon.com/SunFounder-Serial-Module-Display-Arduino/dp/B019K5X53O/ref=sr_1_4?crid=2OK7ZWO1XFL7P&dib=eyJ2IjoiMSJ9.MWRYL3aywzp39AgcJj10H6el9PfAEy2oqV7t83r-XdBHxeJcNOwwtVMOyz3Lv_CRXwCO0C07A0nIWKL_GpLMbtnBydzxntkcET8VXu6mc2vqtOsabApTP3LrONeBX0lDeofTZQTcOXjFFwotR7Ip-wsRX-vwywddo9I0JodGotrJEvtNQU__DaNf_sIXPobOyGkZUyzFGcS1dfrJNNvu-i6qnIxMxtdXVr7qpc8FELdxcwCnCqrWrVSMhGl0rvXD1dDDSHFdfzVLSTw_oc9GWN3c21eVY2Xz7jYSQ4qb9p8._OjXyK1EkWw_i6nFtWSAndx5QvDp-sPTEIo0pUbpj5A&dib_tag=se&keywords=LCD+Display+Module+1602+16x02+IIC%2FI2C&qid=1708170258&sprefix=lcd+display+module+1602+16x02+iic%2Fi2c%2Caps%2C190&sr=8-4

RGB LED - https://www.amazon.com/EDGELEC-Tri-Color-Multicolor-Diffused-Resistors/dp/B077XGF3YR/ref=sr_1_4?crid=2ZOGDK1EUAZQA&dib=eyJ2IjoiMSJ9.cj1Rrn3LpZbidJPVqHeDUeM4LT_0dOHSgVvngtK4uSU9zVUJzksPPMYeqO8WziS5ubZ5zVaXMCGqk3VOa3_zkXAQhQkVBXM3tlsLAqGRBff4ErqVLSpIcGZxSmUq-upxYmJmbRF1FzoQtWkqYSjbVYR9itbawCt-SYgsOTRxgKhvtjF3-9kRx8VR886CIiHJNquwyT3JCvn5erAHRLTnK_191SAzCn5KssVa6zICNn8.IsteXs11NuTocydKp54bNu04kThgTGsckxb7_-eW_bA&dib_tag=se&keywords=RGB+5mm+Diffused+LED&qid=1708170296&sprefix=rgb+5mm+diffused+led%2Caps%2C229&sr=8-4

Needed libraries for the code:
SPI.h - https://github.com/PaulStoffregen/SPI/blob/master/SPI.h
MFRC522.h - https://github.com/miguelbalboa/rfid
LiquidCrystal_I2C.h - https://github.com/fdebrabander/Arduino-LiquidCrystal-I2C-library

Instructions:
Use 10KOhm for the button and 3 220Ohm for the LED.
1. Soldier I2C module to the display and connect the module to Arduino. If the backlight on the display doesn't lit up check the solder joints.
2. Connect the LED pins to the corresponding pins: red - 2; green - 3; blue - 4.
3. Connect the button with the 10KOhm resistor to the 5 pin.
4. Connect the buzzer to the 7 pin.
5. Connect the RFID sensor. SS - 10 pin, RST - 9 pin.

   IMPORTANT:
   Make sure that you set the String MasterTag to the card that is by default the correct one. You can do this by scanning your card. It will show you the card tag in the Serial monitor. Set your card tag to the String MasterTag.

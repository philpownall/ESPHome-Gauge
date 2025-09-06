# ESPHome-Gauge
A Gauge using an ESP32-C3 with attached color display

### Ingredients
- The Spotpear desktop trinket from [Spotpear](https://spotpear.com/shop/ESP32-C3-desktop-trinket-Mini-TV-Portable-Pendant-LVGL-1.44inch-LCD-ST7735.html)

The attached 1.44inch 128x128 TFT color LCD screen is driven by an ST7735S with a white LED backlight

[GAUGE](Gauge.png)

The Gauge uses LVGL to show a Home Assistant temperature sensor on the attached display

The display uses the following pins - dc_pin: GPIO0, cs_pin: GPIO02, reset_pin: GPIO05 
The display is driven by a ST7735 SPI chip which uses the following ESP32C3 pins: clk_pin: GPIO03, mosi_pin: GPIO04, the miso_pin is NC
The display backlight cannot be controlled: use it.fill(COLOR_OFF) or the equivalent LVGL command

There are 4 physical buttons: Boot (GPIO9) (ESP32C3 pin 15) and reset (ESP32C3 pin 7: Reset), key1 (ESP32C3 GPIO8) and key2 (ESP32C3 GPIO10)
The Boot pin is usable after boot is completed.  Key1 and Key2 are user programmable.
ESP32C3 pin GPIO11 is connected to a controllable red LED

The desktop trinket has a small battery power connector on the bottom side, but it is not very useful as the device has no power button,
and the display backlight cannot be turned off.

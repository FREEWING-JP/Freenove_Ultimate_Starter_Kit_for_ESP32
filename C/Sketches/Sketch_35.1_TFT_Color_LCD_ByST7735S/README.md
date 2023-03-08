## SPI TFT Color LCD ST7735S on Freenove ESP32-WROVER CAM board

* YouTube demo  
[<img src="https://img.youtube.com/vi/1S3dxJ9Wgxw/maxresdefault.jpg" alt="ESP32 SPI IPS Color LCD ST7735S tutorial" title="ESP32 SPI IPS Color LCD ST7735S tutorial" width="320" height="180"> YouTube https://youtu.be/1S3dxJ9Wgxw](https://youtu.be/1S3dxJ9Wgxw)

* Hardware  
[Freenove ESP32-WROVER CAM board](https://www.amazon.co.jp/dp/B09BC1N9LL/ref=nosim?tag=freewing-22)  
[0.96 inch TFT Display IPS LCD ST7735S 3.3V 160x80 SPI Interface](https://www.amazon.co.jp/dp/B07S728JV4/ref=nosim?tag=freewing-22)  
  
* Base Source Code  
[moononournation / Arduino_GFX](https://github.com/moononournation/Arduino_GFX)  
examples/HelloWorld/HelloWorld.ino  
  
* Wiring  
```
//  LCD - ESP32  
//  GND - GND  
//  VCC - +3.3V  
//  SCL - GPIO 13  
//  SDA - GPIO 14  
//  RES - GPIO 0  
//  DC  - GPIO 12  
//  CS  - GPIO 15  
//  BLK/LED - GPIO 2  
```
```
#define GFX_BL 2

Arduino_DataBus *bus = new Arduino_ESP32SPI(
  12 /* DC */, 
  15 /* CS */,
  13 /* SCK */,
  14 /* MOSI */,
  GFX_NOT_DEFINED /* MISO */,
  VSPI /* spi_num */);

Arduino_GFX *gfx = new Arduino_ST7735(
  bus,
  0 /* RST */,
  3 /* rotation */,
  true /* IPS */,
  80 /* width */, 160 /* height */,
  26 /* col offset 1 */, 1 /* row offset 1 */,
  26 /* col offset 2 */, 1 /* row offset 2 */);
```

* Breadboard Wiring  
![Sketch_35.1_TFT_Color_LCD_ByST7735S.png](https://user-images.githubusercontent.com/16265606/223708544-2b4e0578-f5d9-4a69-a7a9-3fdd731d2eaa.png)

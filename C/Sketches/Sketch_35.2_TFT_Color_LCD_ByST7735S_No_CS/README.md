## SPI TFT Color LCD ST7735S on Freenove ESP32-WROVER CAM board

* YouTube demo  
[<img src="https://img.youtube.com/vi/1S3dxJ9Wgxw/maxresdefault.jpg" alt="ESP32 SPI IPS Color LCD ST7735S tutorial" title="ESP32 SPI IPS Color LCD ST7735S tutorial" width="320" height="180"> YouTube https://youtu.be/1S3dxJ9Wgxw](https://youtu.be/1S3dxJ9Wgxw)

* Hardware  
[Freenove ESP32-WROVER CAM board](https://www.amazon.co.jp/dp/B09BC1N9LL/ref=nosim?tag=freewing-22)  
[0.96 inch TFT Display IPS LCD ST7735S 3.3V 160x80 SPI Interface](https://www.amazon.co.jp/dp/B07S728JV4/ref=nosim?tag=freewing-22)  
  
* Base Source Code  
[moononournation / Arduino_GFX](https://github.com/moononournation/Arduino_GFX)  
examples/HelloWorld/HelloWorld.ino  
  
## No /CS control version

CS tied to GND for Reduce GPIO pin  

* Wiring  
```
//  LCD - ESP32  
//  GND - GND  
//  VCC - +3.3V  
//  SCL - GPIO 13  
//  SDA - GPIO 14  
//  RES - GPIO 15  
//  DC  - GPIO 12  
//  CS  - GND  
//  BLK/LED - GPIO 2  
```
```
#define GFX_BL 2

Arduino_DataBus *bus = new Arduino_ESP32SPI(
  12 /* DC */, 
  GFX_NOT_DEFINED /* CS */,
  13 /* SCK */,
  14 /* MOSI */,
  GFX_NOT_DEFINED /* MISO */,
  VSPI /* spi_num */);

Arduino_GFX *gfx = new Arduino_ST7735(
  bus,
  15 /* RST */,
  3 /* rotation */,
  true /* IPS */,
  80 /* width */, 160 /* height */,
  26 /* col offset 1 */, 1 /* row offset 1 */,
  26 /* col offset 2 */, 1 /* row offset 2 */);
```

* Breadboard Wiring  
![Sketch_35.2_TFT_Color_LCD_ByST7735S_No_CS.png](https://user-images.githubusercontent.com/16265606/223712220-6b2e9cfc-9475-474f-bfb3-5a595d95989c.png)

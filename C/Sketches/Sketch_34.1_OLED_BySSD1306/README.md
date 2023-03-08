## I2C OLED SSD1306 on Freenove ESP32-WROVER CAM board

* YouTube demo  
[<img src="https://img.youtube.com/vi/H4BSCT6YwdI/maxresdefault.jpg" alt="ESP32 I2C OLED SSD1306 tutorial" title="ESP32 I2C OLED SSD1306 tutorial" width="320" height="180"> YouTube https://youtu.be/H4BSCT6YwdI](https://youtu.be/H4BSCT6YwdI)  

* Hardware  
[Freenove ESP32-WROVER CAM board Starter kit](https://www.amazon.co.jp/dp/B09BC1N9LL/ref=nosim?tag=freewing-22)  
[0.96 inch OLED Display SSD1306 3.3V 128x64 I2C Interface](https://www.amazon.co.jp/dp/B081ZQ5Z97/ref=nosim?tag=freewing-22)  
  
* Base Source Code  
[ThingPulse / esp8266-oled-ssd1306](https://github.com/ThingPulse/esp8266-oled-ssd1306)  
examples/SSD1306DrawingDemo/SSD1306DrawingDemo.ino  

* Wiring  
```
//  OLED - ESP32  
//  GND  - GND  
//  VCC  - +3.3V  
//  SCL  - GPIO 13  
//  SDA  - GPIO 14  
```
```
#define I2C_ADRS 0x3c
#define I2C_SCL 13
#define I2C_SDA 14

SSD1306Wire display(I2C_ADRS, I2C_SDA, I2C_SCL);
```

* Breadboard Wiring  
![Sketch_34.1_OLED_BySSD1306.png](https://user-images.githubusercontent.com/16265606/223709216-c1189012-0bbb-4b8e-80dd-95b276f5cae7.png)

# openmv-MJPEG-by-esp8266
shows off how to do MJPEG streaming for openmv by esp8266

1.程序功能：
使用esp8266给openmv增加图传功能

2.硬件要求：
openmv3或4
esp8266 (wemos D1 Mini,其它版本应该没问题，但这个版本的引脚与openmv连接更合适)

3.硬件连接：
   GPIO    NodeMCU   Name   |   openmv
   ===================================
 GPIO16       D0      SS    |   P3  (PB12) 
 GPIO13       D7      MOSI  |   P0  (PB15) 
 GPIO12       D6      MISO  |   P1  (PB14) 
 GPIO14       D5      SCK   |   P2  (PB13) 
 GPIO2        D4 指令信号(低触发)  (P7) 
   GND                          GND 22

4.使用：
  openmv与esp8266连接，openmv通过usb供电
  谷歌浏览器打开:
  http://192.168.1.41/capture 显示单张图片
  http://192.168.1.41/stream  显示图片流
  
5.实测效果：
  320*240 黑白 3KB  传图速度 0.1秒/张 
  640*480 黑白 17KB 传图速度 0.4秒/张 

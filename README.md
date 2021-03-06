# AZ-Touch-ESP-Video

This is an example how to use AZ-Touch MOD for ESP32 to show live pictures of an IP camera on the screen. This can be used for example for video surveillance, video door bells and similar applications. 

![My image](https://user-images.githubusercontent.com/3049858/105029941-56348500-5a53-11eb-8301-2ac0e21983a8.jpg)


[![Watch the video](https://i9.ytimg.com/vi/41QTn6MzIbA/mq2.jpg?sqp=CITAm4AG&rs=AOn4CLBQiqDSzxs3ZZmQxMmFEhXdGAX4Ow)](https://youtu.be//41QTn6MzIbA)


## Hardware 

I've used our AZ-Touch MOD kit for ESP32 as hardware plattform. This kit comes with a 2.4 or 2.8 inch tft touchscreen. The demo will work with both screen sizes, but of course it makes more sense to use the bigger 2.8 inch screen in this application.

![My image](https://cdn.shopify.com/s/files/1/1509/1638/products/2.Produkt_500x.jpg?v=1604667072)

You can find all information about the hardware here:
https://www.hwhardsoft.de/english/projects/arduitouch-esp/


## Camera

This example was written for the ESP32-CAM camera. 
![My image](https://user-images.githubusercontent.com/3049858/105034491-d8c04300-5a59-11eb-9577-a203aa188705.jpg)

Please install the CameraWebServer example on the ESP32-cam which comes with the Arduino IDE.
![My image](https://user-images.githubusercontent.com/3049858/105033964-1c667d00-5a59-11eb-9af5-de14a0812b04.jpg)

Please choose "ESP Wrover Module" as board and "Huge APP ..." as partition scheme:
![My image](https://user-images.githubusercontent.com/3049858/105033944-17093280-5a59-11eb-8acb-c223c089b0b0.jpg)


The software can be used with other IP cameras too if this cameras can provide a jpg picture via http in QVGA (320 x 240) or VGA (640 x 480) size. Probably some small changes especially in the host address configuration are needed in this case.


## Libraries

Install the following libraries through Arduino Library Manager

Arduino TFT_eSPI Library https://github.com/Bodmer/TFT_eSPI 

Arduino TJpg_Decoder library https://github.com/Bodmer/TJpg_Decoder

You can also download the library also directly as ZIP file and uncompress the folder under yourarduinosketchfolder/libraries/   

After installing the libraries, restart the Arduino IDE. 


## TFT_eSPI Setup

I've prepared a User setup files for the TFT_eSPI library especially for AZ-Touch and ESP32 

https://github.com/HWHardsoft/AZ-Touch-ESP_Video/blob/main/TFT_eSPI_Setup/User_Setup.h

Please replace the original User_Setup.h file in your ...\Arduino\libraries\TFT_eSPI\ folder


## Settings 

Open the file settings.h in the Arduino IDE and enter your WiFi SSID & password in the fields in the WiFi section: 

const char* ssid = "your ssid";
const char* password = "your password";

Furthermore you have to change the host ip address to the ip address of your camera.

const char* host = "192.168.178.40";


## Credits 

This example based on the awesome work of:

* Stefan Fambach    www.fambach.net
* Github user 0015  https://github.com/0015/IdeasNProjects




# License

This library is free software; you can redistribute it and/or
modify it under the terms of the GNU Lesser General Public
License as published by the Free Software Foundation; either
version 2.1 of the License, or (at your option) any later version.

This library is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
Lesser General Public License for more details.

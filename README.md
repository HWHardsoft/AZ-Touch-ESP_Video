# AZ-Touch-ESP-Video

This is an example how to use AZ-Touch MOD for ESP32 to show live pictures of an IP camera display on the screen. This can be used for example for  
video surveillance, video door bells and similar applications. 

![My image](https://user-images.githubusercontent.com/3049858/105029941-56348500-5a53-11eb-8301-2ac0e21983a8.jpg)

## Hardware 

I've used our AZ-Touch MOD kit for ESP32 as hardware plattform. This kit comes with a 2.4 or 2.8 inch tft touchscreen. The demo will work with both screen sizes, but of course it makes more sense to use the bigger 2.8 inch screen in this application.

![My image](https://cdn.shopify.com/s/files/1/1509/1638/products/2.Produkt_500x.jpg?v=1604667072)

You can find all information about the hardware here:
https://www.hwhardsoft.de/english/projects/arduitouch-esp/


## Libraries

Install the following libraries through Arduino Library Manager

Arduino TFT_eSPI Library https://github.com/Bodmer/TFT_eSPI 

Arduino TJpg_Decoder library https://github.com/Bodmer/TJpg_Decoder

You can also download the library also directly as ZIP file and uncompress the folder under yourarduinosketchfolder/libraries/   

After installing the libraries, restart the Arduino IDE. 

## TFT_eSPI Setup

I've prepared a User setup files for the TFT_eSPI library especially for AZ-Touch and ESP32 




## Settings

Enter your WiFi SSID & password in the fields in the WiFi section: 

#define WIFI_SSID "xxxxxx"    // Enter your SSID here 

#define WIFI_PASS "xxxxx"    // Enter your WiFi password here 


## SSL certificates
The tracker is using SSL communication with the website worldometers.info It is necessary needed to add this URL via the WiFi101 / WiFiNINA Firmware Updater of the Arduino IDE to the Arduino MKR WiFi 1010 board

![My image](https://hackster.imgix.net/uploads/attachments/1089827/grafik_5hEqived4T.png?auto=compress%2Cformat&w=740&h=555&fit=max)


## Country settings

You can change/add/delete the countries in the main loop of the program according your interests.

![My image](https://hackster.imgix.net/uploads/attachments/1089828/grafik_eRLuAc5tGD.png?auto=compress%2Cformat&w=680&h=510&fit=max)


# License

This library is free software; you can redistribute it and/or
modify it under the terms of the GNU Lesser General Public
License as published by the Free Software Foundation; either
version 2.1 of the License, or (at your option) any later version.

This library is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
Lesser General Public License for more details.

# RAK831_LoRaGateway

#There should be a start script at 

```
$ sudo nano /opt/ttn-gateway/bin/start.sh

```

At the beginning of this script you will find some lines to generate a reset on pin 25. Change the pin number from “25” to “17”.


Setting up RAK831 using in AS923 Thailand  

1) Install Software in RPI3 lite version

![ScreenShot](https://cdn.instructables.com/FQT/00JT/J1GOYEID/FQT00JTJ1GOYEID.LARGE.jpg?auto=webp&crop=3:2)

https://www.raspberrypi.org/downloads/raspbian/


2) Config RPI3 to use SPI and Install LoRaWan Gateway 

https://www.hackster.io/naresh-krish/getting-started-with-the-rak-831-lora-gateway-and-rpi3-e3351d

if you choos NO you can fill data gateway name, description, Lat,Lon,Alt, Email 

![ScreenShot](https://ttnstaticfile.blob.core.windows.net/media/django-summernote/2017-10-10/90b61a02-3f46-415d-bb73-9837dbd7f59b.png)

  - Clone the installer and start the installation Choos NO  
  
```
$ git clone -b spi https://github.com/ttn-zh/ic880a-gateway.git ~/ic880a-gateway
$ cd ~/ic880a-gateway
$ sudo ./install.sh spi

```

3) Change global_conf.json in /opt/ttn-gateway/bin with example file

```
$ cd /opt/ttn-gateway/bin
$ sudo nano global_conf.json 
```

https://github.com/TheThingsNetwork/gateway-conf/blob/master/AS2-global_conf.json

and Register gateway to TTN 

4) Register Gateway 
Login to ttn account and we go to Console --> Gateways --> Register gateway
Let check the box saying "I'm using the legacy packet forwarder" and we are here :

![ScreenShot](https://ttnstaticfile.blob.core.windows.net/media/django-summernote/2017-10-10/29ae7b7e-2034-4269-b434-74ce886cc890.png)

Hit that "Register Gateway" button !!!!!!

5) Test 

![ScreenShot](https://github.com/worrajak/RAK831_LoRaGateway/blob/master/CSV049.jpg)

![ScreenShot](https://github.com/worrajak/RAK831_LoRaGateway/blob/master/CSV048.jpg)

![ScreenShot](https://github.com/worrajak/RAK831_LoRaGateway/blob/master/CSV047.jpg)

![ScreenShot](https://github.com/worrajak/RAK831_LoRaGateway/blob/master/CSV050.jpg)



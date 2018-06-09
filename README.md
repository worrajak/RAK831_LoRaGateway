# RAK831_LoRaGateway
Setting up RAK831 using in AS923 Thailand  

1) Install Software in RPI3 lite version

![ScreenShot](https://cdn.instructables.com/FQT/00JT/J1GOYEID/FQT00JTJ1GOYEID.LARGE.jpg?auto=webp&crop=3:2){:height="50%" width="50%"}

https://www.raspberrypi.org/downloads/raspbian/


2) Config RPI3 to use SPI
Enable SPI:
The SPI peripheral is not turned on by default. To enable it, do the following.

Run 
```
sudo raspi-config
```
- Use the down arrow to select 9 Advanced Options
- Arrow down to A6 SPI.
- Select yes when it asks you to enable SPI,
- Also select yes when it asks about automatically loading the kernel module.
- Use the right arrow to select the <Finish> button.
- Select yes when it asks to reboot.
  
![ScreenShot](https://hackster.imgix.net/uploads/attachments/351868/image_JTajpthsyS.png?auto=compress%2Cformat&w=680&h=510&fit=max){:height="50%" width="50%"}

3) Install Git
```
sudo apt-get update && sudo apt-get upgrade && sudo apt-get install git -y
```

4) Install LoRa Gateway
```
git clone https://github.com/ttn-zh/ic880a-gateway.git ~/ic880a-gateway
cd ic880a-gateway
sudo ./install.sh spi
```


# Home-NVR-Setup-Guide-SmartHome-Automation

I want to equip my home with a surveillance system that I can access from anywhere. This project is a 101 to set up a synology surveillance station with IP cameras

## Components i used

| Components | Description  | Ammount | Link |
| ------------- | ------------- | ------------- | ------------- |
| Surveillance Computer | Synology NVR1218  | 1  | |
| Surveillance Computer | Synology surveillance licence**  | 1  | |
| Harddisc | WD Purple HDD 4TB | 2 | |
| Switch | D-Link Gigabit Switch, 8x RJ-45, PoE+ (DGS-1008MP) | 2 | |
| IP Cam | D-Link DCS-4633EV | 5 | |


** The first 4 surveillance licences are included when buying a NVR1218 -  to install more IP Cams you have to buy more licences

The cabling is carried out as followed:
<img src= "images/Setup.png" width="800">

---
## Setup IP Cams
I had a lot of trouble setting up the IP cameras at first. So here is a step by step guide

To access the installad IP Cams you need the D-Link SetupWizardSE software (you can find the CD supplied with the product)



---
## Setup an In-house light control depending on image recognition and  defined times of day
When I'm not in the house, I want the light to go on at defined times in any room and stop again after a certain time. Also the light should be turned on when a person approaches the entrance door at night.

This requires the following components:

| Components | Description  | Ammount | Link |
| ------------- | ------------- | ------------- | ------------- |
| Mini-Computer | Raspberry Pi 3 B  | 1  | |
| Switchable sockets | Radio switch set RCS 1000 N Comfort  | 1  | |
| Radio interface |433 MHz radio - transmitter and receiver module set  | 1 | |
| Cables | Jumper Wire Set Female-Female | 3 | |


Raspberry Code:

sudo apt-get install git-core
git clone git://git.drogon.net/wiringPi
cd wiringPi
./build

cd ..
git clone git://github.com/xkonni/raspberry-remote.git
cd raspberry-remote

make send

sudo ./send 10101 4 1


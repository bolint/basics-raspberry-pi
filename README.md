# basics-raspberry-pi
Basic Raspberry Pi init flow to enable SSH and add a root user.

* Download the latest Raspbian from here: https://www.raspberrypi.org/downloads/raspbian
* Write it to the SD card with Etcher: https://etcher.io
* Create an empty `ssh` file on the `/boot` partition's root folder
* Install the SD card and power on the Raspbian
* Login with the default user/pass: `pi` / `raspberry`
* Change the password for the `pi` user with ```$ passwd```
* Update the repos ```$ sudo apt-get update```
* [Optional] Install MC ```$ sudo apt-get install mc```
* [Optional] Change the default ssh port (you can use `nano` or `vim` as well):
  * ```$ sudo mcedit /etc/ssh/sshd_config```
  * ```$ sudo service ssh restart```
* Add your user ```$ sudo adduser yourUser```
* Grant sudo permissions with:
  * ```$ sudo visudo```
  * Add your user: ```yourUser    ALL=(ALL:ALL) ALL```
* [Optinal] Enable WiFi with ```$ sudo raspi-config```
* Upgrade the system ```$ sudo apt-get upgrade```

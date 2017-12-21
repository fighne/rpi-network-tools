# rpi-data-collector
Part of RPI network tools collection.

This set of instructions creates a base from which network packets are collected.
*	A base install of Raspbian
*	After creation of the disk image onto media access the boot parition and add an empty file named 'ssh'
*	Boot up Raspberry Pi, look on your network for raspberrypi.local
*	When present ssh pi@raspberrypi.local with password raspberry
*	Security note:: please change password using current guidelines
*	Run the following command "sudo apt-get update"
*	Run the following command "sudo apt-get dist-upgrade"
*	Run the following command "sudo apt-get clean" <= this is important is using a small size MMC
	
Now for the changes to be made to the raspi-config so run the command "raspi-config" and change the following via the menus
*	set memory split to 16
*	resize the partition
*	update raspi-config
	
Reboot the RPI for all changes to take effect.

RPI overclocking - by James Hayden
	James has completed a number of articles, in which he has found a good set of overclocking values for the RPI variants.
	These are well worth the read and could gain you extra performance, your choice please read.
	https://haydenjames.io/raspberry-pi-safe-overclocking-settings/ <= RPI 
	https://haydenjames.io/raspberry-pi-2-overclock/ <= RPI v2
	https://haydenjames.io/raspberry-pi-3-overclock/ <= RPI v3
	
Setup a RamDisk on the RPI edit the fstab run "sudo nano /etc/fstab" and append the following line
"tmpfs		/data		tmpfs	defaults,noatime,nosuid,mode=0777,size=80m"
or id memory size greater than 512Mb
"tmpfs		/data		tmpfs	defaults,noatime,nosuid,mode=0777,size=148m"

This is the base for the network data collector. Sub folders relate to different tool options based upon this.

	

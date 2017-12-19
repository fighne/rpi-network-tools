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
	*	Run the follwoing command "sudo apt-get clean" <= this is important is using a small size MMC
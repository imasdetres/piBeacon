piBeacon
========

iBeacon/AltBeacon transmitter for the Raspberry Pi - inspired by [~~a blog post by James Nebeker and David G. Young~~](http://developer.radiusnetworks.com/2013/10/09/how-to-make-an-ibeacon-out-of-a-raspberry-pi.html)
 (The article is missing right now, but here's a [mirror](https://web.archive.org/web/20140606045234/http://developer.radiusnetworks.com/2013/10/09/how-to-make-an-ibeacon-out-of-a-raspberry-pi.html)).

## Prerequisites
You'll need to download and install [BlueZ](http://www.bluez.org) version 5.7 or later and install it.

1. Install prerequisite packages

		$ sudo apt-get install libusb-dev libdbus-1-dev libglib2.0-dev libudev-dev libical-dev libreadline-dev

2. Download and install the latest BlueZ

		$ sudo wget www.kernel.org/pub/linux/bluetooth/bluez-5.8.tar.xz
		$ sudo unxz bluez-5.x.tar.xz
		$ sudo tar xvf bluez-5.x.tar
		$ cd bluez-5.x

3. Configure and make BlueZ

		$ sudo ./configure --disable-systemd
		$ sudo make
		$ sudo make install


## Installation
		$ sudo cp piBeacon.conf /etc
		$ sudo cp piBeacon /etc/init.d
		$ sudo update-rc.d piBeacon defaults

## Startup
		$ sudo service piBeacon start

## Shutdown
		$ sudo service piBeacon shutdown


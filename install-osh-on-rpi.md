# Install OSH on Raspberry Pi

## Format SD Card

1. Visit the [SD Association’s website](http://www.sdcard.org/) and download [SD Formatter 4.0](https://www.sdcard.org/downloads/formatter_4/) for either Windows or Mac.
2. Follow the instructions to install the software.
3. Insert your SD card into the computer or laptop’s SD card reader and make a note of the drive letter allocated to it, e.g. G:/
4. In SD Formatter, select the drive letter for your SD card and format it.

## Drag and Drop NOOB files

1. [Download](http://www.raspberrypi.org/downloads/)  the NOOB zip files from Raspberry Pi’s website.
2. Drag and drop all of the extracted files from the NOOB folder into the newly formatted SD card.
3. When files have finished moving, eject the SD card and insert into Raspberry Pi.

## Set Up Pi

1. Plug in your keyboard, mouse, and monitor cables.
2. Now plug the USB power cable into your Pi.
3. Your Raspberry Pi will boot, and a window will appear with a list of different operating systems that you can install. We recommend that you use Raspbian – tick the box next to Raspbian and click on `Install`.
4. Raspbian will then run through its installation process. Note that this can take a while.
5. When the install process has completed, the Raspberry Pi configuration menu (raspi-config) will load. Here you are able to set the time and date for your region, enable a Raspberry Pi camera board, or even create users. You can exit this menu by using **Tab** on your keyboard to move to `Finish`.
6. The default login for Raspbian is username `pi` with the password `raspberry`. **Note that you will not see any writing appear when you type the password**. This is a security feature in Linux.
7. To load the graphical user interface, type `startx` and press **Enter**.

## Download and Deploy Open Sensor Hub Base

1. Open the Terminal and type the following commands

```bash
$ wget https://github.com/opensensorhub/osh-core/releases/download/v1.3.2/osh-base-install-1.3.2.zip
$ unzip osh-base-install-1.3.2.zip
$ cd osh-base-install-1.3.2
$ ./launch.sh
```

## Log into OSH Admin

1. Open browser on Raspberry Pi.
2. Go to [http://localhost:8181/sensorhub/admin]
3. Default login is username: `admin`, password: `admin`

## Clone and Install OSH Core

If you want to work with the code, run the following commands in the Terminal

```bash
$ git clone –recursive https://github.com/opensensorhub/osh-core
$ cd osh-core
$ ./gradlew build -x test
```

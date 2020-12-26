# CrowPi2
Official Elecrow CrowPi2 Repository



# QA file
Solutions to common problems encountered with CrowPi2.

# Image releasing
An updated CrowPi2 image which fixes all the issues below can be downloaded from "https://drive.google.com/file/d/1kL1lQcXDQit4ITlbM5aiwib_8aIJ9ziC/view", saving you the trouble of applying the fixes yourself.

(Nb. its normal for the image to restart when booted for the first time.)


# Expanding the Raspberry Pi file system before upgrading your system
Step 1: Configure the Raspberry Pi (in the terminal) by typing:

````
sudo raspi-config
````

Step 2: select as follows:
![image](https://github.com/Elecrow-RD/CrowPi2/blob/main/pictures/1.png)
![image](https://github.com/Elecrow-RD/CrowPi2/blob/main/pictures/2.png)

Step 3: select “Finish”, then select “YES” when it asks for a reboot.



# Which Raspberry Pi version is recommended by CrowPi2 software?
Its recommended for CrowPi2 software to run on Raspberry Pi 4 2G or higher, preferably 4G or 8GB.



# Why can't the SDA0(pin 0 in BCM mode) pin be used?
This pin is used to detect system startup in order to control the power on/off on the PCBA board, so using it may cause the CrowPi2 to unexpectedly shut down.



# To install an operating system (e.g. Raspbian, Retropie) from scratch, follow these steps:
- Step 1: write \*.img file with selected OS to your SD card as you would normally do
- Step 2: open config.txt file under /boot directory on the resulting SD card and add the following commands at the end of the file
````
hdmi_force_hotplug=1
max_usb_current=1
hdmi_group=2
hdmi_mode=87
hdmi_cvt 1920 1080 60 6 0 0 0
hdmi_drive=2
enable_uart=1
gpio=0=op,dl
````
- Step 3: Safely eject SD card, plug it into CrowPi2 and boot

# LCD doesn’t work after a full update (using command “sudo apt-get dist-upgrade”):
You need to reinstall the LCD library using the following commands:

````
sudo pip install Adafruit_BBIO
sudo pip3 install Adafruit_BBIO
````



# Error in the “using the DHT11 sensor” Python lesson:
There is code typo in the “using the DHT11 sensor” lesson.
  
````
instance = dht11.DHT11(jpin=4)
GPIO.setwarnings(True)
GPIO.setmode(GPIO.BCM)
````

Needs to be changed to:

````
instance = dht11.DHT11(pin=4)
GPIO.setwarnings(True)
GPIO.setmode(GPIO.BCM)
````



# Error in the “making circuit using the bread board” Python lesson:
There is an error in the circuit diagram.
The two ends of the resistor should not be in the same column of the breadboard.
You need to build the circuit following the picture below:
![image](https://github.com/Elecrow-RD/CrowPi2/blob/main/pictures/4.png)
![image](https://github.com/Elecrow-RD/CrowPi2/blob/main/pictures/5.png)



# The mouse or keyboard doesn't work, re-pair it with the dongle:
Step 1:
Pair the mouse:
1. First power off the keyboard and the mouse.
2. Then, power on the mouse and quickly plug the receiver into the CrowPi2.
3. Move the mouse until it controls the cursor on CrowPi2.
4. When this happens it means you have succeeded pairing the mouse. 

Step 2:
Pair the keyboard:
1. Unplug the receiver.
2. Power off the keyboard and the mouse.
3. Plug the receiver into CrowPi2, power on the keyboard and you should see the status light come on. When this happens, immediately press the Esc and Q key at the same time, then you should see the status light(blue light) start blinking.
4. Close the keyboard to the receiver.
5. Once the status light stop blinking and on, it means you have successfully paired the keyboard.
6. If the status light is still blinking, just unplug the receiver and the plug it back into the USB port to see the result of step 5.

Now you can power on the keyboard and mouse, and use them normally.



# The fan makes noise or doesn't work
Issues with the fan being noisy or not working are caused by loose contact between the fan and the fan port.
Firmly pressing down on the fan down should see the issue improve.
There is double-sided tape on the back of the fan.
If you tear it off, and stick it to the fan slot, that should provide a more permanent fix the noise caused by the loose fan.



# Caution
Do not use the power bank and the DC port of the power supply to power CrowPi2 at the same time. It will damage the battery life and even potential safety risks.



# List of CrowPi2 on-board modules
![image](https://github.com/Elecrow-RD/CrowPi2/blob/main/pictures/6.png)

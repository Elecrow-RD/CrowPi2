# CrowPi2
Official Elecrow CrowPi2 Repository



# QA file
Here we will list the problems that may be encountered on CrowPi2 and give solutions.



# Expanding the Raspberry Pi file system
Step 1: Configure the Raspberry Pi (in the terminal) by typing:

````
sudo raspi-config
````

Step 2: select as follows:
![image](https://github.com/Elecrow-RD/CrowPi2/blob/main/1.png)
![image](https://github.com/Elecrow-RD/CrowPi2/blob/main/2.png)

Step 3: select “Finish”, then select “YES” when it asks for a reboot.



# Which Raspberry Pi version is recommended by CrowPi2 software?
CrowPi2 software is recommended to run on Raspberry Pi 4 2G or higher, preferably 4G or 8GB.



# Why SDA0(pin 0 in BCM mode) pin can’t be used?
Since this pin is used to detect the startup pin of the system in order to control the power on/off on the PCBA board. If this pin is used, it may cause the CrowPi2 to shut down.



# To install the new Raspbain system, what configuration should be done:
Step 1: If you use the standard Raspbain image, open the config.txt file under the /boot directory of your TF card, add the following command in the end of the config.txt file(start with a new line)

````
hdmi_force_hotplug=1
max_usb_current=1
hdmi_group=2
hdmi_mode=87
hdmi_cvt 1920 1080 60 6 0 0 0
hdmi_drive=2
enable_uart=1
````

Step 2: Open the terminal and type the following command(ensure that CrowPi2 can access the internet)

````
git clone https://github.com/elecrow-engle/elecrow_crowpi2.git
cd elecrow_crowpi2/GPIO
sudo bash ./start.sh 
````

Step 3: Type the command below to reboot the system:

````
sudo reboot 
````



# LCD doesn’t works after a full update(using command “sudo apt-get dist-upgrade”):
You need to reinstall the LCD library using the following commands:

````
sudo pip install Adafruit_BBIO
sudo pip3 install Adafruit_BBIO
````



# Error of Python lesson “using the DHT11 sensor”:
There is an error in the code of the lesson “using the DHT11 sensor”, as shown below:
  
````
instance = dht11.DHT11(jpin=4)
GPIO.setwarnings(True)
GPIO.setmode(GPIO.BCM)
````


You need to change it like these:

````
instance = dht11.DHT11(pin=4)
GPIO.setwarnings(True)
GPIO.setmode(GPIO.BCM)
````



# Error of Python lesson “making circuit using the bread board”:
There is an error in the circuit picture,that is, the two ends of the resistor should not be in the same column of the breadboard. You need to build the circuit follow the picture below:
![image](https://github.com/Elecrow-RD/CrowPi2/blob/main/4.png)
![image](https://github.com/Elecrow-RD/CrowPi2/blob/main/5.png)



# The mouse or keyboard doesn't work, re-pair it with the dongle:
Step 1:
Pair the mouse:
1. First to power off the keyboard and the mouse.
2. Then, power on the mouse, and plug the receiver to CrowPi2 quickly.
3. Slide the mouse until you can control the cursor on CrowPi2.
4. When you can control the cursor on CrowPi2 with the mouse, it means you have succeeded pair the mouse. 

Step 2:
Pair the keyboard:
1. Unplug the receiver.
2. Power off the keyboard and the mouse.
3. Plug the receiver to CrowPi2, power on the keyboard and you will see the red light will on. When the red light still on, press the Esc and Q key at the same time immediately, then, you will see the red light is blinking.
4. Close the keyboard to the receiver, once the blue light and red light on at the same time, it means you have paired the keyboard.
5. You have successfully pair the keyboard and mouse.

Now you can power on the keyboard and mouse, and use them normally.



# Release information about CrowPi2 image
We have not released the CrowPi2 image currently, therefore, backup your image after receiving CrowPi2 yourself! Any news about releasing image, we will update to our official website(https://www.elecrow.com/)



# The fan makes noise or doesn't work
Noise or fan not working are caused by loose contact between the fan and the fan port, you can directly press the fan down to fix the fan tightly, and then it should be work.
In addition, if you want to permanently fix the fan, there is a double-sided tape on the back of the fan, you only need to tear it off, and then stick it to the fan slot, so that there will be no noise caused by the loose fan in the future.



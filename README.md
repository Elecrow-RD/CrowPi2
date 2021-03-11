# CrowPi2
<a href="https://www.elecrow.com"><img src="https://github.com/Pearl-852/CrowPi2/blob/main/images/Elecrow_logo.png" alt="Elecrow"></a>  
![image](https://github.com/Pearl-852/CrowPi2/blob/main/images/crowpi2.jpg)  

<br>

# Official CrowPi2 system image
The latest CrowPi2 system image is available [HERE](https://drive.google.com/file/d/1kL1lQcXDQit4ITlbM5aiwib_8aIJ9ziC/view).  

***Note:** It's normal for your system to restart once, when booted for the first time, in order to expand the filesystem automatically.*  

<br>

# Initial Setup
Run the ***Raspberry Pi Setup Wizard***, it will guide you through the process.  
1. Press **Alt**+**F2**, a ***Run*** dialog box appears  
2. Type the following command, then press **Enter**. <br> `sudo piwiz`  
3. Follow the on-screen instructions to complete the setup process.  
***Note:** For more details on the Raspberry Pi Setup Wizard, see [HERE](https://www.raspberrypi.org/blog/raspbian-update-june-2018/).*  

<br>

# Frequently Asked Questions
Solutions to common problems encountered with CrowPi2 can be found [HERE](https://github.com/Pearl-852/CrowPi2/blob/main/faq/TOC-FAQ.md#frequently-asked-questions).  

<br>

# Known Issues
Known issues that have been found are being listed [HERE](https://github.com/Pearl-852/CrowPi2/blob/main/known_issues/TOC-KI.md#known-issues).  

<br>

# Caution
Do not use any power bank and the DC-12V power port to power the CrowPi2 at the same time. It will damage the power bank battery and may even pose potential safety risks.  

<br>

# Helpful resources that could aid with your programming
- [Raspberry Pi offical website](https://www.raspberrypi.org/help/)  
- [Pinout! - The Raspberry Pi GPIO pinout guide.](https://pinout.xyz/)  
***Note:** You may easily display the hardware features of your particular Raspberry Pi board using the command `pinout` in a terminal.*  

<br>

# Information of CrowPi2 on-board modules

### Digital Module:
| Module             | GPIO pin (Function name)      | GPIO pin (BCM mode)   | GPIO pin (Board mode) |
| -------------------| ------------------------------| ----------------------| ----------------------|
| Relay              | GPIO29                        | 21                    | 40                    |
| PIR motion sensor  | GPIO4                         | 23                    | 16                    |
| Sound sensor       | GPIO5                         | 24                    | 18                    |
| IR receiver        | GPIO28                        | 20                    | 38                    |
| Servo              | GPIO24                        | 19                    | 35                    |
| Stepper motor      | GPIO21, GPIO22, GPIO23, GPIO6 | 5, 6, 13, 25          | 29, 31, 33, 22        |
| Buzzer             | GPIO1                         | 18                    | 12                    |
| Vibration motor    | GPIO2                         | 27                    | 13                    |
| Touch sensor       | GPIO0                         | 17                    | 11                    |
| RGB matrix         | GPIO26                        | 12                    | 32                    |
| Ultrasonic sensor  | GPIO25, GPIO27                | 26, 16                | 37, 36                |
| Tilt sensor        | GPIO3                         | 22                    | 15                    |
| DHT11 sensor       | GPIO7                         | 4                     | 7                     |

### Analog & SPI Module:
| Module             | Analog channel                |
| -------------------| ------------------------------|
| Joystick sensor    | SPI1;y-axis:0;x-axis:1        |
| Button matrix      | SPI1;4                        |
| RFID-RC522         | SPIO                          |

### I2C Module:
| Module             | I2C address                   |
| -------------------| ------------------------------|
| Segment            | 0x70                          |
| LCD display        | 0x21                          |
| Light sensor       | 0x5C                          |


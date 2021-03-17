# How to backup the system SD card?

It is alway a good practise to keep a backup of the system SD card in case anything happens; especially, if you are not too familiar with running the Raspberry Pi.  

Before you begin, prepare the following items  
* 32GB microSD card or larger capacity  
* USB microSD card reader  

Next, we will use the built-in **SD Card Copier** app to do the backup, following the steps below  
1. Insert the new microSD card into the USB card reader.  
2. Plug the card reader into one of the available USB ports on the CrowPi2.  
3. A **Removable medium is inserted** dialog box appears.  
4. Click **Cancel** to dismiss it.  
5. Click the **Menu** button located on the upper left hand corner.  
6. Navigate to **Accessories** and choose **SD Card Copier**.  
7. A **SD Card Copier** window appears.  
8. In the **Copy From Device:** list box, choose the first device **/dev/mmcblk0**  
9. In the **Copy To Device:** list box, choose the last device **/dev/sdX** shown if you have more than 1 USB storage device plugged in.  
***Caution:** Be sure to select the correct device, because the backup process will ERASE ALL DATA previously stored in the selected device.*  
10. Tick the **New Partition UUIDs** check box.  
11. Click **Start** to begin the backup process.  
12. After the process has completed, click **Close** to close the app.  

<br>

[**<< BACK to FAQs**](./TOC-FAQ.md#frequently-asked-questions)


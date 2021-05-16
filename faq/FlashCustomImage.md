# How to flash a new CrowPi2 system image?

To write a new system SD card, follow the steps below  

1. Download the lastest CrowPi2 system image from this [link](../README.md#official-crowpi2-system-image) and save it to your **Downloads** folder.   
2. Insert a new *microSD card* (32GB or larger) with a *USB microSD Card Adapter* into a USB port of the CrowPi2.  
3. Launch the **Raspberry Pi Imager** app (Menu > Accessories > Imager).  
![imager-custom-01](../images/imager-custom-1.png)  
4. Click **CHOOSE OS**.  
![imager-custom-02](../images/imager-custom-2.png)  
5. From the ***Operating System*** list, choose **Use custom**.  
![imager-custom-03](../images/imager-custom-3.png)  
6. In the pop-up **Select image** windows, choose the **Downloads** folder from the left pane, then select the CrowPi2 image that you have downloaded in step 1 above, (Ex. *crowpi2_release_v1.2.0_en_20210305.zip*) and click **Open**.  
![imager-custom-04](../images/imager-custom-4.png)  
7. Click **CHOOSE STORAGE**.  
![imager-custom-05](../images/imager-custom-5.png)  
8. From the ***Storage*** list, choose your desired SD Card for flashing with the selected image.  
![imager-custom-06](../images/imager-custom-6.png)  
9. Review your selected ***OS*** and ***Storage*** and then click **WRITE**.  
![imager-custom-07](../images/imager-custom-7.png)  
10. Click **YES**, when you are ready to start the flashing process.  
![imager-custom-08](../images/imager-custom-8.png)  
11. Enter your user password in the pop-up **Authentication** window and press **OK**.  
![imager-custom-09](../images/imager-custom-9.png)  
12. After flashing has completed, click **CONTINUE** and close the **Raspberry Pi Imager** app.  
![imager-custom-10](../images/imager-custom-10.png)  
13. Congratulation! Your new ***CrowPi2 SD Card*** is now ready for use in the CrowPi2. Shutdown the system, then unplug the power and replace the system SD Card with the new ***CrowPi2 SD Card***.  
14. Lastly, once the system has booted up, run the **Raspberry Pi Setup Wizard** to complete the initial system setup. (See this [link](../README.md#initial-setup) for instructions.)  

<br>

[**<< BACK to FAQs**](./TOC-FAQ.md#frequently-asked-questions)

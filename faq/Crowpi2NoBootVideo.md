# How to disable the Crowpi2 Boot Video at bootup?

Edit the **rc.local** file from the ***/etc*** directory.  
1. Press **Ctrl**+**Alt**+**T**, a new Terminal window appears.  
2. At the command prompt, type `sudo nano /etc/rc.local` and press **Enter**.  
3. locate the following line  
```
omxplayer /usr/share/elecrow/video/boot_video.mp4 &
```
4. Add a '**#**' at the beginning to comment out the command as shown below,
```
#omxplayer /usr/share/elecrow/video/boot_video.mp4 &
```
5. Press **Ctrl**+**X**, **Y** and then **Enter** to save the changes.  
6. From the next system bootup, the Crowpi2 Boot Video will not be played.  
***Note:** If you change your mind later, just repeat the instructions above and delete the* *'**#**' added in step 4.*  

<br>

[**<< BACK to FAQs**](./TOC-FAQ.md#frequently-asked-questions)


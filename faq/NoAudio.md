# No audio sound after a system upgrade (sudo apt full-upgrade).

Since the new release of Raspberry Pi OS from 4th of December 2020, which switches to use the PulseAudio sound server. In some cases, this might affect the audio output settings after the system upgrade.  

To correct the problem, see the instructions [HERE](https://www.raspberrypi.org/blog/new-raspberry-pi-os-release-december-2020/) under the sections of ***How do I get it?*** and ***Updates***.  

### Or follow the steps below:
1. Update your system to the latest version  
`sudo apt update && sudo apt full-upgrade`  
(It is safe to just accept the default answer to any questions you are asked during the update procedure.)
2. Install the PulseAudio Bluetooth support  
`sudo apt purge bluealsa`  
`sudo apt install pulseaudio-module-bluetooth`  
`reboot`  
3. Swap over the volume and input selector on the taskbar from ALSA to PulseAudio, after your system has restarted.  
a) Right-click a blank area on the taskbar and choose **Add / Remove Panel Items**.  
b) Find the plugin labeled **Volume Control (ALSA/BT)** in the list, select it and click **Remove**.  
c) Click the **Add** button, find the plugin labeled **Volume Control (PulseAudio)** and click **Add**.  
d) Use the **Up** or **Down** button to move the new **Volume Control** to your desired position.  
e) Click the **Close** button, to close the ***Panel Preferences*** window.  
4. Right-click on the **Volume Control** icon on the taskbar, select **Audio Outputs** and choose **HDMI** if it wasn't ticked.  
5. Finally, to prevent some applications that are ignoring the effect of the PulseAudio output switcher, which probably caused by an old ALSA configuration file still being on the system. Remove it with the following command in a terminal.  
`rm ~/.asoundrc`  

<br>

[**<< BACK to FAQs**](./TOC-FAQ.md#frequently-asked-questions)


# Power shuts off automatically after about 30 seconds during boot up.

It is missing the SDA0 (BCM_GPIO-0) signal from the Raspberry Pi.  

Put the system microSD card into a PC and use a text editor to verify the **config.txt** file under the **/boot** partition on the microSD card contains the following statement toward the end of the file.  
`gpio=0=op,dl`  

***Note:** Make sure there is no typos **gpio=0** <-- This is a zero*  

If that statement does not exist, add it to the end of the file and save it.  

<br>

[**<< BACK to FAQs**](./TOC-FAQ.md#frequently-asked-questions)


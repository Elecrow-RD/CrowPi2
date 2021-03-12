# Why can't the SDA0 (BCM_GPIO-0) pin be used?

The **SDA0** (BCM_GPIO-0) pin is reserved for Raspberry Pi startup detection, in order to control the power on/off of the PCBA board. So without this pin signal from the Raspberry Pi, the CrowPi2 will shutdown unexpectedly.  

<br>

[**<< BACK to FAQs**](./TOC-FAQ.md#frequently-asked-questions)


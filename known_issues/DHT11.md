# Error in the Python lesson: Using the DHT11 sensor.

There is a coding typo found in the **Using the DHT11 sensor** lesson.  
  
````
instance = dht11.DHT11(jpin=4)    <-- typo
GPIO.setwarnings(True)
GPIO.setmode(GPIO.BCM)
````

Needs to be changed to:  

````
instance = dht11.DHT11(pin=4)
GPIO.setwarnings(True)
GPIO.setmode(GPIO.BCM)
````

<br>

[**<< BACK to Known Issues**](./TOC-KI.md#known-issues)


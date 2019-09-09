# IDD-Fa19-Lab1: Blink!

**A lab report by Samson Schirmer**

## Part A. Set Up a Breadboard

[Image here](https://github.com/sas695/IDD-Fa18-Lab1/blob/master/Breadboard.JPG)



## Part B. Manually Blink a LED

**a. What color stripes are on a 220 Ohm resistor?**
     
     red, red, black, black, brown
     
**b. What do you have to do to light your LED?**

     Press the button in order to complete the circuit.

## Part C. Blink a LED using Arduino

### 1. Blink the on-board LED

**a. What line(s) of code do you need to change to make the LED blink (like, at all)?**

	void loop() {
  digitalWrite(LED_BUILTIN, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(15);                       // wait for a second
  digitalWrite(LED_BUILTIN, LOW);    // turn the LED off by making the voltage LOW
  delay(15);
  }

**b. What line(s) of code do you need to change to change the rate of blinking?**

     The values in the delay() command should be changed.
     
**c. What circuit element would you want to add to protect the board and external LED?**

     A resistor.

**d. At what delay can you no longer *perceive* the LED blinking? How can you prove to yourself that it is, in fact, still blinking?**

When delay() = 10.

**e. Modify the code to make your LED blink your way. Save your new blink code to your lab 1 repository, with a link on the README.md.**


### 2. Blink your LED

**Make a video of your LED blinking, and add it to your lab submission.**

[Video here](https://github.com/sas695/IDD-Fa18-Lab1/blob/master/MyBlink.mov)


## Part D. Manually fade an LED

**a. Are you able to get the LED to glow the whole turning range of the potentiometer? Why or why not?**
     Yes, as I increase the resistance using the potentiameter, the LED glow is dimmer.
     As I decrease the resistance using the potentiameter, the LED glow is brighter.

## Part E. Fade an LED using Arduino

**a. What do you have to modify to make the code control the circuit you've built on your breadboard?**
     I modified the code so that the LED is on pin 11 instead of pin 9.
     
**b. What is analogWrite()? How is that different than digitalWrite()?**
     The analogWrite() function writes an analog value (PWM wave) to a pin. It can be used to light a      LED at varying brightnesses; whereas the digitalWrite() function can only be turned on (full 5V)      or of (0V). 

## Part F. FRANKENLIGHT!!!

### 1. Take apart your electronic device, and draw a schematic of what is inside. 

[Image here](https://github.com/sas695/IDD-Fa18-Lab1/blob/master/Device%20Schematic.jpg)

**a. Is there computation in your device? Where is it? What do you think is happening inside the "computer?"**

     Yes, there is a 8-bit microprocessor (CP6604BM) that computes mouse movement to cursor location      on the monitor.

**b. Are there sensors on your device? How do they work? How is the sensed information conveyed to other portions of the device?**

Yes, there are optical sensors which use a LED and a light detector (an array of photodiodes), to detect movement relative to the mouse surface.

**c. How is the device powered? Is there any transformation or regulation of the power? How is that done? What voltages are used throughout the system?**

The device is powered by a USB 1.0 port. It's energy trandformation can be described with a power source of 5 V @ 100 mA (0.5 W) 

**d. Is information stored in your device? Where? How?**

Yes there is information stored in the Microprocessor, which is a digital integrated circuit that accepts binary data as input, processes it according to instructions stored in its memory and provides results as output. 

### 2. Using your schematic, figure out where a good point would be to hijack your device and implant an LED.

I plugged in my USB powered Apple mouse and located the power and ground wires and their location on the microchip. I then constructed a simple circuit on my breadboard to light an LED when the power and ground from the LED circuit were connected to the power and ground of the Apple mouse. 

### 3. Build your light!

[Image here](https://github.com/sas695/IDD-Fa18-Lab1/blob/master/IMG_2543.jpg)

[Video here]()

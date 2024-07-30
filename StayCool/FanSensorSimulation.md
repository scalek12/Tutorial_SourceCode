# Fan and Sensor

## Fan and Sensor @unplugged
In this tutorial you will use the micro:bit to simulate how a
 temperature sensor will decide when to turn a fan on and off.


## Step 1: Starter Code @fullscreen
The code has already been started for you. The red blocks at the beginning of
 the ``||basic:forever||`` loop set the value of two different variables, 
 ``||variable:celsius||`` and ``||variable:farenheit||``. 
Since the micro:bit temperature sensor reads in celsius, we convert that value to farenheit.
We show the farenheit number on the micro:bit LED matrix using the ``||basic:showNumber||`` block.
In the next step we'll turn the fan on if the temperature gets too hot.

## Step 2: Decide if the temperature is too hot
Now look at the ``||logic:if then||`` block. Notice that the code will compare
the ``||variable: farenheit||`` reading to 85 degrees. If it's warmer than 85 degrees the fan should
turn on. Right now that's not what the code says will happen. Let's fix this. Our fan is connected to
the micro:bit on ``||digitalWritePin P0||``. We will turn the fan on by sending data to ``||P0||``.  To signal the
fan to turn on, we need to send a '1' to the ``||digitalWritePin P0||``. Look at the code below,
we're sending a 0, not a 1. Modify the ``||digitalWritePin P0||`` block and change the value we send from 0 to 1.
```ghost
if (0 == 0) {
    	
    }
 pins.digitalWritePin(DigitalPin.P0, 1)    
 basic.showIcon(IconNames.Happy)
 basic.pause(5000)
```

## Step 3: Show a happy face
When the temperature is warmer than 85 degree, we send a signal to turn the fan on. 
We will also show a happy face. Find the ``||basic:showIcon||`` block and add it below
the ``||digitalWritePin P0||`` block. Modify the ``||basic:showIcon||`` to show a happy face. 
Also add a ``||basic: pause||`` block below the 
 ``||basic:showIcon||`` block to make sure that we have time to see the happy face. 
 Change the value for the ``||basic: pause||`` to 5 seconds.


## Step 4: Test the Code
Use the simulator to test your code. You can change the temperature value in the
simulator to see what happens. Once you reach 85 degrees farenheit, watch for your 
happy face and 1 signal on ``||P0||``.
Great Job!

## Step 5(optional): Copy the code and make changes
If you have time, try making modifications to this code. You can add an
else block ``||logic:else||`` to your if statement ``||logic:if then||``. What if the 
temperature is below 85 degrees? You can turn the fan off by sending a 0 signal 
to ``||P0||``. You could also show a sad face icon. 


```template
let celsius = 0
let farenheit = 0

basic.forever(function () {
    celsius = input.temperature()
    farenheit = 1.8 * celsius + 32
    basic.showNumber(farenheit)
    if (farenheit > 85) {
        pins.digitalWritePin(DigitalPin.P0, 0)
    }
})

```
    
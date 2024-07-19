# Roll The Die

## Role a Die, Make a Decision @unplugged
In this tutorial you will use the micro:bit to make a game that will to generate a number and then decide
if that number is a winner.


## {Step 1 @fullscreen}
The code has already been started for you. It says that  when someone presses button **A** (``||input:on button A pressed||``),
the micro:bit will pick a random number (``||math: pick random||``).  

It will assign the random number to a variable the we created named ``||variable:number_on_die||``. 
Then micro:bit will show that number on the screen. 

## {Step 2}
Let's test out this code using the simulator. On the simulator to your left click the
A button on the micro:bit. 

You will see a number appear on the LED matrix. Click the **A** button several more times. Observe what numbers appear.

## {Step 3}
We want our micro:bit to act like a die. Now, think about rolling a die. What is the lowest number that you could roll? 
What is the highest number that you could roll?

Click on the ``||math: pick random||`` block in the code below. You see that the code 
says the lowest number generated will be 0 and the highest number will be 10. 
Is that right? 

Change the lowest and highest numbers to match what would be on a die. Test your changes using
the simulator. Observe what numbers appear.

## {Step 4}
Now that you have the die rolling between 1 and 6, decide on a "winning
number."  Pick a number between 1 and 6 as the winning number. 

In the next step  you'll use the ``||logic: if then else||`` block 
to decide when the ``||variable: number_on_die||`` is a winner.
```ghost
if (0 == 0) {
    	
    } else {
    	
    }
```

## {Step 5}
Look at the ``||logic:if then else||`` block. We want the micro:bit to compare the value
of ``||variable: number_on_die||`` to the winning number you chose in the last step.
Let's add code to compare two numbers. 

First, click on the ``||logic:Logic||`` category
in the toolbox. Drag the ``||logic: 0 = 0 ||`` block and replace the ``||logic: true||`` section of the ``||logic: if||`` block.

## {Step 6}
Next you will compare the ``||variable: number_on_die||`` to your winning number.

Click the ``||variable:Variable||`` tool and choose ``||variable: number_on_die||``
drag this block to the first circle of the ``||logic: 0=0||`` block. 

Then put your winning number in the second circle of the ``||logic: 0=0||`` block.

## {Step 7}
What should happen when the die rolls a winning number? You'll show a happy face
on the micro: bit. When it's not a winning number, you'll show a sad face. In the next
step, let's add code to show the faces.
```ghost
  basic.showIcon(IconNames.Happy)
  basic.showIcon(IconNames.Sad)
```

## {Step 8}
From the ``||basic:Basic||`` tool, drag the ``||basic:showIcon||`` and place
it inside the ``||logic:if||`` portion of the ``||logic: if then else||`` block.

Choose the ``||basic:Happy||`` icon from the ``||basic:showIcon||`` block.

Next, drag another ``||basic:showIcon||`` block inside the ``||logic: else||`` block.

Choose the ``||basic:Sad||`` icon from the ``||basic:showIcon||`` block.

## {Step 9}
Use the simulator to test your code.
Great Job!

## {Step 10}
If you have time, try making modifications to this code. You could change the winning number,
add another if statement to make more winning numbers, or add a winning and losing sound.
To make changes, you can copy these code blocks into a new project where you can add more code blocks.


```template
let number_on_die = 0
input.onButtonPressed(Button.A, function () {
    number_on_die = randint(0, 10)
    basic.showNumber(number_on_die)
     if (true) {
    	
    } else {
    	
    }
})

```
    
# Lesson 6 - Using the Light Sensor

## Overview

In this tutorial, you'll write JavaScript code on your iPad to control 
the **brightness** of the micro:bit's LEDs based on **light sensor input**. 
You'll learn how to:

* Read light levels using the built-in **light sensor**
* Use a **variable** to store the light level
* Use **conditional logic** to adjust LED brightness
* Test your code in the **simulator** and on the physical **micro\:bit**
* Reflect on your learning in your **notebook**

💡 The micro:bit has a built-in light sensor — it measures light using 
the same LEDs used for the display!

## Step 1  Start Your Project

Add a project comment at the top of your file:  
`// Adjust LED brightness based on ambient light level`

## Step 2 - Create a Variable

Define and initialize a variable to store the light level

```typescript
// Adjust LED brightness based on ambient light level
let lightLevel: number
lightLevel = 0
```

## Step 3 - Store the Light Level
Use the ``||input:light level||`` function to read the current light level (0-255) 
and story it in the variable. Add a comment above this statement:  

`// Read light level from micro:bit's light sensor`

```typescript
// Adjust LED brightness based on ambient light level
let lightLevel: number
lightLevel = 0

// Read light level from micro:bit's light sensor
lightLevel = input.lightLevel()
```

## Step 4 - Add a Forever Loop

Use a ``||basic:forever||`` function to make the program run continuously.  
Add a comment above the loop:  
`// Continuously update light level and adjust LED brightness`

```javascript
// Continuously update light level and adjust LED brighness`
basic.forever(function () {
  // Read light level from micro:bit's light sensor
  lightLevel = input.lightLevel()

  // Your brightness adjustment code goes here
})
```
## Step 5 - How LED Brightness Works 
You use the led commands to adjust brightness inside the ``||led:Led||`` category 
to adjust the brightness of the led lights. The values are (0-255), where 0 is very 
dim and 255 is very bright.

## Step 5 - Adjust LED Brightness with Conditionals

Inside the `forever` loop, use an ``||logic:if else||``structure to change 
brightness based on light level. Use ``||led:set brightness||`` found in 
``||led:Led ... more||`` to set the brightness. 
* Light level < 50 - set brightness to 255 - Bright in the dark
* Light level < 150 - set brihtness to 150 - Dim in medium light 
* Otherwise - set brightness to 100 - Very dim in bright light 
Add inline comments for each condition to explain what's happening

```javascript
// Continuously update light level and adjust LED brighness`
basic.forever(function () {
  // Read light level from micro:bit's light sensor
  lightLevel = input.lightLevel()

  if (lightLevel < 50) { 
    led.setBrightness(255)  // Bright in the dark
  } else if (lightLevel < 150) {
    led.setBrightness(100)  // Dim in medium light
  } else {
    led.setBrightness(10)   // Very dim in bright light
  }
})
```

## Step 6 - Display a Pattern

After setting brightness, add an LED display to test brightness visually.  
Comment:  
``// Display icon at current brightness level``

```javascript
// Continuously update light level and adjust LED brighness`
basic.forever(function () {
  // Read light level from micro:bit's light sensor
  lightLevel = input.lightLevel()

  if (lightLevel < 50) { 
    led.setBrightness(255)  // Bright in the dark
  } else if (lightLevel < 150) {
    led.setBrightness(100)  // Dim in medium light
  } else {
    led.setBrightness(10)   // Very dim in bright light
  }
  
  // Display icon at current brightness level
  basic.showIcon(IconNames.SmallHeart)
})
```

## Step 7 - Test in the Simulator

Tap the **Play** button in the simulator.
Use the **light slider** (bottom of simulator) to simulate changing light conditions.
You should see the icon change brightness depending on the simulated light level.

## Step 8 - Download to Your micro:bit

1. Tap **Download**.
2. Connect your iPad to the micro\:bit using **Bluetooth pairing**.
3. Send the program to the micro\:bit.
4. Try covering the micro\:bit with your hand or turning off the lights — the LED brightness should increase!

## Step 9  Reflect in Your Notebook

In your notebook, respond to these reflection prompts:

1. What is the range of values the **light sensor** can read?
2. How did your program change the **LED brightness** based on light?
3. Why is it useful to use **conditional logic** with sensor data?
4. Describe a real-world application where this kind of sensor-to-output programming might be used.

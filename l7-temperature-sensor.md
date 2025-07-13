# Lesson - Temperature Sensor

## 🧭 Overview

In this tutorial, you'll learn how to use the **built-in temperature sensor** on 
the micro:bit to read and display the **current temperature**. You'll write 
JavaScript code in the micro\:bit app on your **iPad**, run it in the simulator, 
and download it to your physical device.

You will:

- Read temperature values using the `input.temperature()` function
- Store values in a variable
- Display temperature on the LED screen
- Use conditionals to respond to different temperature ranges
- Reflect on your learning in your notebook

---

## Step 1 – Start a New Project

At the top of your code, write this comment:  
`// Read and display temperature using micro:bit sensor`

## Step 2 – Declare and Initialize the Variable

Create a variable to store the temperature.  
Add a comment above it:  
`// Declare a variable to hold the temperature reading`

```javascript
// Read and display temperature using micro:bit sensor

// Declare a variable to hold the temperature reading
let temp: number
temp = 0
```
---

## Step 3 – Create a Forever Loop

Type the following loop to read and display the temperature every second.  
Comment the code with a comment block:  
`
/*
Read the current temperature in degrees Celsius
Display the temperature on the LED screen
Pause for 1 second before repeating
*/
`
```javascript
basic.forever(function () {
    /*
    Read the current temperature in degrees Celsius 
    Display the temperature on the LED screen 
    Pause for 1 second before repeating 
    */
    temp = input.temperature()
    basic.showNumber(temp)
    basic.pause(1000)
})
```

## Step 4 – Add Conditionals to React to Temperature

You can give the micro:bit logic to respond to different temperatures.
* Temperature < 15 - show a square - cold 
* Temperature < 25 - show happy - comfortable 
* Otherwise - surprised - hot 
Add inline comments for each condition: 

```javascript
basic.forever(function () {
  temp = input.temperature()

  if (temp < 15) {
    basic.showIcon(IconNames.Square)  // Cold
  } else if (temp < 25) {
    basic.showIcon(IconNames.Happy)   // Comfortable
  } else {
    basic.showIcon(IconNames.Surprised) // Hot
  }

  basic.pause(1000)
})
```


##  Step 5 – Test in the Simulator

1. Tap the **Play** button in the simulator.
2. Use the **temperature slider** to change the value and observe the icon changes.
   Check that each temperature range shows the correct icon.

---

##  Step 6 – Download to Your micro:bit

1. Tap **Download**.
2. Pair your **micro:bit via Bluetooth** (or connect via USB on computer).
3. Transfer the code to your device.
4. Try warming the micro:bit in your hand or cooling it near a fan — watch the icon change based on temperature!

## Step 7 – Reflect in Your Notebook

In your notebook, respond to the following:

1. What function did you use to read the temperature?
2. What variable stored the temperature value?
3. How did the micro:bit respond to different temperature ranges?
4. Why might this kind of sensor-based logic be useful in a real-world product?
5. Optional: How could you extend this program to give a temperature warning or sound alert?

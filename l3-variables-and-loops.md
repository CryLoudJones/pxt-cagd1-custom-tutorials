# Lesson 3 - Variables & Loops

### Overview

In this tutorial, you'll learn how to use **variables** and **loops** with **JavaScript** 
in the **micro:bit MakeCode editor**. These are key coding tools used to store and repeat information.

You'll use:

* A **variable** to store a number
* A **for loop** to count through values
* A **forever loop** to keep your code running
* The **LED display** to show your results

You'll also practice adding **code comments** and finish with a written **reflection** in your notebook.

### Step 1 - Start Your Project

At the very top of your code, type this comment:  

`// This project shows how to use variables and loops on the micro:bit`

### Step 2 - Create a Variable

Drag the ``||variables:let||`` block from the ``||variables:Variables||`` category in the 
Toolbox to declare a variable: `counter`. Then initialize it to zero.  
Add a comment above the line:  
`// Create a variable to hold the counter value`

```typescript
// Create a variable to hold the counter value
let counter: number
counter = 0
```

### Step 3 - Use a For Loop to Show Numbers 0–4

Drag a ``||loops:for||`` loop from ``||loops:Loops||`` to loop from 0 to 4.  
Show the index on each iteration.  
Add a comment above it:  
`// Use a for loop to show numbers from 0 to 4`

This loop shows numbers 0, 1, 2, 3, 4 one after the other.
```typescript
// Use a for loop to show numbers from 0 to 4
for (let i = 0; i < 5; i++) {
  basic.showNumber(i)
}
```

### Step 4 - Add a Forever Loop to Count Up

Drag the ``||basic:run code forever||`` from the ``||basic:Basic||`` category into your code.  
Inside the loop, increase the counter by 1 (use ``||variables:change||``).  
  
Show the number. Then pause for one second.  
  
Add comments to explain what it does:  
`
// Increase counter by 1 every second  
// Show the updated value on the screen
`

```typescript
// Increase counter by 1 every second
// Show the updated value on the screen
basic.forever(function () {
  counter += 1
  basic.showNumber(counter)
  basic.pause(1000)
})
```

### Step 5 - Test in the Simulator

Tap the **Play** button to test your code in the **simulator** (in the top-left of the screen).
You should see:

* Numbers 0-4 scroll one time
* Then the counter starts increasing every second

### Step 6 - Download to Your micro:bit

1. Tap the ``|Download|`` button.
2. Follow the prompts to **connect your micro\:bit** via Bluetooth

### Step 7 - Reflect in Your Notebook

Answer these questions in your notebook:

1. What is a **variable**, and how did you use one in this tutorial?
2. What is a **loop**, and how is the `for` loop different from the `forever` loop?
3. Why might a programmer use a loop instead of writing the same code over and over?
4. What did you notice about how JavaScript is written in MakeCode?
5. Optional: How could you make this program more interactive or useful?


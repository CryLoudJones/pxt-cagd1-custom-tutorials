# Lesson 4 - Conditionals & Button Presses

## Overview

In this tutorial, you'll learn how to use **if/else conditionals** to respond 
to **button presses** on the micro:bit. You'll write JavaScript code in MakeCode to:

* Check if **Button A** or **Button B** is pressed
* Use an **if/else** structure to decide what to show
* Test your code in the simulator and on the physical micro:bit
* Reflect on how conditionals work in your notebook

*Need help? Tap the **Hint** button in MakeCode for sample code at any time.*

## Step 1 - Start Your Project

Type a comment at the top: 
  
`// This program uses conditionals and button presses on the micro:bit`

## Step 2 - Create a Button Press Event

Drag the ``||input:run code on button pressed||`` block from the ``||input:Input||``
category into your code.  
Add a comment above the event:  
  

`// Run code when button A is pressed`

```typescript
// Run code when button A is pressed
input.onButtonPressed(Button.A, function () {

})
```

## Step 3 - Add an If/Else Conditional

Inside the button press block, add an ``||logic:if else||`` block from 
the ``||logic:Logic||`` category.  
Replace `true` with a condition: `counter % 2 == 0`.  
Add this comment above the if statement:  
  
`// Check if counter is even`

```typescript
// Run code when button A is pressed
input.onButtonPressed(Button.A, function () {
  // Check if counter is even
  if (counter % 2 == 0){

  } else {

  }
})
```

## Step 4  - Add a Variable to Track State

At the top of your code after the commen use ``||variables:let||`` to declare `counter`.  
Then use ``||variables:equals||`` to initialize it.

```typescript
// This program uses conditionals and button presses on the micro:bit
let counter: number 
counter = 0
```

## Step 5 - Track State 
Inside the button press block, increase the counter by 1.  
Inside your `if...else`, use ``||basic:show icon||`` to display different 
icons based on the condition.

```typescript
// Run code when button A is pressed
input.onButtonPressed(Button.A, function () {
  // Check if counter is even
  if (counter % 2 == 0) {
  basic.showIcon(IconNames.Happy)
  } else {
    basic.showIcon(IconNames.Sad)
  }
})
```
## Step 6 - Test in the Simulator

Tap **Play** to run your code in the simulator.  
Press the virtual **A button** several times.  
You should see the icon change based on whether the counter is even or odd.

## Step 7 - Download to Your micro:bit

Tap ``|Download|`` and follow the instructions to download to your micro:bit.

## Step 7 - Reflect in Your Notebook

Answer the following reflection questions:

1. What is a **conditional** in programming?
2. How does the micro:bit use **button events** to trigger actions?
3. What does your program do when the counter is even vs. odd?
4. Why might you use **if/else logic** in real-world micro:bit apps?

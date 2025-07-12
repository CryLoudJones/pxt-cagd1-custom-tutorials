# Lesson 2 - Introduction to micro:bit

## Overview:

In this tutorial, you'll explore how to use the micro:bit's LED screen to **display information** using four output types:

* **Strings** (text messages)
* **Numbers**
* **Built-in icons**
* **Custom LED patterns**

You'll also:

* Write clean, commented code
* Use the simulator to test your program
* Download and run it on the micro:bit
* Reflect on how these outputs work compared to other programming environments

*Press the **Hint** button if you want to see sample code for any step.*


## Step 1 – Add a Project Comment

Start with a **comment at the top** that explains the goal of your program.  
`// micro:bit output demo: string, number, icon, and custom LED pattern`

```typescript
// micro:bit output demo: string, number, icon, and custom LED pattern
```

## Step 2 – Show a String

From the ``||basic:Basic||`` category, drag a ``||basic:show string||`` block into the workspace.  
Replace the text with a message of your choice (like `"Hello!"` or `"Hi Team"`).  
Add a comment above the block:  
`// Display a greeting message`

```typescript
// micro:bit output demo: string, number, icon, and custom LED pattern
// Display a greeting message
basic.showString("Hi team")
```

## Step 3 – Show a Number

From ``||basic:Basic||``, drag in a ``||basic:show number||`` block.  
Use any number, or use a variable if you want (e.g., `let age = 16`).  
Comment the block:  
`// Show a number (can be from a variable)`

```typescript
// micro:bit output demo: string, number, icon, and custom LED pattern
// Display a greeting message
basic.showString("Hi team")

// Show a number (can be from a variable)
basic.showNumber(16)
```

## Step 4 – Show a Built-in Icon

Drag a ``||basic:show icon||`` block from ``||basic:Basic||`` and choose any icon (e.g., Heart, Happy).  
Add a comment:  
`// Display a built-in icon`

```typescript
// micro:bit output demo: string, number, icon, and custom LED pattern
// Display a greeting message
basic.showString("Hi team")

// Show a number (can be from a variable)
basic.showNumber(16)

// Display a built-in icon
basic.showIcon(IconNames.Happy)
```

## Step 5 – Show a Custom LED Pattern

Add a ``||basic:show leds||`` block from ``||basic:Basic||`` and design your own pattern.  
Examples: a letter, shape, or symbol using the 5x5 LED grid.  
Add a comment:  
`// Display a custom LED pattern`

```typescript
// micro:bit output demo: string, number, icon, and custom LED pattern
// Display a greeting message
basic.showString("Hi team")

// Show a number (can be from a variable)
basic.showNumber(16)

// Display a built-in icon
basic.showIcon(IconNames.Happy)

// Display a custom LED pattern
basic.showLeds(`
    # . # . #
    . # # # .
    # # # # # 
    . # # # .
    # . # . #
`)
```

## Step 6 – Test Your Code

Press the **Play** button to test your program in the **simulator**.
Make sure each output appears in the correct order.

## Step 7 – Download to micro:bit

Click ``|Download|`` and transfer the file to your micro:bit.
Test it by connecting your micro\:bit and watching your outputs appear on the device.

## Step 8 – Notebook Reflection

In your notebook, answer the following reflection prompts:

1. What are the **four output types** you used in this program?
2. How does the micro:bit's **LED screen** differ from other output methods you've used (like console output or GUIs)?
3. Why is it important to **comment** your code?
4. Optional: What would you add next to make your output more interactive?


* for PXT/microbit
<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>
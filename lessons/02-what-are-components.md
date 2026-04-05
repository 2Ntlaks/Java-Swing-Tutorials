## Part 2: What Are Components?

## Introduction

In Part 1, you built an empty Swing `JFrame`. A blank window appeared on your screen with nothing inside it. That window is your foundation, but on its own it is not very useful.

To build a real application, you need to place things inside the window. Things like text, buttons, text fields, and menus. In Java Swing, these things are called **components**.

Before we start adding components to our frame, let us take a step back and understand what they are and how they work. This part is a theory lesson. There is no new code to write. The goal is to give you the big picture so that when we start building in the next parts, everything makes sense.

---

## What is a Component?

A component is a ready-made building block that Swing provides for creating graphical user interfaces. Every element you see and interact with in a desktop application is a component.

Think about the apps you use every day. When you see a piece of text on screen, that is a component. When you click a button, that is a component. When you type into a text field, that is a component. Swing gives you Java classes for all of these, and you simply create them and add them to your window.

The word "component" just means a part of something. A Swing component is a part of your GUI. You assemble multiple components together inside a `JFrame` to build a complete interface.

---

## Common Swing Components

Here are the most common Swing components you will work with in this series. You do not need to memorize them right now. This is just a preview so you know what is available.

| Component | What It Does |
|---|---|
| `JLabel` | Displays text or an image on the screen. The user cannot interact with it. |
| `JButton` | A clickable button. You can make it trigger an action when clicked. |
| `JTextField` | A single-line text input where the user can type. |
| `JTextArea` | A multi-line text input for longer text. |
| `JCheckBox` | A small box the user can check or uncheck. |
| `JComboBox` | A dropdown menu that lets the user pick from a list of options. |
| `JPanel` | An invisible container used to group other components together. |

Each of these is a Java class in the `javax.swing` package, just like `JFrame`. You will notice they all start with the letter "J". This is a Swing naming convention that makes them easy to recognize.

---

## How Components Work

Every component in Swing follows the same basic pattern. You create it, then you add it to the frame. That is it.

The pattern looks like this:

~~~
Step 1: Create the component
Step 2: Add it to the frame using this.add()
~~~

For example, if you wanted to add a label to your window, the thinking would be:

~~~
Step 1: Create a JLabel
Step 2: Add the JLabel to the frame
~~~

If you wanted to add a button, the thinking would be:

~~~
Step 1: Create a JButton
Step 2: Add the JButton to the frame
~~~

The pattern stays the same no matter which component you are working with. Once you learn how to add one component, you know how to add any component. The only difference is which class you use and how you configure it.

> **Note:** We will write the actual Java code for this in the next parts. For now, just understand the two-step pattern: create, then add.

---

## What is a Layout Manager?

There is one more concept to be aware of before we start building.

When you add a single component to a frame, it appears on screen without any issues. But what happens when you add two components? Or five? Or ten? Something needs to decide **where** each component goes inside the window.

That "something" is called a **layout manager**. A layout manager is an object that controls how components are arranged inside a container like a `JFrame` or a `JPanel`.

Swing provides several layout managers, and each one arranges components differently. Some place them left to right, some place them in a grid, and some let one component fill the entire space.

We will not go deep into layout managers right now. You will experience the problem firsthand in a later part when you try to add multiple components and things do not appear the way you expect. Then you will learn how to fix it with a layout manager.

For now, just know that layout managers exist and that they control the positioning of your components.

---

## The Big Picture

Here is how everything connects:

A **JFrame** is your window. It is the outermost container.

**Components** are the building blocks you place inside the window. Labels, buttons, text fields, and more.

A **layout manager** controls how those components are arranged inside the window.

In the next parts, we will start putting this into practice. You will add your first component to the empty frame you built in Part 1, and you will see it appear on screen.

---

## Key Takeaways

- Every visual element in a Swing application is a component.
- Swing components are Java classes in the `javax.swing` package, and they all start with the letter "J".
- Adding a component to a frame always follows two steps: create it, then add it with `this.add()`.
- A layout manager controls where components are positioned inside the window.
- You do not need to memorize every component right now. You will learn them one at a time in the parts that follow.

---

## What's Next

In Part 3, you will add your first component to the empty frame you built in Part 1. You will use a `JLabel` to display text on the screen. It is the simplest component in Swing, and it will be the first time you see something appear inside your window.

---

*End of Part 2 -- What Are Components?*

*Next: [Part 3 -- Adding Text with JLabel](03-adding-text-with-jlabel.md)*

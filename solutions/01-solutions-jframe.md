# 01 - Solutions: JFrame

Lesson reference: [Part 1 - Your First Window](../lessons/01-your-first-window.md)

Use the lesson first, then come back here to compare your answers.

## Base Program

~~~java
package javaswing_01;

import javax.swing.JFrame;

public class JavaSwing_01 extends JFrame
{
    public JavaSwing_01()
    {
        this.setSize(400, 400);
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        this.setVisible(true);
    }

    public static void main(String[] args)
    {
        new JavaSwing_01();
    }
}
~~~

## Exercise Solutions

### Exercise 1

Your result should be a blank `400 x 400` window.

### Exercise 2

Change the size line:

~~~java
this.setSize(800, 600);
~~~

Then try:

~~~java
this.setSize(200, 200);
~~~

The first number is width. The second is height.

### Exercise 3

Add this before `this.setVisible(true);`:

~~~java
this.setTitle("My First Swing App");
~~~

The title appears in the window title bar.

### Exercise 4

If you remove:

~~~java
this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
~~~

the window closes, but the program usually keeps running in the IDE. That is why this line is important.

### Exercise 5

If you remove:

~~~java
this.setVisible(true);
~~~

the program runs, but no window appears because the frame is still invisible.

### Exercise 6

Add:

~~~java
this.setResizable(false);
~~~

Now the user cannot drag the edges of the window to resize it.

### Exercise 7

Add this before `this.setVisible(true);`:

~~~java
this.setLocationRelativeTo(null);
~~~

This centers the window on the screen.

### Exercise 8

We call `this.setVisible(true)` last so the window is fully configured before it appears. If you call it too early, the frame may appear before its size, title, location, or components are ready.

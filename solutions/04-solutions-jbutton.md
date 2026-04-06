# 04 - Solutions: JButton

Lesson reference: [Part 4 - Adding Buttons with JButton](../lessons/04-adding-buttons-with-jbutton.md)

## Base Program

~~~java
package javaswing_04;

import javax.swing.JFrame;
import javax.swing.JButton;

public class JavaSwing_04 extends JFrame
{
    public JavaSwing_04()
    {
        JButton button1 = new JButton("Click Me");
        this.add(button1);

        this.setSize(400, 400);
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        this.setVisible(true);
    }

    public static void main(String[] args)
    {
        new JavaSwing_04();
    }
}
~~~

## Exercise Solutions

### Exercise 1

Your window should show one button with the text `Click Me`.

### Exercise 2

Change the button text:

~~~java
JButton button1 = new JButton("Submit");
~~~

You can replace `"Submit"` with `"OK"`, `"Cancel"`, or `"Save"`.

### Exercise 3

A clearer variable name:

~~~java
JButton submitButton = new JButton("Submit");
this.add(submitButton);
~~~

### Exercise 4

If you remove `this.add(button1);`, the button will not appear because it was never placed inside the frame.

### Exercise 5

Example:

~~~java
JButton button1 = new JButton("");
~~~

An empty button still appears, but without text. A long string makes the button wider.

### Exercise 6

Example:

~~~java
package javaswing_04;

import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.JButton;

public class JavaSwing_04 extends JFrame
{
    public JavaSwing_04()
    {
        JLabel label1 = new JLabel("Hello");
        this.add(label1);

        JButton button1 = new JButton("Click Me");
        this.add(button1);

        this.setSize(400, 400);
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        this.setVisible(true);
    }

    public static void main(String[] args)
    {
        new JavaSwing_04();
    }
}
~~~

Only one component appears because the default `BorderLayout` puts both into the center area. This leads directly into [Part 5](../lessons/05-the-layout-problem.md).

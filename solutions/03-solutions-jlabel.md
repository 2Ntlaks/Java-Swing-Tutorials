# 03 - Solutions: JLabel

Lesson reference: [Part 3 - Adding Text with JLabel](../lessons/03-adding-text-with-jlabel.md)

## Base Program

~~~java
package javaswing_03;

import javax.swing.JFrame;
import javax.swing.JLabel;

public class JavaSwing_03 extends JFrame
{
    public JavaSwing_03()
    {
        JLabel label1 = new JLabel("Welcome to Java Swing!");
        this.add(label1);

        this.setSize(400, 400);
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        this.setVisible(true);
    }

    public static void main(String[] args)
    {
        new JavaSwing_03();
    }
}
~~~

## Exercise Solutions

### Exercise 1

Your window should show the text:

~~~java
"Welcome to Java Swing!"
~~~

### Exercise 2

Example:

~~~java
JLabel label1 = new JLabel("My name is Ntlakanipho");
~~~

### Exercise 3

If you use:

~~~java
JLabel label1 = new JLabel("");
~~~

the label is still there, but it displays no visible text. A longer sentence makes the label wider.

### Exercise 4

If you remove:

~~~java
this.add(label1);
~~~

the label is created in memory but never added to the frame, so it does not appear.

### Exercise 5

If you add the label after `this.setVisible(true);`, the label may still appear, but this is poor practice. It is better to add components before making the window visible.

### Exercise 6

Add:

~~~java
this.setTitle("JLabel Demo");
~~~

The title is shown in the title bar, while the `JLabel` text appears inside the content area.

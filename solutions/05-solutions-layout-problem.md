# 05 - Solutions: Layout Problem

Lesson reference: [Part 5 - The Layout Problem](../lessons/05-the-layout-problem.md)

## Exercise Solutions

### Exercise 1

If you add the label first and the button second, only the button appears.

If you reverse the order, only the label appears.

Reason: both components are being added to `BorderLayout.CENTER`, and the last one replaces the previous one.

### Exercise 2

If you add:

1. `JLabel`
2. `JButton`
3. another `JLabel`

only the third component appears. The last component added to the center wins.

### Exercise 3

Example solution:

~~~java
package javaswing_05;

import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.JButton;
import java.awt.BorderLayout;

public class JavaSwing_05 extends JFrame
{
    public JavaSwing_05()
    {
        JLabel label1 = new JLabel("Hello, Student!");
        this.add(label1, BorderLayout.NORTH);

        JButton button1 = new JButton("Click Me");
        this.add(button1, BorderLayout.CENTER);

        this.setSize(400, 400);
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        this.setVisible(true);
    }

    public static void main(String[] args)
    {
        new JavaSwing_05();
    }
}
~~~

Now both components appear because they are in different regions.

### Exercise 4

Example:

~~~java
package javaswing_05;

import javax.swing.JFrame;
import javax.swing.JButton;
import java.awt.BorderLayout;

public class JavaSwing_05 extends JFrame
{
    public JavaSwing_05()
    {
        this.add(new JButton("North"), BorderLayout.NORTH);
        this.add(new JButton("South"), BorderLayout.SOUTH);
        this.add(new JButton("East"), BorderLayout.EAST);
        this.add(new JButton("West"), BorderLayout.WEST);
        this.add(new JButton("Center"), BorderLayout.CENTER);

        this.setSize(400, 400);
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        this.setVisible(true);
    }

    public static void main(String[] args)
    {
        new JavaSwing_05();
    }
}
~~~

### Exercise 5

`this.add(label1);` and `this.add(button1);` both use the center region by default. Since `BorderLayout.CENTER` only holds one component, the button replaces the label. To make both visible, you must either use different `BorderLayout` regions or switch to another layout manager like [FlowLayout](../lessons/06-flowlayout.md).

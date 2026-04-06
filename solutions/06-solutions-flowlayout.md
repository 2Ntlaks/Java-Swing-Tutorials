# 06 - Solutions: FlowLayout

Lesson reference: [Part 6 - FlowLayout](../lessons/06-flowlayout.md)

## Exercise Solutions

### Exercise 1

Use the lesson's first program. The important line is:

~~~java
this.setLayout(new FlowLayout());
~~~

That allows both the label and button to appear.

### Exercise 2

Example:

~~~java
this.setLayout(new FlowLayout());

this.add(new JButton("One"));
this.add(new JButton("Two"));
this.add(new JButton("Three"));
this.add(new JButton("Four"));
this.add(new JButton("Five"));
~~~

When the window gets narrow, the buttons wrap onto the next row.

### Exercise 3

Example:

~~~java
this.setLayout(new FlowLayout(FlowLayout.LEFT));
~~~

or:

~~~java
this.setLayout(new FlowLayout(FlowLayout.RIGHT));
~~~

`LEFT` keeps the components against the left side. `RIGHT` keeps them against the right side.

### Exercise 4

If you remove:

~~~java
this.setLayout(new FlowLayout());
~~~

the old layout problem returns because the frame goes back to its default `BorderLayout`.

### Exercise 5

Example:

~~~java
this.setLayout(new FlowLayout());

this.add(new JLabel("First"));
this.add(new JButton("A"));
this.add(new JLabel("Second"));
this.add(new JButton("B"));
this.add(new JLabel("Third"));
~~~

With `FlowLayout`, the components appear in the same order you add them.

### Exercise 6

Example:

~~~java
this.setLayout(new FlowLayout(FlowLayout.CENTER, 20, 20));
~~~

The second number is the horizontal gap. The third is the vertical gap.

Smaller numbers make components closer together. Larger numbers spread them out.

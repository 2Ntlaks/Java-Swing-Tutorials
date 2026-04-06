# 07 - Solutions: Event Handling

Lesson reference: [Part 7 - Event Handling: Button Clicks](../lessons/07-event-handling-button-clicks.md)

## Exercise Solutions

### Exercise 1

Use the one-button example from the lesson. Clicking `Save` should:

- change the label to `Saved!`
- print `Saved!` in the console

### Exercise 2

Use the two-button example from the lesson. Each button should update the label and console with its own message.

### Exercise 3

Add a reset button:

~~~java
JButton resetButton;
~~~

Inside the constructor:

~~~java
resetButton = new JButton("Reset");
resetButton.addActionListener(this);
this.add(resetButton);
~~~

Inside `actionPerformed`:

~~~java
if (event.getSource() == resetButton)
{
    messageLabel.setText("Welcome!");
    System.out.println("Reset!");
}
~~~

### Exercise 4

If you remove:

~~~java
saveButton.addActionListener(this);
~~~

clicking the save button does nothing because no listener is connected to it.

### Exercise 5

Example structure:

~~~java
JLabel messageLabel;
JButton happyButton;
JButton sadButton;
JButton excitedButton;
JButton calmButton;
~~~

Inside `actionPerformed`:

~~~java
if (event.getSource() == happyButton)
{
    messageLabel.setText("I am happy!");
    System.out.println("I am happy!");
}

if (event.getSource() == sadButton)
{
    messageLabel.setText("I am sad!");
    System.out.println("I am sad!");
}

if (event.getSource() == excitedButton)
{
    messageLabel.setText("I am excited!");
    System.out.println("I am excited!");
}

if (event.getSource() == calmButton)
{
    messageLabel.setText("I am calm!");
    System.out.println("I am calm!");
}
~~~

### Exercise 6

If `messageLabel` is declared only inside the constructor, `actionPerformed` cannot access it. You will get a scope error because local variables belong only to the method where they were created.

That is why the lesson declares components at class level when multiple methods need them.

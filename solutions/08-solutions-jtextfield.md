# 08 - Solutions: JTextField

Lesson reference: [Part 8 - JTextField](../lessons/08-jtextfield.md)

## Exercise Solutions

### Exercise 1

Use the greeting example from the lesson. Typing a name and clicking `Greet` should update the label and print the same message in the console.

### Exercise 2

Add this line inside `actionPerformed` after reading the text:

~~~java
nameField.setText("");
~~~

This clears the field after the greeting is shown.

### Exercise 3

Example:

~~~java
nameField = new JTextField("Type here", 20);
~~~

The default text appears inside the field. If the user deletes it and types something else, `getText()` returns the new text.

### Exercise 4

Examples:

~~~java
nameField = new JTextField(5);
nameField = new JTextField(40);
~~~

Changing the number changes the visible width only. It does not limit how many characters the user can type.

### Exercise 5

Example:

~~~java
JLabel firstNameLabel;
JLabel lastNameLabel;
JTextField firstNameField;
JTextField lastNameField;
JButton greetButton;
JLabel messageLabel;
~~~

Inside `actionPerformed`:

~~~java
String first = firstNameField.getText();
String last = lastNameField.getText();

messageLabel.setText("Hello, " + first + " " + last + "!");
System.out.println("Hello, " + first + " " + last + "!");
~~~

### Exercise 6

Example:

~~~java
String firstNumber = firstField.getText();
String secondNumber = secondField.getText();

int a = Integer.parseInt(firstNumber);
int b = Integer.parseInt(secondNumber);
int result = a + b;

messageLabel.setText("Result: " + result);
System.out.println("Result: " + result);
~~~

Full event logic:

~~~java
if (event.getSource() == addButton)
{
    int a = Integer.parseInt(firstField.getText());
    int b = Integer.parseInt(secondField.getText());
    int result = a + b;

    messageLabel.setText("Result: " + result);
    System.out.println("Result: " + result);
}
~~~

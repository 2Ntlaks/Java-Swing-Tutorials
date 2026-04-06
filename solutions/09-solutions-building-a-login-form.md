# 09 - Solutions: Building a Login Form

Lesson reference: [Part 9 - Building a Login Form](../lessons/09-building-a-login-form.md)

## Exercise Solutions

### Exercise 1

Use the complete login form from the lesson. The expected test results are:

- `admin` and `1234` -> `Login successful!`
- anything else -> `Invalid username or password.`

### Exercise 2

Add a third button:

~~~java
JButton exitButton;
~~~

Inside the constructor:

~~~java
exitButton = new JButton("Exit");
exitButton.addActionListener(this);
this.add(exitButton);
~~~

Inside `actionPerformed`:

~~~java
if (event.getSource() == exitButton)
{
    System.out.println("Application closed.");
    System.exit(0);
}
~~~

### Exercise 3

Add this inside the clear-button block:

~~~java
usernameField.requestFocus();
~~~

Now the cursor returns to the username field after clearing.

### Exercise 4

Add an instance variable:

~~~java
int attempts = 0;
~~~

Update the failed-login block:

~~~java
attempts++;

if (attempts >= 3)
{
    messageLabel.setText("Too many failed attempts.");
    loginButton.setEnabled(false);
    System.out.println("Too many failed attempts.");
}
else
{
    messageLabel.setText("Invalid credentials. Attempts: " + attempts);
    System.out.println("Invalid credentials. Attempts: " + attempts);
}
~~~

### Exercise 5

Use `if` and `else if`:

~~~java
if (username.equals("admin") && password.equals("1234"))
{
    messageLabel.setText("Welcome, Admin!");
    System.out.println("Welcome, Admin!");
}
else if (username.equals("student") && password.equals("5678"))
{
    messageLabel.setText("Welcome, Student!");
    System.out.println("Welcome, Student!");
}
else
{
    messageLabel.setText("Invalid username or password.");
    System.out.println("Login failed. Username: " + username);
}
~~~

### Exercise 6

Suggested components:

- `firstNameLabel`
- `lastNameLabel`
- `emailLabel`
- `passwordLabel`
- `firstNameField`
- `lastNameField`
- `emailField`
- `passwordField`
- `registerButton`
- `clearButton`
- `messageLabel`

Core register logic:

~~~java
String firstName = firstNameField.getText();
String lastName = lastNameField.getText();
String email = emailField.getText();

String message = "Registered: " + firstName + " " + lastName + ", " + email;
messageLabel.setText(message);
System.out.println(message);
~~~

Core clear logic:

~~~java
firstNameField.setText("");
lastNameField.setText("");
emailField.setText("");
passwordField.setText("");
messageLabel.setText("Enter your details.");
~~~

This exercise is a strong extension of the login-form lesson because it uses the same building blocks with a different goal.

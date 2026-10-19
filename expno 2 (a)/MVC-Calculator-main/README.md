MVC Calculator

A simple Calculator Application in Java developed using the MVC (Model-View-Controller) Architecture and Java Swing.

📌 Project Description

This project is a basic calculator that performs four mathematical operations:

Addition
Subtraction
Multiplication
Division

The project follows the MVC architecture, which separates the application into three parts: Model, View, and Controller.

🏗️ MVC Architecture
1. Model – ModelsCalculator.java

The Model contains the calculation logic.

It performs:

Addition
Subtraction
Multiplication
Division
2. View – ViewsCalculator.java

The View provides the graphical user interface (GUI) using Java Swing.

It contains:

First Number input field
Second Number input field
Addition button
Subtraction button
Multiplication button
Division button
Result field
3. Controller – ControllerCalculator.java

The Controller handles user actions.

It:

Detects which button was clicked
Gets numbers from the View
Calls the appropriate Model method
Displays the result in the View
4. Run – RunCalculator.java

This class contains the main() method and starts the Calculator application.

📂 Project Structure
MVC-Calculator/
│
├── ModelsCalculator.java
├── ViewsCalculator.java
├── ControllerCalculator.java
├── RunCalculator.java
└── README.md
⚙️ Technologies Used
Java
Java Swing
MVC Architecture
Object-Oriented Programming
▶️ How to Run
Clone or download this repository.
Open the project in VS Code, IntelliJ IDEA, or Eclipse.
Make sure Java/JDK is installed.
Compile the Java files.
Run RunCalculator.java.
Enter two numbers and select an operation.
🧮 Operations
Button	Operation
+	Addition
-	Subtraction
*	Multiplication
/	Division
🎯 Purpose

The main purpose of this project is to understand the MVC design pattern, Java Swing GUI development, event handling, and separation of application logic.

👩‍💻 Author

Neha

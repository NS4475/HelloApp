# Use Case 1: Print a basic greeting in the console

* **Description:** A foundational setup that creates the main application class and prints a simple "Hello World" string to the console.
* **Disadvantages of previous use case:** N/A (This is the initial baseline).
* **Preconditions:** Java Development Kit (JDK) installed and Maven project structure configured.
* **Main Flow:** Program execution begins -> enters the `main` method -> `System.out.println` executes -> program terminates.
* **Post Conditions:** The text "Hello World" is visible in the standard console output.
* **Hints:** Utilize the standard `System.out.println()` method for basic console output.
* **Code Snippets Examples:** `System.out.println("Hello World");`
* **Concepts Learned:** Project architecture, standard application entry points (`public static void main`), and basic standard output.


# Use Case 2: Display "Hello" with Command-Line Argument

* **Description:** The app accepts a user's name as a command-line argument and displays a personalized greeting. This enhances the basic functionality of UC1 by allowing user input to customize the output.
* **Disadvantages of Previous Use Case:** UC1 is limited because it only displays a static message. To make the application more interactive and useful, it should accept user input and personalize the output based on that input.
* **Preconditions:** App is launched with a command-line argument containing a name.
* **Main Flow:**
  1. User runs the application with a name argument: `java HelloApp John`
  2. App reads the name from the `args[0]` parameter
  3. App displays "Hello, John!" to the console
  4. App terminates
* **Postconditions:** Personalized greeting is displayed based on the command-line argument provided.



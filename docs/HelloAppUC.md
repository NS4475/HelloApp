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


# Use Case 3: Display "Hello" with Command-Line Argument or Default Message

* **Description:** The app accepts a user's name as a command-line argument and displays a personalized greeting. If no name is provided, it defaults to "World". This use case combines the basic functionality from UC1 with the personalization from UC2, adding robustness through default handling.
* **Disadvantages of Previous Use Case:** UC2 requires a command-line argument to work correctly. If the user runs the program without providing an argument, the application will crash with an `ArrayIndexOutOfBoundsException`. This makes the program fragile and less user-friendly. UC3 addresses this limitation by providing a sensible default value when no argument is supplied.
* **Preconditions:** App is launched with or without a command-line argument.
* **Main Flow:** 1. User runs the application with or without a name argument: `java HelloApp John` or `java HelloApp`
  2. App checks if a command-line argument was provided
  3. If an argument exists, app reads the name from `args[0]`
  4. If no argument exists, app uses the default value "World"
  5. App displays the personalized greeting
  6. App terminates
* **Postconditions:** Personalized greeting is displayed with either the provided name or the default "World".
* **Hints:** Check the length of the `args` array before accessing elements. Use an if-else statement or ternary operator to assign the name based on argument availability. Test with and without command-line arguments to ensure both paths work correctly.
* **Code Snippets Examples:** `String name = (args.length > 0) ? args[0] : "World";`
* **Concepts Learned:** Conditional Logic, Ternary Operator, Array Length Checking, Default Values, Defensive Programming, String Concatenation, and Program Flexibility.



# CHATBOX
*SimpleChatbot Documentation*

*Introduction:*
SimpleChatbot is a Java program designed to interact with users through a text-based interface.
It responds to specific keywords and phrases entered by the user, providing appropriate responses. 
This documentation provides a detailed explanation of the code structure, functionality, and usage guidelines.


*Installation:*
No installation is required for SimpleChatbot.
The program can be run directly from any Java development environment that supports console applications.


*Usage:*
1. Compile the SimpleChatbot.java file using a Java compiler.
2. Run the compiled program using the Java Virtual Machine (JVM).
3. Enter text-based queries or commands when prompted by the program.
4. Interact with the chatbot by typing messages and receiving responses.


*Code Explanation:*
The SimpleChatbot program consists of a single Java class with a main method that serves as the entry point for the application.
Here's an overview of the code structure:

- *Imports:* The program imports the Scanner class from the java.util package to enable user input via the console.

- *Main Method:* The main method initializes a Scanner object to read user input from the console.
- It displays a welcome message and enters a while loop to continuously interact with the user.

- *Interaction Loop:* Within the loop, the program reads user input, converts it to lowercase for easier matching, and checks for specific keywords using conditional statements (if-else). Based on the input, the program provides corresponding responses or prompts the user to rephrase if the input is not recognized.

- *Exit Condition:* If the user enters a farewell message (e.g., "bye"), the program prints a goodbye message and breaks out of the loop, ending the conversation.

- *Scanner Closure:* Finally, the program closes the Scanner object to release system resources.


*Execution Illustrations:*
 images are included in this documentation, but screenshots or recordings of the program's execution can be provided separately to illustrate the user interaction process.


*Troubleshooting:*
- Ensure that the Java development environment is properly configured and the SimpleChatbot.java file is compiled without errors.
- Check for typos or syntax errors in user input to avoid unrecognized commands or responses.
- If the program freezes or becomes unresponsive, check for infinite loops or logical errors in the code.



*Conclusion:*
SimpleChatbot is a basic Java program that demonstrates how to create a text-based chatbot using simple keyword matching. 
It provides a starting point for building more sophisticated chatbots with additional features and natural language processing capabilities.



By following the usage guidelines and understanding the code structure, users can interact with the chatbot and customize its behavior according to their requirements.


###CODE###


import java.util.Scanner;

public class SimpleChatbot {
    
    public static void main(String[] args)
    {
        Scanner scanner = new Scanner(System.in); // Create a scanner object to read user input from the console
        System.out.println("Hello! I'm a simple chatbot. How can I assist you?"); // Display a welcome message
        
        // Main interaction loop
        while (true)
        {
            String input = scanner.nextLine().toLowerCase(); // Read user input and convert it to lowercase for easier matching
            
            // Check for specific keywords in the input and provide corresponding responses
            if (input.contains("hello") || input.contains("hi")) {
                System.out.println("Hello there! How can I help you?"); // Respond to greetings
            } 
            else if (input.contains("how are you"))
            {
                System.out.println("I'm just a program, so I don't have feelings, but thanks for asking!"); // Respond to inquiries about the bot's well-being
            } 
            else if (input.contains("bye"))
            {
                System.out.println("Goodbye! Have a great day!"); // Respond to farewell messages and exit the conversation loop
                break; // Exit the loop and end the conversation
            }
            else {
                // If no specific keyword is matched, provide a default response
                System.out.println("I'm sorry, I didn't understand that. Can you please rephrase?");
            }
        }
        
        scanner.close(); // Close the scanner to release system resources
    }
}


program images :
![Screenshot 2024-03-18 122441](https://github.com/potnurukrishnarao/CHATBOX/assets/163103947/0ae4592c-a9ef-4ea6-ae51-4e47784332a0)


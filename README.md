Overview
This project demonstrates how to perform API testing using TestNG and RestAssured for validating APIs. The primary goal of this project is to implement temporary solutions, reduce technical debt, and isolate problematic code while performing API tests. It uses the JSONPlaceholder API to perform basic GET and POST requests and incorporates best practices for API testing.
Project Setup
Prerequisites
Before running the tests, ensure you have the following installed on your system:

Java 8 or higher
Maven
IDE (e.g., Eclipse, IntelliJ IDEA)
Steps to Set Up the Project
Clone the Repository
Clone the project repository to your local machine:

git clone <repository-url>
Import into IDE
Open your IDE (Eclipse, IntelliJ, etc.), and import the project as a Maven Project.

Install Dependencies
Maven will automatically download the necessary dependencies for TestNG, RestAssured, and any other libraries specified in the pom.xml file.

Project Structure
src/
│
├── main/
│   └── java/
│       └── com/example/api/
│           └── ApiTest.java        # Test cases for API requests
│
└── test/
    └── java/
        └── com/example/api/
            └── ApiTest.java        # TestNG Test cases
testng.xml                       # TestNG configuration file
pom.xml                           # Maven dependencies and build configuration
README.md                         # Project Documentation
How to Run the Tests
Running Tests via IDE (e.g., Eclipse or IntelliJ)
Right-click on the testng.xml file.
Choose Run As > TestNG Suite.
This will execute all the test methods defined in the testng.xml configuration file.

Running Tests via Command Line
You can also run the tests via Maven from the command line:

Navigate to the project directory.
Execute the following command:
mvn test
This command will trigger Maven to run the tests specified in the project.

Test Cases
ApiTest.java
testGetRequest(): Sends a GET request to a sample API (https://jsonplaceholder.typicode.com/posts/1) and verifies the response status code.
testAllPosts(): Sends a GET request to fetch all posts and checks the response status and body size.
testPostRequest(): Sends a POST request to create a new post and verifies that the creation was successful.
Sample Output
After running the tests, you will see the following output:

[INFO] Scanning for projects...
[INFO] ------------------------------------------------------------------------
[INFO] Building API Testing Project 1.0-SNAPSHOT
[INFO] ------------------------------------------------------------------------
[INFO] 
[INFO] --- maven-surefire-plugin:2.22.2:test (default-test) @ api-testing-project ---
[INFO] 
[INFO] Results:
[INFO] 
[INFO] Tests run: 3, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 1.234 sec - in TestNG suite
[INFO] 
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
Documentation
Temporary Solutions
The current tests focus on verifying basic functionality, such as status code validation. In the future, we plan to extend these tests to validate response bodies, error handling, and implement data-driven testing.
Technical Debt
Some tests, such as the POST request test, are currently basic and lack full validation and error handling. These aspects are noted for future improvements.
Future Enhancements
Validate response bodies with more detailed assertions.
Implement more test scenarios for different API endpoints.
Introduce parameterized or data-driven tests for better coverage.
Contributing
Feel free to fork this project, submit issues, and make pull requests for improvements.

License
This project is licensed under the MIT License - see the LICENSE file for details.

This README covers the project setup, how to run tests, and includes necessary documentation for understanding the project, including technical debts and plans for future improvements. Adjust the repository URL and any other specific details according to your project.







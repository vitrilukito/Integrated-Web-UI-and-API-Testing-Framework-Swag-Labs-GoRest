# Integrated Web UI and API Testing Framework: Swag Labs & GoRest

This repository contains two automation tests:
- **First**: the web UI automation test project for [Swag Labs](https://www.saucedemo.com/) e-commerce website. It is built using Cucumber, WebDriverManager, and Selenium, and aims to ensure the functionality of the login page, product page, checkout page, and cart. The repository includes source code for the project, POM implementation, Gherkin test cases, and Cucumber implementation, along with sample test cases.
- **Second**: the API automation test project for Gorest. It is built to test the [Gorest API](https://www.gorest.co.in/) using positive test cases, negative test cases, and boundary tests. It leverages various dependencies like RestAssured, Cucumber, Assertion, JSON and JSONSchemaValidator for API testing and validation.

Both projects are written in Java programming language, using the JUnit testing framework and Gradle as the build tool.

## Table of Contents

- Technologies Used
- Project Structure
- Requirements
- Dependencies
- Installation
- Configurations
- Running Tests
- Test Cases

## Technologies Used

- **Java**: The primary programming language for the project.
- **Cucumber**: A testing tool that supports Behavior Driven Development (BDD) for defining test cases in Gherkin syntax.
- **Gradle**: A build automation tool used to manage dependencies and build the project.
- **Selenium**: A web automation tool for interacting with web applications.
- **Rest Assured**: An API automation tool to test and validate RESTful APIs.
- **JSON**: A text-based format for storing and exchanging data in each request in an API.

## Project Structure

### Gorest API Automation Test
Here is the breakdown of the project structure:
- **api.feature**: The feature file that contains the scenarios to be tested in Gorest API.
- **JSON Schema Data**: Defines the structure and validation rules for JSON objects used in API requests and responses, ensuring data integrity.
- **Endpoint**: The specific URL path for accessing the Gorest API, enabling interaction with resources like users and posts.
- **ApiModel**: Defines the structure and behavior of data objects used in the application. It includes static responses that link API responses to their respective page representations, facilitating smooth integration and data flow between components.
- **ApiUtility**: Contains helper functions and classes that provide common functionality, promoting code reuse and simplifying application logic.
- **ApiPage**: Object-oriented representations of API endpoints or related logic.
- **ApiRunner**: Contains the runner classes for running the Cucumber tests.
- **ApiStep**: Contains the step definitions that link Cucumber steps to actual code logic.


### Swag Labs Web UI Automation Test
Here is the breakdown of the project structure:
- **Login.feature**: Contains scenarios for testing the login functionality, including valid and invalid login attempts.
- **Product.feature**: Tests the product page, such as displaying available products and adding them to the cart.
- **Checkout.feature**: Scenarios that verify the checkout process, handling successful and empty cart scenarios.
- **Cart.feature**: Tests the shopping cart functionalities, including viewing items and removing products.
- **Security.feature**: Ensures that the account is secured and will be automatically logged out after a certain period of inactivity.
- **WebModel**: Encapsulate the interactions with the UI elements on each page, providing methods to perform actions (like clicking buttons, entering text) and verify page content.
- **WebUtility**: This includes classes for managing the WebDriver instance, handling configuration settings, and providing reusable methods for various tasks.
- **WebPage**: Each class defines the elements on the page and the methods that encapsulate interactions with those elements. The methods within these classes are called by step definitions in the Cucumber tests.
- **WebStep**: Contains the step definition classes for Cucumber scenarios. Each class corresponds to a feature file and implements the methods that define how to interact with the web application during testing.
- **CucumberTest**: This is used to generate reports in HTML and JSON files.
- **Hooks**: These are blocks of code that run before or after each scenario. They allow us to set up any preconditions or perform clean-up tasks after tests.

## Requirements

- [Java 8 or above](https://www.oracle.com/java/technologies/javaese-downloads.html)
- [IntelliJ IDEA](https://www.jetbrains.com/idea) or another Java IDE
- [Gradle](https://www.gradle.org/install/) for dependency management and build automation
- [JUnit](https://junit.org/junit5/)
- [RestAssured](https://rest-assured.io/)
- [Maven Repository](https://mvnrepository.com)
- [Cucumber](https:cucumber.io)
- [JSONValidator](https://github.com/json-schema-org./json-schema-validator)
- [Selenium Web Driver](https://www.selenium.dev/documentation/webdriver/)
- Browser: The latest version of Google Chrome with the latest version of the WebDriver installed

## Dependencies

The following dependencies are included in the project:

- testImplementation platform('org.junit:junit-bom:5.10.0')
- testImplementation 'org.junit.jupiter:junit-jupiter'
- testImplementation 'org.junit.vintage:junit-vintage-engine:5.7.2'
- implementation group: 'io.cucumber', name: 'cucumber-java', version: '7.20.1'
- implementation group: 'org.seleniumhq.selenium', name: 'selenium-java', version: '4.27.0'
- testImplementation group: 'junit', name: 'junit', version: '4.13.2'
- testImplementation("io.github.bonigarcia:webdrivermanager:5.9.2")
- testImplementation group: 'io.cucumber', name: 'cucumber-junit', version: '7.20.1'
- testRuntimeOnly 'org.junit.jupiter:junit-jupiter-engine:5.9.0'
- testImplementation group: 'org.assertj', name: 'assertj-core', version: '3.26.3'
- testImplementation 'org.junit.jupiter:junit-jupiter-api:5.8.1'
- testImplementation group: 'io.rest-assured', name: 'rest-assured', version: '5.5.0'
- testImplementation group: 'org.json', name: 'json', version: '20240303'
- implementation group: 'io.rest-assured', name: 'json-schema-validator', version: '5.5.0'


## Installation

1. Clone the repository:
   git clone https://github.com/vitrilukito/Integrated-Web-UI-and-API-Testing-Framework-Swag-Labs-GoRest
2. Open the project in IntelliJ IDEA or your preferred IDE
3. Ensure that Gradle is installed and properly configured in your IDE
4. Run the following Gradle command to download the required dependencies: ./gradlew build

## Configurations

To run this project, make sure you have the following configured:
1. **Java Development Kit (JDK)**: Install JDK 8 or higher on your machine. You can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html) or use [OpenJDK](https://www.openjdk.java.net/install/).
2. **Gradle**: Ensure you have Gradle installed. You can install it following the instructions on the [Gradle website](https://gradle.org/install/).
3. **IntelliJ IDEA**: Use IntelliJ IDEA as your IDE for coding. You can download it from the [JetBrains website](https://jetbrains.com/idea/download/).
4. **Dependencies**: The project uses the following dependencies, which are included in the 'build.gradle' file:
   - JUnit
   - Selenium
   - Cucumber
   - Web Driver Manager
   - Assertion 
   - RestAssured
   - JSON
   - JSONSchemaValidator
  
After setting up these tools, you can run the tests and work on the project.

## Running Tests

You can run the tests in the project using the Gradle wrapper or directly from the IDE.

### Running via IDE

1. Navigate to the Runner class.
2. Right-click the class and select "Run" to execute the Cucumber feature.

### Running via Command Line
1. Use the Gradle command: ./gradlew test

## Test Cases

### Gorest API Automation Test

This project includes a total of 23 test cases categorized into:
- **Positive Test Cases**: Validate the successful execution of API calls with valid inputs.
- **Negative Test Cases**: Verify the API's behavior with invalid inputs or missing required fields.
- **Boundary Test Cases**: Ensure correct handling of boundary values (e.g., maximum and minimum limits).

- **Positive Test Cases**: Validate the successful execution of the GET, POST, PUT, and DELETE requests.

**Sample of positive test case:**


<img width="622" alt="image" src="https://github.com/user-attachments/assets/1e50c7e6-b7e8-4240-982f-45ae6831567e" />



**Step Definitions:**
Here are the step definitions that implement the above test case:


<img width="539" alt="image" src="https://github.com/user-attachments/assets/74a08bee-c1e7-4985-9787-128315cc51a6" />




**Page Object:**
The WebPage class of the above test case is as below:


<img width="551" alt="image" src="https://github.com/user-attachments/assets/cae3d6ad-6a9a-4c7a-9577-b775819e442e" />


<img width="672" alt="image" src="https://github.com/user-attachments/assets/952b1afa-ed38-452e-bc5b-96b40184b5c0" />




- **Negative Test Cases**: Verify the API's behavior with invalid inputs, invalid usernames, or missing required fields.

**Sample of negative test case:**


<img width="729" alt="image" src="https://github.com/user-attachments/assets/b0d7cad8-14d0-47a0-a6a0-eb114c0c3880" />




**Step Definitions:**
Here are the step definitions that implement the above test case:


<img width="597" alt="image" src="https://github.com/user-attachments/assets/a54c79f0-357b-487b-8f18-14c88ecc9f86" />



**Page Object:**
The WebPage class of the above test case is as below:


<img width="599" alt="image" src="https://github.com/user-attachments/assets/fa05ca10-5581-42df-a261-66d6904f9fb1" />




- **Boundary Test Cases**: Explore the boundaries of input domains for APIs, including the valid and invalid values.

**Sample of boundary test case:**


<img width="671" alt="image" src="https://github.com/user-attachments/assets/20131caa-1d4e-4638-bc18-7d4888db31cf" />



**Step Definitions:**
Here are the step definitions that implement the above test case:


<img width="592" alt="image" src="https://github.com/user-attachments/assets/20407fea-3e8c-47db-a630-db08530281d7" />

<img width="512" alt="image" src="https://github.com/user-attachments/assets/193142d9-b67f-4770-8f8d-ac559575c682" />



**Page Object:**
The WebPage class of the above test case is as below:


<img width="627" alt="image" src="https://github.com/user-attachments/assets/4181098e-92c6-42d6-b157-36dff5673eac" />

<img width="514" alt="image" src="https://github.com/user-attachments/assets/0f51a26b-5ad7-4b8e-957a-4c5f689a305e" />



You can view all the test cases in the [api.feature file](src/test/resources/apiFeatures/api.feature).


### Swag Labs Web UI Automation Project

This project includes a total of 5 pages and 50 test cases categorized into:
- **Positive Test Cases**: Validate the successful execution of login page, product page, checkout page, cart, and security with valid inputs.

**Sample of positive test case:**


<img width="438" alt="image" src="https://github.com/user-attachments/assets/a40c7e66-40b6-4164-b92c-1702ff9f37d7" />


**Step Definitions:**
Here are the step definitions that implement the above test case:


<img width="465" alt="image" src="https://github.com/user-attachments/assets/c506f043-f084-4b46-b3b1-48d95b4fa632" />


**Page Object:**
The WebPage class is used to interact with the login page:


<img width="479" alt="image" src="https://github.com/user-attachments/assets/45c08e2c-ff50-41cf-bbc9-c7ba781e3257" />


- **Negative Test Cases**: Verify the API's behavior with invalid inputs, invalid usernames, or missing required fields.

**Sample of negative test case:**


<img width="583" alt="image" src="https://github.com/user-attachments/assets/f02da3a7-7cdb-4726-8882-b3a4cc53e8fd" />



**Step Definitions:**
Here are the step definitions that implement the above test case:


<img width="494" alt="image" src="https://github.com/user-attachments/assets/8615ee21-8a0d-4299-a90a-f39135f8edcc" />



**Page Object:**
The WebPage class of the above test case is as below:


<img width="576" alt="image" src="https://github.com/user-attachments/assets/c4589ef3-3411-484f-ba6f-4408b249cc1b" />




- **Boundary Test Cases**: Ensure correct handling of boundary values, including invalid inputs.

**Sample of boundary test case:**


<img width="486" alt="image" src="https://github.com/user-attachments/assets/1ef1aba1-f95d-4770-bc24-d9d1177c8f79" />




**Step Definitions:**
Here are the step definitions that implement the above test case:


<img width="486" alt="image" src="https://github.com/user-attachments/assets/e3a0d2cb-353f-4afb-baae-6079ac1d537b" />




**Page Object:**
The WebPage class of the above test case is as below:


<img width="584" alt="image" src="https://github.com/user-attachments/assets/eee5d175-01ce-4c1e-895e-0fc01a4ebbfa" />




The test cases are presented in 5 different files. You can view all the test cases here:
- [Cart.feature](src/test/resources/webFeatures/Cart.feature)
- [Checkout.feature](src/test/resources/webFeatures/Checkout.feature)
- [Login.feature](src/test/resources/webFeatures/Login.feature)
- [Product.feature](src/test/resources/webFeatures/Product.feature)
- [Security.feature](src/test/resources/webFeatures/Security.feature)

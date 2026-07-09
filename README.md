# Demo Web Shop Automation Framework

## Overview

This project is a Selenium WebDriver-based Test Automation Framework developed for automating the Demo Web Shop application using:
* Java
* Selenium WebDriver
* Cucumber BDD
* TestNG
* Maven
* Page Object Model (POM)
* Allure Reports
* Extent Reports
* Apache POI (Excel Data Handling)

The framework follows industry-standard automation practices with reusable page objects, feature-driven development, reporting, and data-driven testing.





## Application Under Test

*Website:* (https://demowebshop.tricentis.com/)
The framework automates key e-commerce functionalities including:
* User Registration
* User Login
* Product Search
* Product Filtering
* Product Comparison
* Wishlist Management
* Shopping Cart Operations
* Guest Checkout
* Registered User Checkout
* Order Placement
* Recently Viewed Products
* Account Management
* Return Requests
  

## Technology Stack

| Technology / Tool | Purpose | Version |
| :--- | :--- | :--- |
| *Java* | Core Programming Language | JDK 17 |
| *Selenium WebDriver* | UI Browser Automation | Latest |
| *Cucumber BDD* | Behavior-Driven Development Framework | Latest |
| *TestNG* | Test Execution Engine and Assertions | Latest |
| *Maven* | Build and Dependency Management Tool | Latest |
| *Page Object Model (POM)* | Framework Design Pattern Architecture | - |
| *Apache POI* | Excel-based Test Data Management | Latest |
| *Allure Reports* | Interactive Graphical Test Reporting | Latest |
| *Extent Reports* | Detailed Test Logs and Execution Summaries | Latest |


## Framework Architecture

The project follows the Page Object Model (POM) design pattern.

```text
DemoShop_Cucumber
│
├── src/main/java
│   ├── pages
│   └── utility classes
│
├── src/test/java
│   ├── runner
│   ├── stepdefinitions
│   └── hooks
│
├── src/test/resources
│   ├── features
│   └── test data
│
├── allure-results
├── target
├── test-output
├── pom.xml
└── testng.xml
```


### Project Structure

### Pages Package Layout
```
The framework structure isolates UI interactions through the following Page Object Model (POM) classes:
* AccountPage.java — Manages user profiles, addresses, and order history.
* CartPage.java — Handles quantities, coupon codes, and transitions to checkout.
* CategoryPage.java — Manages item navigation, sorting options, and grid/list views.
* CheckoutPage.java — Automates billing, shipping, payment methods, and final order confirmations.
* CompareProductsPage.java — Handles the side-by-side product comparison grid.
* ContactUsPage.java — Handles the contact form submission.
* ExcelLoginUtility.java — A utility class for reading user credentials from Excel files.
* GuestCheckoutPage.java — Handles checkout flows for non-registered users.
* HomePage.java — Manages the landing page elements (sliders, featured products).
* LoginPage.java — Houses locators for the user sign-in portal.
* ProductDetailsPage.java — Manages item variants, quantity inputs, and "Add to Cart" buttons.
* ProductFilterPage.java — Automates refining product grids by price filters.
* ProductSortingPage.java — Automates refining product grids by position, name, or price sorting.
* RecentlyViewedPage.java — Validates history tracking of items viewed by the user.
* RegisteredCheckoutPage.java — Manages the fast-track checkout for signed-in accounts.
* RegisterPage.java — Handles new account creation forms.
* ReturnRequestPage.java — Automates product returns.
* SearchResultsPage.java — Validates search text queries against returned items.
* WishlistPage.java — Handles favorite items and moving them to the shopping cart.
```


## Feature Coverage

### User Management
* User Registration
* User Login
* User Logout
* Account Information Management

### Product Operations
* Product Search
* Category Navigation
* Product Sorting
* Product Filtering
* Product Details Validation

### Shopping Features
* Add Product to Cart
* Update Cart
* Remove Product from Cart
* Compare Products
* Add Products to Wishlist

### Checkout Features
* Guest Checkout
* Registered User Checkout
* Order Confirmation

### Customer Services
* Contact Us
* Return Request
* Recently Viewed Products

---

## Test Data Management
Excel-based test data handling is implemented using:
* 'UserCredentials.xlsx'
* 'ExcelLoginUtility.java'

### Benefits:
* Data-driven testing
* Reusable test data
* Easy maintenance
* Reduced hardcoding

## Cucumber BDD Implementation
Feature files are stored under:

src/test/resources/features


### Example:

Cucumber
Feature: Product Search

  Scenario: Search product and add to cart
    Given the user is on the Demo Web Shop homepage
    When the user searches for a product
    Then matching products should be displayed


## Test Execution

### Run All Scenarios

Shell
mvn clean test


### Run Specific Scenario Using Tags

Example:

Java
@CucumberOptions(
    tags = "@ProductSearch"
)

*Execute:*

Shell
mvn test


### Run Through TestNG

Plain Text
* Right Click -> Run As -> TestNG Suite


## Reporting

### Allure Report

#### Generate Results:

Shell
mvn test


#### Generate Report:

html
<!-- test-output/ -->

### Provides:
* Pass/Fail Status
* Execution Summary
* Screenshots
* Test Logs

## Design Patterns Used

### Page Object Model (POM)
#### Advantages:
* Reusable code
* Easy maintenance
* Better readability
* Reduced code duplication

### Data-Driven Testing
#### Advantages:
* Multiple test combinations
* Test-data separation
* Better scalability

### Behavior Driven Development (BDD)
#### Advantages:
* Collaboration
* Business-readable scenarios
* Better documentation

## Maven Dependencies
### Main dependencies used:

XML
<dependency>
    <groupId>org.seleniumhq.selenium</groupId>
    <artifactId>selenium-java</artifactId>
</dependency>

<dependency>
    <groupId>io.cucumber</groupId>
    <artifactId>cucumber-java</artifactId>
</dependency>

<dependency>
    <groupId>io.cucumber</groupId>
    <artifactId>cucumber-testng</artifactId>
</dependency>

<dependency>
    <groupId>org.testng</groupId>
    <artifactId>testng</artifactId>
</dependency>

<dependency>
    <groupId>io.qameta.allure</groupId>
    <artifactId>allure-cucumber7-jvm</artifactId>
</dependency>



## Key Framework Features
* Selenium WebDriver Automation
* Cucumber BDD Framework
* TestNG Integration
* Page Object Model
* Data-Driven Testing
* Excel Utility Support
* Allure Reporting
* Extent Reporting
* Reusable Components
* Scalable Framework Structure
* Maven Build Management

  

## Authors
* Nisha Mandwal
* Pammi Yashwitha Reddy
* Pasagadugula Sree Keerthana
* Mamatha Potunuru
* Arthi Prasanna Reddy Musatla
* Kandukuri Siddarth Goud

*Role:* Project Engineer | SDET Automation Engineer  

*Project Type:*

End-to-End E-Commerce Automation Testing Framework for Demo Web Shop Application using Selenium, Cucumber, TestNG, Maven, and Page Object Model.



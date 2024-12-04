# Scholarship System

A simple Java console-based application that simulates a scholarship application process for students, allowing them to fill out necessary information, and checks if they are eligible for a scholarship based on their academic performance (GWA). The system supports both **High School** and **College** students with different eligibility criteria.

## Features

- **Student Information Collection**: Allows students to enter personal details such as name, age, address, email, contact number, school, grade level, program, and their GWA (Grade Weighted Average).
- **Scholarship Eligibility**:
  - **High School Students**: Accepted if GWA >= 85.
  - **College Students**: Accepted if GWA <= 3.0 (assuming a 4.0 scale).
- **Polymorphism**: The program handles different types of students (`HighSchoolStudent` and `CollegeStudent`) with their own specific scholarship eligibility rules, allowing for easy extension and future changes.
- **Object-Oriented Design**: The program demonstrates key OOP principles such as **Encapsulation**, **Inheritance**, **Polymorphism**, and **Abstraction**.

## Prerequisites

- Java 8 or higher is required to run the program.
- Basic understanding of object-oriented programming (OOP) concepts like **Encapsulation**, **Inheritance**, **Polymorphism**, and **Abstraction**.

## OOP Concepts Used

### 1. **Encapsulation**
   - **Encapsulation** refers to the concept of bundling the data (attributes) and methods that operate on the data into a single unit, or class. In this program, the student information such as `studentName`, `studentAge`, `studentEmail`, and `studentGWA` are private, and the only way to access or modify them is through public getter and setter methods. This ensures that the data is protected from unauthorized access and modification.
   
### 2. **Inheritance**
   - **Inheritance** is a mechanism where one class (child) acquires the properties and behaviors (methods) of another class (parent). In this program, `HighSchoolStudent` and `CollegeStudent` classes inherit from the abstract class `ScholarshipApplication`. These subclasses inherit common student properties, and each class implements its own version of the `processApplication()` method.

### 3. **Polymorphism**
   - **Polymorphism** allows objects of different types to be treated as objects of a common super type. It specifically refers to the ability to call the same method on different objects, with each object responding in a way appropriate to its type. In this program, the method `processApplication()` is defined in the abstract class `ScholarshipApplication` but is overridden in the subclasses `HighSchoolStudent` and `CollegeStudent` to provide specific behavior for each type of student.

### 4. **Abstraction**
   - **Abstraction** is the concept of hiding the complex implementation details and showing only the necessary parts of the object. In this program, the `ScholarshipApplication` class is **abstract**, meaning it cannot be instantiated directly. It defines the blueprint for student application processing with the abstract method `processApplication()`. Subclasses like `HighSchoolStudent` and `CollegeStudent` provide their own implementation of `processApplication()`.

   javac ScholarshipSystem.java

## **Experiment No : Extra**

## **Experiment Name : Study and Implementation of Basic Object-Oriented Programming Concepts in C++.**

## **Submission Date : October 17, 2024**


---

## **Theory :**
<div align="justify">
The theory of this lab report focuses on the foundational concepts of object-oriented programming (OOP) such as classes, inheritance, polymorphism, and operator overloading. 

In OOP, a class is a blueprint that defines the properties (attributes) and behaviors (methods) of objects. Creating instances of these classes allows for encapsulation, where data and methods are bundled together. Inheritance enables the creation of new classes (derived classes) based on existing ones, facilitating code reuse and extension. Polymorphism allows different classes to be treated as instances of a base class, where function overriding enables specialized behavior in derived classes. 

Additionally, operator overloading provides a way to define custom behaviors for standard operators, enhancing code readability and functionality. The concepts also include managing collections through classes, static members for shared data, and abstraction for defining common interfaces in derived classes. 

This lab emphasizes practical implementation of these concepts to develop efficient, reusable, and organized code structures.
</div>

## **Problem 1:**
Create a class called Book with attributes such as title, author, and price. Include a method to display the book's details. Write a program that instantiates a Book object and displays its details.

## **Code :**

```cpp
#include <iostream>
using namespace std;

class Book {
private:
    string title;
    string author;
    double price;

public:
    Book(string t, string a, double p) {
        title = t;
        author = a;
        price = p;
    }

    void displayDetails() {
        cout << endl << "The Book Information: " << endl;
        cout << "Title: " << title << endl;
        cout << "Author: " << author << endl;
        cout << "Price: BDT " << price << endl;
    }
};

int main() {
    string title, author;
    double price;

    cout << "Enter book title: ";
    getline(cin, title);

    cout << "Enter author name: ";
    getline(cin, author);

    cout << "Enter price: ";
    cin >> price;

    Book myBook(title, author, price);
    myBook.displayDetails();

    return 0;
}
```

## **Output :**
<p align="center">
<img width="472" height="220" alt="Screenshot 2024-10-16 at 7 43 01 PM" src="https://github.com/user-attachments/assets/a4767676-caba-445d-868a-a32fa8217980">
</p>

## **Discussion :**
<div align="justify">
This program demonstrates a basic example of object-oriented programming by using a Book class. The class has private attributes for storing the book's title, author, and price. It includes a constructor to set these values when an object is created, and a method displayDetails to print out the book's information. The program takes input from the user for the title, author, and price, creating a Book object with this data, and then displays the details. This approach helps in organizing and handling book information in a structured way.
</div>

<br>

## **Problem 2:**
Develop a class Student that has attributes for student ID and name. Include a method to display the student's information. Create an instance of the Student class and print its details.

## **Code :**

```cpp
#include <iostream>
using namespace std;

class Student {
private:
    int studentID;
    string name;

public:
    Student(int id, string n) {
        studentID = id;
        name = n;
    }

    void displayInfo() {
        cout << "The Student Informations: " << endl;
        cout << "Student ID: " << studentID << endl;
        cout << "Name: " << name << endl;
    }
};

int main() {
    Student student1(2210044, "Somya Disha");
    student1.displayInfo();

    return 0;
}
```

## **Output :**
<p align="center">
<img width="472" height="200" alt="Screenshot 2024-10-16 at 7 54 54 PM" src="https://github.com/user-attachments/assets/ce522701-9bc4-43b1-82d6-d02217c046d6">
</p>

## **Discussion :**
<div align="justify">
This code creates a Student class that stores a student's ID and name. It has a constructor for initializing these values and a method called displayInfo() to print the student's details.
In the main() function, an instance of the Student class is created with a specific ID and name. The displayInfo() method displays the student's information. Overall, this code demonstrates basic object-oriented programming concepts in C++.
</div>

<br>

## **Problem 3:**
Implement a class called Calculator with methods for basic arithmetic operations (addition, subtraction, multiplication, division). Write a program that allows the user to perform calculations using the Calculator class.

## **Code :**

```cpp
#include <iostream>
using namespace std;

class Calculator {
private:
    double result;

public:
    double add(double a, double b) {
        result = a + b;
        return result;
    }

    double subtract(double a, double b) {
        result = a - b;
        return result;
    }

    double multiply(double a, double b) {
        result = a * b;
        return result;
    }

    double divide(double a, double b) {
        if (b != 0) {
            result = a / b;
            return result;
        } else {
            cout << "Error: Division by zero!" << endl;
            return 0; 
        }
    }

    void displayResult() {
        cout << "Result: " << result << endl;
    }
};

int main() {
    Calculator cal;
    double num1, num2;
    char operation;

    cout << "Enter first number: ";
    cin >> num1;
    cout << "Enter an operation (+, -, *, /): ";
    cin >> operation;
    cout << "Enter second number: ";
    cin >> num2;

    if (operation == '+') {
        cout << "Result: " << cal.add(num1, num2) << endl;
    } else if (operation == '-') {
        cout << "Result: " << cal.subtract(num1, num2) << endl;
    } else if (operation == '*') {
        cout << "Result: " << cal.multiply(num1, num2) << endl;
    } else if (operation == '/') {
        cout << "Result: " << cal.divide(num1, num2) << endl;
    } else {
        cout << "Invalid operation!" << endl;
    }

    return 0;
}
```

## **Output :**
<p align="center">
<img width="472" height="220" alt="Screenshot 2024-10-16 at 8 02 15 PM" src="https://github.com/user-attachments/assets/4a0c8dc4-5c27-47e5-86e3-427b16bed801">
</p>

## **Discussion :**
<div align="justify">
This code defines a simple calculator using a Calculator class that performs addition, subtraction, multiplication, and division. The user inputs two numbers and an operation, which the program processes by calling the respective method. It includes error handling for division by zero, ensuring a smooth user experience. This example highlights basic object-oriented programming concepts and input validation.
</div>

<br>

## **Problem 4:**
Create a Person class with attributes for name and age. Implement a method to check if the person is an adult (18 years or older). Instantiate a Person object and check if they are an adult.

## **Code :**

```cpp
#include <iostream>
using namespace std;

class Person {
private:
    string name;
    int age;

public:
    Person(string n, int a) {
        name = n;
        age = a;
    }

    int isAdult() {
        if (age >= 18) {
            return 1; 
        } else {
            return 0; 
        }
    }

    void displayInfo() {
        cout << endl << "The Person Information: " << endl;
        cout << "Name: " << name << endl;
        cout << "Age: " << age << endl;
        if (isAdult() == 1) {
            cout << name << " is an adult." << endl;
        } else {
            cout << name << " is not an adult." << endl;
        }
    }
};

int main() {
    string name;
    int age;

    cout << "Enter Name: ";
    getline(cin, name);
    cout << "Enter Age: ";
    cin >> age;

    Person person1(name, age);
    person1.displayInfo();

    return 0;
}
```

## **Output :**
<p align="center">
<img width="472" height="250" alt="Screenshot 2024-10-16 at 8 08 04 PM" src="https://github.com/user-attachments/assets/5e11d2c6-fac1-4f0b-878e-1619cea347f0">
</p>

## **Discussion :**
<div align="justify">
This code defines a Person class with attributes for name and age. It includes a method to check if the person is an adult and another method to display the person's details. In the main() function, a Person object is created, and the user can input the name and age. The program then displays whether the person is an adult or not. This example illustrates basic concepts of object-oriented programming, such as encapsulation and method usage.
</div>

<br>

## **Problem 5:**
Design a class hierarchy with a base class Employee and subclasses Manager and Intern. Implement methods to calculate and display the salary of each type of employee. Write a program that demonstrates the use of inheritance and method overriding.

## **Code :**

```cpp
#include <iostream>
using namespace std;

class Employee {
protected:
    string name;
    double baseSalary;

public:
    Employee(string n, double salary) {
        name = n;
        baseSalary = salary;
    }

    virtual double calculateSalary() {
        return baseSalary;
    }

    virtual void displayInfo() {
        cout << "Employee Name: " << name << endl;
        cout << "Base Salary: BDT " << baseSalary << endl;
        cout << "Total Salary: BDT " << calculateSalary() << endl;
    }
};

class Manager : public Employee {
public:
    double bonus; 

    Manager(string n, double salary, double b) : Employee(n, salary) {
        bonus = b;
    }

    double calculateSalary() override {
        return baseSalary + bonus;
    }

    void displayInfo() override {
        cout << "Manager Name: " << name << endl;
        cout << "Base Salary: BDT " << baseSalary << endl;
        cout << "Bonus: BDT " << bonus << endl;
        cout << "Total Salary: BDT " << calculateSalary() << endl;
    }
};

class Intern : public Employee {
public:
    int hoursWorked;   
    double hourlyRate; 

    Intern(string n, double salary, int hours, double rate) : Employee(n, salary) {
        hoursWorked = hours;
        hourlyRate = rate;
    }
    
    double calculateSalary() override {
        return baseSalary + (hoursWorked * hourlyRate);
    }

    void displayInfo() override {
        cout << "Intern Name: " << name << endl;
        cout << "Base Salary: BDT " << baseSalary << endl;
        cout << "Hours Worked: " << hoursWorked << endl;
        cout << "Hourly Rate: BDT " << hourlyRate << endl;
        cout << "Total Salary: BDT " << calculateSalary() << endl;
    }
};

int main() {
    Manager manager1("Shirin Akter", 50000, 30000);  
    Intern intern1("Somya Disha", 5000, 8, 150);      

    cout << "Manager Details:" << endl;
    manager1.displayInfo();

    cout << endl << "Intern Details:" << endl;
    intern1.displayInfo();

    return 0;
}
```

## **Output :**
<p align="center">
<img width="472" height="350" alt="Screenshot 2024-10-16 at 8 17 14 PM" src="https://github.com/user-attachments/assets/6573a287-d740-4290-b0d3-c4cb4dfaf847">
</p>

## **Discussion :**
<div align="justify">
This C++ code implements a basic employee management system using object-oriented principles. It features a base class, Employee, which holds common attributes like name and base salary, and defines methods for calculating and displaying salary.
Two derived classes, Manager and Intern, extend the Employee class. The Manager class includes a bonus, while the Intern class calculates salary based on hours worked and an hourly rate.
In the main function, instances of Manager and Intern are created, and their details are displayed. This demonstrates how inheritance allows for specialized behavior while maintaining a common interface for all employees.
</div>

<br>

## **Problem 6:**
Implement a class called Library that manages a collection of Book objects. Include methods to add and remove books, as well as display all available books. Write a program to test the functionality of the Library class.

## **Code :**

```cpp
#include <iostream>
#include <string>
using namespace std;

class Book {
public:
    string title;
    string author;

    Book() {
        title = "";
        author = "";
    }

    Book(string t, string a) {
        title = t;
        author = a;
    }
};

class Library {
private:
    Book books[100]; 
    int bookCount; 

public:
    Library() {
        bookCount = 0;
    }

    void addBook(Book book) {
        if (bookCount < 100) {
            books[bookCount] = book; 
            cout << "Added: " << book.title << " by " << book.author << endl;
            bookCount++;
        } else {
            cout << "Library is full." << endl;
        }
    }

    int removeBook(string title) {
        for (int i = 0; i < bookCount; i++) {
            if (books[i].title == title) {
                cout << "Removed: " << books[i].title << endl;
                for (int j = i; j < bookCount - 1; j++) {
                    books[j] = books[j + 1];
                }
                bookCount--;
                return 1; 
            }
        }
        cout << "Not found: " << title << endl;
        return 0; 
    }
    
    int displayBooks() {
        if (bookCount == 0) {
            cout << "No books available." << endl;
            return 0; 
        }
        cout << "Books in Library:" << endl;
        for (int i = 0; i < bookCount; i++) {
            cout << books[i].title << " by " << books[i].author << endl;
        }
        return 1; 
    }
};

int main() {
    Library library;

    library.addBook(Book("Nondito Noroke", "Humayun Ahmed"));
    library.addBook(Book("Shongkhonil Karagar", "Humayun Ahmed"));
    library.addBook(Book("Opekkha", "Humayun Ahmed"));

    library.displayBooks();

    library.removeBook("Opekkha");

    library.displayBooks();

    library.removeBook("Shongkhonil Karagar");
    library.displayBooks();
    
    return 0;
}
```

## **Output :**
<p align="center">
<img width="472" height="400" alt="Screenshot 2024-10-16 at 8 37 18 PM" src="https://github.com/user-attachments/assets/5ac39f5f-5245-484e-a0fd-0686e1e20897">
</p>

## **Discussion :**
<div align="justify">
This code defines a simple library system using two classes: Book and Library. The Book class holds the title and author of a book, providing constructors for initializing these attributes.
The Library class manages a collection of Book objects. It can add books up to a limit of 100, remove a book by title, and display the list of available books. The addBook method checks if there's space in the library before adding a new book, while removeBook searches for a book by title and adjusts the list accordingly. If a book is not found, it provides feedback to the user.
In the main() function, the library is instantiated, and three books are added. The library's contents are displayed, a book is removed, and the updated list is shown. This demonstrates the basic functionalities of adding, removing, and listing books in a library context. The design emphasizes simplicity and usability, making it easy to expand with additional features in the future.
</div>

<br>

## **Problem 7:**
Create a class ShoppingCart that holds a list of Product objects. Implement methods to add items to the cart, remove items, and calculate the total price. Write a program to test the functionality of the ShoppingCart class.

## **Code :**

```cpp
#include <iostream>
#include <string>
using namespace std;

class Product {
public:
    string name;
    double price;

    Product() {
        name = "";
        price = 0.0;
    }

    Product(string n, double p) {
        name = n;
        price = p;
    }
};

class ShoppingCart {
private:
    Product products[100]; 
    int productCount; 

public:
    ShoppingCart() {
        productCount = 0;
    }

    void addProduct(Product product) {
        if (productCount < 100) {
            products[productCount] = product; 
            cout << "Added: " << product.name << " for BDT " << product.price << endl;
            productCount++;
        } else {
            cout << "Shopping cart is full." << endl;
        }
    }

    int removeProduct(string name) {
        for (int i = 0; i < productCount; i++) {
            if (products[i].name == name) {
                cout << "Removed: " << products[i].name << endl;
                for (int j = i; j < productCount - 1; j++) {
                    products[j] = products[j + 1];
                }
                productCount--;
                return 1; 
            }
        }
        cout << "Not found: " << name << endl;
        return 0; 
    }

    double calculateTotal() {
        double total = 0;
        for (int i = 0; i < productCount; i++) {
            total += products[i].price;
        }
        return total; 
    }

    int displayProducts() {
        if (productCount == 0) {
            cout << "Shopping cart is empty." << endl;
            return 0; 
        }
        cout << "Products in Shopping Cart:" << endl;
        for (int i = 0; i < productCount; i++) {
            cout << products[i].name << " for BDT " << products[i].price << endl;
        }
        return 1; 
    }
};

int main() {
    ShoppingCart cart;

    cart.addProduct(Product("Apple", 20));
    cart.addProduct(Product("Banana", 5));
    cart.addProduct(Product("Orange", 30));

    cart.displayProducts();

    double total = cart.calculateTotal();
    cout << "Total Price: BDT " << total << endl;

    int result = cart.removeProduct("Banana");

    cart.displayProducts();

    total = cart.calculateTotal();
    cout << "Total Price after removal: BDT " << total << endl;

    return 0;
}
```

## **Output :**
<p align="center">
<img width="472" height="400" alt="Screenshot 2024-10-16 at 8 50 41 PM" src="https://github.com/user-attachments/assets/008cdbe5-e265-4f18-8599-534b59656c93">
</p>

## **Discussion :**
<div align="justify">
The provided code implements a simple shopping cart system using C++. It defines two classes: Product and ShoppingCart. The Product class stores the name and price of individual products, while the ShoppingCart class manages a collection of products.
The shopping cart allows adding products, removing them by name, calculating the total price of all items, and displaying the current products. This functionality is achieved through various member functions that ensure the cart can handle a maximum of 100 products.
Key features include feedback messages upon adding or removing items, and a total price calculation that updates dynamically as products are added or removed. The design demonstrates the use of basic object-oriented programming principles, such as encapsulation and the separation of concerns, making the code modular and easier to maintain. Overall, this implementation provides a foundational understanding of managing collections of objects and performing operations on them in C++.
</div>

<br>

## **Problem 8:**
Write an abstract class called Appliance with an abstract method turnOn(). Create subclasses WashingMachine and Refrigerator that implement this method. Write a program that demonstrates method overriding(function overriding).

## **Code :**

```cpp
#include <iostream>
using namespace std;

class Appliance {
public:
    virtual void turnOn() = 0; 
};

class WashingMachine : public Appliance {
public:
    void turnOn() override {
        cout << "Washing machine is now on." << endl;
    }
};

class Refrigerator : public Appliance {
public:
    void turnOn() override {
        cout << "Refrigerator is now on." << endl;
    }
};

int main() {
    WashingMachine w;
    Refrigerator r;

    w.turnOn();     
    r.turnOn(); 
    
    return 0;
}
```

## **Output :**
<p align="center">
<img width="472" height="150" alt="Screenshot 2024-10-16 at 8 55 35 PM" src="https://github.com/user-attachments/assets/1b1d43c9-4031-4a33-b22a-d46e793d15c8">
</p>

## **Discussion :**
<div align="justify">
The code illustrates polymorphism using an abstract base class, Appliance, which defines a pure virtual function turnOn(). Two derived classes, WashingMachine and Refrigerator, implement this function to display messages indicating their operation. This design allows for easy extension; new appliances can be added by creating additional derived classes. The example effectively demonstrates the principles of abstraction and polymorphism in object-oriented programming.
</div>

<br>

## **Problem 9:**
Design a class School that manages a collection of Student objects. Implement methods to add, remove, and search for students by ID. Write a program to test the School class.

## **Code :**

```cpp
#include <iostream>
#include <string>
using namespace std;

class Student {
public:
    int id;
    string name;

    Student() {
        id = 0;
        name = ""; 
    }
    Student(int studentId, string studentName) {
        id = studentId;   
        name = studentName;
    }
};

class School {
private:
    Student students[100]; 
    int studentCount; 

public:
    School() {
        studentCount = 0;
    }

    int addStudent(int id, string name) {
        if (studentCount < 100) {
            students[studentCount] = Student(id, name); 
            cout << "Added Student: " << name << " with ID: " << id << endl;
            studentCount++;
            return 1;
        } 
        cout << "School is full, cannot add more students." << endl;
        return 0; 
    }

    int removeStudent(int id) {
        for (int i = 0; i < studentCount; i++) {
            if (students[i].id == id) {
                cout << endl << "Removed Student: " << students[i].name << " with ID: " << id << endl;
                for (int j = i; j < studentCount - 1; j++) {
                    students[j] = students[j + 1];
                }
                studentCount--;
                return 1;
            }
        }
        cout << "Student with ID: " << id << " not found." << endl;
        return 0; 
    }

    int searchStudent(int id) {
        for (int i = 0; i < studentCount; i++) {
            if (students[i].id == id) {
                cout << endl << "Found Student: " << students[i].name << " with ID: " << id << endl;
                return 1; 
            }
        }
        cout << "Student with ID: " << id << " not found." << endl;
        return 0; 
    }
};

int main() {
    School school;

    school.addStudent(1, "Sharmin");
    school.addStudent(2, "Disha");
    school.addStudent(3, "Nilima");

    school.searchStudent(2); 
    school.searchStudent(4); 

    school.removeStudent(1); 
    school.removeStudent(4); 

    school.searchStudent(1); 
    
    return 0;
}
```

## **Output :**
<p align="center">
<img width="472" height="300" alt="Screenshot 2024-10-16 at 9 07 29 PM" src="https://github.com/user-attachments/assets/aaf53f81-387d-41b7-abbe-f562cc58cf18">
</p>

## **Discussion :**
<div align="justify">
The code implements a simple student management system using classes in C++. The Student class holds information about each student, including their ID and name. The School class manages a collection of students with capabilities to add, remove, and search for students based on their ID.
The system demonstrates basic object-oriented principles, such as encapsulation and data management. Adding, removing, and searching for students are handled through methods, ensuring organized and maintainable code. The user-friendly output messages guide interactions, making it clear whether operations succeed or fail. This structure could be further expanded to include features like updating student information or listing all students.
</div>

<br>

## **Problem 10:**
Create a class Game that has methods to start, pause, and end the game. Implement a method to display the game's status. Write a program that simulates a simple game using the Game class.

## **Code :**

```cpp
#include <iostream>
#include <string>
using namespace std;

class Game {
private:
    string status; 

public:
    Game() {
        status = "Not started"; 
    }

    void start() {
        status = "Running"; 
        cout << endl << "Game started." << endl;
    }

    void pause() {
        if (status == "Running") {
            status = "Paused";
            cout << endl << "Game paused." << endl;
        } else {
            cout << "Game is not running. Can't pause." << endl;
        }
    }
    
    void end() {
        status = "Ended";
        cout << endl << "Game ended." << endl;
    }

    void displayStatus() {
        cout << "Current game status: " << status << endl; 
    }
};

int main() {
    Game myGame; 

    myGame.displayStatus(); 

    myGame.start(); 
    myGame.displayStatus();

    myGame.pause(); 
    myGame.displayStatus(); 

    myGame.start(); 
    myGame.displayStatus(); 

    myGame.end(); 
    myGame.displayStatus(); 

    return 0;
}
```

## **Output :**
<p align="center">
<img width="472" height="400" alt="Screenshot 2024-10-16 at 9 18 33 PM" src="https://github.com/user-attachments/assets/cfee9347-f394-4d95-9b26-58a9f73972c3">
</p>


## **Discussion :**
<div align="justify">
The code shows a simple game management system using a Game class in C++. The class keeps track of the game's status, which can be "Not started," "Running," "Paused," or "Ended." It has methods to start the game, pause it, end it, and display the current status.
The code uses encapsulation by keeping the status hidden from direct access. The methods make sure that the game can only be paused when it is running, which prevents errors. This setup is straightforward and allows for easy changes or additions in the future while showing basic concepts of object-oriented programming.
</div>

<br>

## **Problem 11:**
Design a class Person that includes a static variable to count the number of Person objects created. Implement a method to display the total count of persons. Write a program that creates several Person objects and displays the count.

## **Code :**

```cpp
#include <iostream>
#include <string>
using namespace std;

class Person {
private:
    string name;
    int age;    
    static int count;

public:
    Person(string n, int a) {
        name = n;  
        age = a;  
        count++;   
    }

    static void displayCount() {
        cout << "Total number of Person objects created: " << count << endl; 
    }
};

int Person::count = 0;

int main() {
    Person p1("Disha", 22); 
    Person p2("Nur", 24);   
    Person p3("Shammey", 26); 

    Person::displayCount(); 

    return 0;
}
```

## **Output :**
<p align="center">
<img width="472" height="120" alt="Screenshot 2024-10-16 at 9 24 10 PM" src="https://github.com/user-attachments/assets/17968fa9-93ce-454b-a4b8-be41f2432b1b">
</p>


## **Discussion :**
<div align="justify">
The code defines a Person class that keeps track of how many Person objects are created using a static variable called count. Each time a new Person is made, the constructor increases this count. The static method displayCount() shows the total number of Person objects created. This example highlights how static members work in a class, allowing shared data among all instances. The program displays the total count of Person objects when it runs.
</div>

<br>

## **Problem 12:**
Define a class Complex with private members real and imaginary. Overload the operators +, -, *, and / to perform addition, subtraction, multiplication, and division of two complex numbers, respectively. Create a constructor to initialize the complex number and include a method to display the result. The main() function should be used to test these overloaded operators.

## **Code :**

```cpp
#include <iostream>
using namespace std;

class Complex {
private:
    double real;      
    double imaginary; 
    
public:
    Complex(double r, double i) {
        real = r;       
        imaginary = i;  
    }

    Complex operator+(Complex other) {
        return Complex(real + other.real, imaginary + other.imaginary);
    }

    Complex operator-(Complex other) {
        return Complex(real - other.real, imaginary - other.imaginary);
    }

    Complex operator*(Complex other) {
        return Complex(real * other.real - imaginary * other.imaginary, 
                       real * other.imaginary + imaginary * other.real);
    }

    Complex operator/(Complex other) {
        double denominator = other.real * other.real + other.imaginary * other.imaginary;
        return Complex((real * other.real + imaginary * other.imaginary) / denominator,
                       (imaginary * other.real - real * other.imaginary) / denominator);
    }

    void display() {
        if (imaginary >= 0)
            cout << real << " + " << imaginary << "i" << endl; 
        else
            cout << real << " - " << -imaginary << "i" << endl; 
    }
};

int main() {
    double r1, i1, r2, i2;

    cout << "First real part: ";
    cin >> r1;
    cout << "First imaginary part: ";
    cin >> i1;
    
    cout << "2nd real part: ";
    cin >> r2;
    cout << "2nd imaginary part: ";
    cin >> i2;

    Complex c1(r1, i1);  
    Complex c2(r2, i2);  

    Complex sum = c1 + c2;          
    Complex difference = c1 - c2;   
    Complex product = c1 * c2;     
    Complex quotient = c1 / c2;    

    cout << "Sum: ";
    sum.display();                   

    cout << "Difference: ";
    difference.display();            

    cout << "Product: ";
    product.display();               

    cout << "Quotient: ";
    quotient.display();             

    return 0;
}
```

## **Output :**
<p align="center">
<img width="472" height="250" alt="Screenshot 2024-10-16 at 9 31 58 PM" src="https://github.com/user-attachments/assets/a7491dc7-c0d0-4729-a835-9bf707b5d9c5">
</p>


## **Discussion :**
<div align="justify">
This program models complex numbers in C++ and allows for arithmetic operations like addition, subtraction, multiplication, and division. Using operator overloading, it provides a clean and intuitive way to work with complex numbers. The user inputs the real and imaginary parts, and the program outputs the results of the calculations in a standard format. Overall, it effectively demonstrates how to manage and manipulate complex numbers in a simple manner.
</div>

<br>

## **Problem 13:**
Define a class Rectangle with private members length and breadth. Overload the operators == to check if two rectangles have equal areas, and > and < to compare if one rectangle is larger or smaller than the other based on area. Implement a constructor to initialize the rectangle's dimensions and a method to calculate its area. The main() function should test the overloaded operators.

## **Code :**

```cpp
#include <iostream>
using namespace std;

class Rectangle {
private:
    double length;  
    double breadth; 

public:
    Rectangle(double l, double b) {
        length = l;   
        breadth = b; 
    }

    double area() {
        return length * breadth; 
    }

    int operator==(Rectangle other) {
        return area() == other.area(); 
    }

    int operator>(Rectangle other) {
        return area() > other.area(); 
    }

    int operator<(Rectangle other) {
        return area() < other.area(); 
    }
};

int main() {
    double l1, b1, l2, b2;

    cout << "Enter length and breadth for Rectangle 1: ";
    cin >> l1 >> b1;
    cout << "Enter length and breadth for Rectangle 2: ";
    cin >> l2 >> b2;

    Rectangle r1(l1, b1); 
    Rectangle r2(l2, b2); 

    if (r1 == r2) {
        cout << endl <<  "Rectangle 1 and Rectangle 2 have equal areas." << endl;
    } else {
        cout << endl << "Rectangle 1 and Rectangle 2 do not have equal areas." << endl;
    }

    if (r1 > r2) {
        cout << endl << "Rectangle 1 is larger than Rectangle 2." << endl;
    } else {
        cout << endl << "Rectangle 1 is not larger than Rectangle 2." << endl;
    }

    if (r1 < r2) {
        cout << endl << "Rectangle 1 is smaller than Rectangle 2." << endl;
    } else {
        cout << endl << "Rectangle 1 is not smaller than Rectangle 2." << endl;
    }

    return 0;
}
```

## **Output :**
<p align="center">
<img width="472" height="250" alt="Screenshot 2024-10-16 at 10 03 15 PM" src="https://github.com/user-attachments/assets/262e026c-564e-4df2-ab37-7ba684899b7d">
</p>


## **Discussion :**
<div align="justify">
This program defines a Rectangle class that allows you to compare two rectangles based on their areas. It includes a constructor to initialize the rectangle's dimensions and methods to overload the operators ==, >, and <. The program takes input for the lengths and breadths of two rectangles, compares their areas, and outputs whether they are equal or if one is larger or smaller than the other. This demonstrates the use of operator overloading in C++, making comparisons intuitive and straightforward.
</div>

<br>

## **Conclusion :**
<div align="justify">
In conclusion, this report presents 13 C++ programs that show important ideas of object-oriented programming (OOP). Each program demonstrates key concepts like encapsulation, inheritance, polymorphism, and operator overloading, which help organize and manage data effectively.

The examples range from managing books and students to performing operations on complex numbers and handling game statuses. Each discussion explains how the program works and the OOP principles it uses, showing how these ideas can make code easier to understand and maintain. Overall, this collection is a helpful resource for learning basic C++ programming and the benefits of OOP in creating software.

</div>


<br>

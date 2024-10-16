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



## **Conclusion :**
<div align="justify">
Both programs effectively use OOP concepts to solve common problems. The Array class finds the second lowest and second highest values, while the LeapYear class checks if a year is a leap year. Correcting my earlier mistake of not using OOP for the leap year problem reinforces the value of structured programming in lab work.

</div>


<br>

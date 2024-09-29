## **Experiment No : 07**

## **Experiment Name : Implementation of C++ Classes and Object-Oriented Programming Concepts**

## **Submission Date : September 30, 2024**


---

## **Theory :**
<div align="justify">
Object-oriented programming (OOP) in C++ is about using classes to organize data and functions together. Encapsulation keeps data safe by allowing only certain functions to access it. Inheritance lets one class take on the properties of another class, making code reusable. Polymorphism allows different classes to have their own way of doing the same task using virtual functions. These ideas are used in different examples like managing employees, calculating areas of shapes, and handling bank accounts, showing how useful OOP is in C++.


</div>

## **Problem 5:**
Write a C++ program to implement a class called Date that has private member variables for day, month, and year. Include member functions to set and get these variables, as well as to validate if the date is valid.

## **Code :**

```C++
#include <iostream>
using namespace std;

class Date {
private:
    int day, month, year;

public:
    void setDate(int d, int m, int y) {
        day = d;
        month = m;
        year = y;
    }

    void showDate() {
        cout << "Date: " << day << "/" << month << "/" << year << endl;
    }
    int LeapYear() {
        if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0))
            return 1;
        else
            return 0;
    }
    int ValidDate() {
        if (month < 1 || month > 12)
            return 0;
        if (day < 1 || day > 31)
            return 0;

        if (month == 4 || month == 6 || month == 9 || month == 11) {
            if (day > 30)
                return 0;
        }
        
        if (month == 2) {
            if (LeapYear()) {
                if (day > 29)
                    return 0;
            } else {
                if (day > 28)
                    return 0;
            }
        }
        return 1; 
    }
};

int main() {
    Date date;
    int d, m, y;

    cout << "DD/MM/YYYY: ";
    cin >> d >> m >> y;

    date.setDate(d, m, y);

    if (date.ValidDate() == 1) {
        date.showDate();
        cout << "The date is valid." << endl;
    } else {
        cout << "The date is invalid." << endl;
    }

    return 0;
}

```

## **Output :**
<p align="center">
<img width="500" height="230" alt="Screenshot 2024-09-29 at 11 19 57 PM" src="https://github.com/user-attachments/assets/e0f2c3e6-3385-47d8-b1a9-1175db05136c">
</p>

## **Discussion and Conclusion :**
<div align="justify">
At first, I solved the problem by assuming that all months have 30 days and didn’t think about leap years. This worked for some dates but gave wrong results for months like February or months with 31 days. To fix this, I changed the program to check the number of days in each month and added a check for leap years in February. Now, the program correctly checks if the date is valid, making it more accurate.
</div>

## **Problem 6:**
Write a program in C++ to display the first n terms of the Fibonacci series by using OOP concept.

## **Code :**

```C++
#include <iostream>
using namespace std;

class Fibonacci {
    int n; 
public:
    Fibonacci(int num) {
        n = num;
    }

    void printSeries() {
        int a = 0, b = 1, next;
        for (int i = 1; i <= n; i++) {
            cout << a << " ";
            next = a + b;
            a = b;
            b = next;
        }
    }
};

int main() {
    int num;

    cout << "Enter the number of terms: ";
    cin >> num;

    Fibonacci f(num);

    f.printSeries();

    return 0;
}

```

## **Output :**
<p align="center">
<img width="500" height="230" alt="Screenshot 2024-09-29 at 11 39 40 PM" src="https://github.com/user-attachments/assets/1daec2dc-a3dc-47c1-9e8a-401588c1cb0d">
</p>

## **Discussion and Conclusion :**
<div align="justify">
This C++ program uses object-oriented programming (OOP) to show the Fibonacci series. It has a class called Fibonacci with a variable n that holds the number of terms. The constructor sets n, and the printSeries() method calculates and prints the Fibonacci numbers. This approach keeps the code organized and allows for creating multiple objects with different values while using simple OOP concepts.
</div>

## **Problem 6:**
Write a program in C++ to display the first n terms of the Fibonacci series by using OOP concept.

## **Code :**

```C++
#include <iostream>
using namespace std;

class Fibonacci {
    int n; 
public:
    Fibonacci(int num) {
        n = num;
    }

    void printSeries() {
        int a = 0, b = 1, next;
        for (int i = 1; i <= n; i++) {
            cout << a << " ";
            next = a + b;
            a = b;
            b = next;
        }
    }
};

int main() {
    int num;

    cout << "Enter the number of terms: ";
    cin >> num;

    Fibonacci f(num);

    f.printSeries();

    return 0;
}

```

## **Output :**
<p align="center">
<img width="500" height="230" alt="Screenshot 2024-09-29 at 11 39 40 PM" src="https://github.com/user-attachments/assets/1daec2dc-a3dc-47c1-9e8a-401588c1cb0d">
</p>

## **Discussion and Conclusion :**
<div align="justify">
This C++ program uses object-oriented programming (OOP) to show the Fibonacci series. It has a class called Fibonacci with a variable n that holds the number of terms. The constructor sets n, and the printSeries() method calculates and prints the Fibonacci numbers. This approach keeps the code organized and allows for creating multiple objects with different values while using simple OOP concepts.
</div>


<br>

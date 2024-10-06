## **Experiment No : 08**

## **Experiment Name : Implementation of Object-Oriented Programming in Array and Conditional Logic.**

## **Submission Date : October 07, 2024**


---

## **Theory :**
<div align="justify">
Object-Oriented Programming (OOP) is a programming paradigm that structures software around objects, making code more modular, reusable, and easier to maintain. It achieves this by bundling data and the methods that operate on it within classes. One key feature of OOP is encapsulation, which hides the internal workings of objects, while abstraction simplifies user interaction by only exposing essential functionality. Inheritance allows new classes to inherit attributes and behaviors from existing ones, fostering code reuse and a clear hierarchical relationship. Polymorphism enhances flexibility by enabling different classes to be treated in a uniform way through common interfaces.

In this lab, OOP principles are applied to tackle problems related to array manipulation and conditional logic. By encapsulating logic within classes, the code becomes cleaner, easier to manage, and reusable. Array manipulation, such as finding specific values, is efficiently handled by OOP's structure. Similarly, conditional logic controls decision-making within the program, showcasing OOP's ability to solve practical tasks like determining leap years and handling arrays. These implementations highlight the practical advantages of OOP in real-world applications, where well-organized and flexible code is essential.

</div>

## **Problem 3:**
Write a C++ program to find the second lowest and highest numbers in a given array by using OOP concept.

## **Code :**

```C++
#include <iostream>
using namespace std;

class Array {
private:
    int lowest, highest, secondLowest, secondHighest;

public:
    void findSecond(int arr[], int size) {
        lowest = highest = arr[0];
        secondLowest = secondHighest = arr[0];

        for (int i = 1; i < size; i++) {
            if (arr[i] < lowest) 
                lowest = arr[i];
            if (arr[i] > highest) 
                highest = arr[i];
        }

        secondLowest = highest;
        secondHighest = lowest;

        for (int i = 0; i < size; i++) {
            if (arr[i] > lowest && arr[i] < secondLowest) secondLowest = arr[i];
            if (arr[i] < highest && arr[i] > secondHighest) secondHighest = arr[i];
        }
    }

    void displayResults() {
        cout << "Second Lowest: " << secondLowest << endl;
        cout << "Second Highest: " << secondHighest << endl;
    }
};

int main() {
    int arr[10];
    cout << "Enter 10 elements: ";
    for (int i = 0; i < 10; i++) {
        cin >> arr[i];
    }

    Array a;
    a.findSecond(arr, 10);
    a.displayResults();

    return 0;
}

```

## **Output :**
<p align="center">
<img width="500" height="200" alt="Screenshot 2024-09-29 at 11 49 53 PM" src="https://github.com/user-attachments/assets/d8c5c8d9-8406-4731-88d3-797a9aadd3ad">
</p>

## **Discussion :**
<div align="justify">
In this C++ program, I defined a class called Array to find the second lowest and second highest numbers in an integer array. I started by setting the lowest and highest values, then went through the array to determine these. After that, I calculated the second lowest and second highest numbers and displayed the results. I assumed there would be at least two different values, so adding checks for this would improve the program.
</div>

<br>

## **Problem 6:**
Write a C++ program to check whether a given year is a leap year or not by using OOP concept.

## **Code :**

```C++
#include <iostream>
using namespace std;

class LeapYear {
private:
    int year;

public:
    
    LeapYear(int y) {
        year = y;
    }

    int isLeapYear() {
        if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0))
            return 1;
        return 0;
    }

    void display() {
        if (isLeapYear())
            cout << year << " is a leap year." << endl;
        else
            cout << year << " is not a leap year." << endl;
    }
};

int main() {
    int year;
    cout << "Enter a year: ";
    cin >> year;

    LeapYear check(year); 
    check.display();   

    return 0;
}

```

## **Output :**
<p align="center">
<img width="500" height="150" alt="Screenshot 2024-10-07 at 12 35 42 AM" src="https://github.com/user-attachments/assets/ca570985-e68d-421b-8469-96fe679e2402">
</p>

## **Discussion :**
<div align="justify">
In this C++ program, I created a LeapYear class to check if a year is a leap year. The isLeapYear method applies the leap year rules, and the display method shows the result. In the main function, I prompt for a year and use the class to display the result. In the lab, I mistakenly didn't solve it using OOP concepts, so I repeated it in my lab report.
</div> 

## **Conclusion :**
<div align="justify">
Both programs effectively use OOP concepts to solve common problems. The Array class finds the second lowest and second highest values, while the LeapYear class checks if a year is a leap year. Correcting my earlier mistake of not using OOP for the leap year problem reinforces the value of structured programming in lab work.

</div>


<br>

## **Experiment No : 06**

## **Experiment Name : Implementation of Friend Funcition for data management in C++**

## **Submission Date : September 15, 2024**


---

## **Theory :**
<div align="justify">
In C++, the concept of friend functions is a powerful feature that allows specific non-member functions to access the private and protected members of a class. Unlike regular member functions, which are inherently bound to the class they belong to and have access to its private and protected data, friend functions are not part of the class's interface. Instead, they are defined outside of the class but are granted special access privileges through a friend declaration.<br><br>

The primary advantage of friend functions is their ability to perform operations that require direct access to the internal state of a class without compromising the encapsulation principle. Encapsulation, one of the core principles of object-oriented programming, emphasizes keeping the internal details of an object hidden from the outside world and only exposing necessary operations through public interfaces. While this principle maintains a clear separation between an object's internal state and its external interactions, there are scenarios where direct access to private members is essential for certain functionalities.
</div>

## **Problem:**
Create a C++ program that features three Student classes with private members for Name, Roll, and Marks. <br> a. Input data for three students and display their details. <br> b. Compare the marks to identify the student with the highest and lowest marks, displaying their roll numbers accordingly and compute the average marks of all three students. <br> c. Define a friend function named Teacher that will access the private data of the Student class.

## **Code :**
```C++
#include <iostream>
#include <string>
using namespace std;

class Student1 {
private:
    string Name = "a";
    int Roll = 1;
    int Mark = 90;

public:
    void show() {
        cout << Roll << endl;
    }

    int getMark() {
        return Mark;
    }

    friend void Teacher1(Student1& s1);
};

void Teacher1(Student1 &s1) {
    cout << "Students details from friend functions: " << endl;
    cout << "Roll " << s1.Roll << " with mark " << s1.getMark() << endl;
}

class Student2 {
private:
    string Name = "b";
    int Roll = 2;
    int Mark = 80;

public:
    void show() {
        cout << Roll << endl;
    }

    int getMark() {
        return Mark;
    }

    friend void Teacher2(Student2& s2);
};

void Teacher2(Student2 &s2) {
    cout << "Roll " << s2.Roll << " with mark " << s2.getMark() << endl;
}

class Student3 {
private:
    string Name = "c";
    int Roll = 3;
    int Mark = 70;

public:
    void show() {
        cout << Roll << endl;
    }

    int getMark() {
        return Mark;
    }

    friend void Teacher3(Student3& s3);
};

void Teacher3(Student3 &s3) {
    cout << "Roll " << s3.Roll << " with mark " << s3.getMark() << endl;
}

int main() {
    Student1 student1;
    Student2 student2;
    Student3 student3;

    Teacher1(student1);
    Teacher2(student2);
    Teacher3(student3);

    cout << "Best CT Roll: ";
    if (student1.getMark() >= student2.getMark() && student1.getMark() >= student3.getMark()) {
        student1.show();
    } else if (student2.getMark() >= student1.getMark() && student2.getMark() >= student3.getMark()) {
        student2.show();
    } else {
        student3.show();
    }

    cout << "Worst CT Roll: ";
    if (student1.getMark() <= student2.getMark() && student1.getMark() <= student3.getMark()) {
        student1.show();
    } else if (student2.getMark() <= student1.getMark() && student2.getMark() <= student3.getMark()) {
        student2.show();
    } else {
        student3.show();
    }

    cout << "Average Mark: ";
    int totalMark = student1.getMark() + student2.getMark() + student3.getMark();
    int avgMark = totalMark / 3;

    cout << avgMark << endl;

    return 0;
}

```

## **Output :**
<p align="center">
<img width="500" height="230" alt="Picture" src="https://github.com/user-attachments/assets/de7e2627-6930-487f-b9ef-58a633d0345c">
</p>

## **Discussion and Conclusion :**
<div align="justify">
This code shows the use of friend functions in C++ to access and display private data within student classes. Each class (Student1, Student2, Student3) has private attributes (Name, Roll, Mark) and public methods (show() and getMark()). Friend functions (Teacher1, Teacher2, Teacher3) are used to access these private members directly and display student details.
The main() function creates instances of these classes, uses friend functions to print student information, and calculates the best and worst marks along with the average mark. This code effectively shows how friend functions can access and manipulate private class data.
</div>
<br>








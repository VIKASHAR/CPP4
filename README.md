# CPP MODULE 4 :

# 4a :

# PROGRAM STATEMENT :
Write a CPP Program for Class conversion that can be achieved by conversion function which is 
done by the use of operator overloading (use Integer data)

# ALGORITHM :
1. Define a class with a private member variable of type int.
2. Overload the operator int() in the class to convert the class object into a int type.
3. Define the overloaded operator outside the class using the scope resolution operator.
4. In the main function, create an object of the class, set its value, and use the overloaded operator to 
convert it into a double.
5. Display the converted double value and end the program.

# PROGRAM :
NAME : Vikash A R
REG NO : 212222040179
```
#include <bits/stdc++.h>
using namespace std;
class Class_type_one
{
 int a;
public:
 Class_type_one()
 {
 cin >> a;
 }
 int get()
 {
 return a;
 }
 void display() 
 {
 cout << a << endl;
 }
};
class Class_type_two
{
 int b;
public:
 void operator=(Class_type_one objA)
 {
 b = objA.get();
 }
 void display() 
 {
 cout << b << endl;
 }
};
int main()
{
 Class_type_one a;
 Class_type_two b;
 b = a;
 a.display();
 b.display();
 return 0;
}
```

# OUTPUT :
![image](https://github.com/user-attachments/assets/f29b4442-6ff8-4764-96dd-f83df2b35b1d)

# RESULT :
Thus, The program is verified and executed successfully.The outputs match the expected 
results, confirming its correctness.

# 4b :

# PROGRAM STATEMENT :
Write a CPP program to demonstrate on the object composition (use character data)

# ALGORITHM :
1. Define a class Component with a private member variable of type character and methods to set and 
get its value.
2. Define a class Composite that has an object of the Component class as its member (object 
composition).
3. Provide methods in the Composite class to interact with the Component object (e.g., set and get the 
value).
4. In the main function, create an object of the Composite class, set the value for the Component object, 
and retrieve it.
5. Display the value from the Component object and end the program.end the program.

# PROGRAM :
```
#include <iostream>
using namespace std;
class A 
{
 char data;
public:
 A(char a) : data(a)
 {
 cout << "Constructor A(char a) is invoked" << endl;
 }
 void display() 
 {
 cout << "Data in member object of class A in class B = " << data << endl;
 }
};
class B 
{
 A objA; 
 char data;
public:
 B(char a) : objA(a), data(a) 
 {
 cout << "Data in object of class B = " << data << endl;
 }
 void display()
 {
 objA.display();
 }
};
int main()
{
 char a;
 cin>>a;
 
 B objB(a);
 objB.display();
 return 0;
}
```

# OUTPUT :
![image](https://github.com/user-attachments/assets/96e5fa56-6b26-47ce-814c-d1742549c2fe)

# RESULT :
Thus, The program is verified and executed successfully.The outputs match the expected 
results, confirming its correctness.

# 4c :

# PROGRAM STATEMENT :
Write a CPP program to initialise the members of a class and use the this pointer to do it.

# ALGORITHM :
1. Read three integers x, y, and z from the user.
2. Instantiate the MyClass object obj using the constructor with x, y, and z as arguments.
3. Inside the constructor, initialize the class members a, b, and c using this pointer.
4. Call the display() method to print the values of a, b, and c.
5. Return from main() to terminate the program.

# PROGRAM :
```
#include <iostream>
using namespace std;
class MyClass
{
 int a, b, c;
public:
 MyClass(int a, int b, int c)
 {
 this->a = a;
 this->b = b;
 this->c = c;
 }
 void display()
 {
 cout << "a=" << a << " b=" << b << " c=" << c << endl;
 }
};
int main()
{
 int x, y, z;
 cin >> x >> y >> z;
 MyClass obj(x, y, z);
 obj.display();
 return 0;
}
```

# OUTPUT :
![image](https://github.com/user-attachments/assets/6f302ed5-9096-4323-b52e-716fcb77f823)

# RESULT :
Thus, The program is verified and executed successfully.The outputs match the expected 
results, confirming its correctness.

# 4d :

# PROGRAM STATEMENT :
Write a CPP program to demonstrate the use of a virtual destructor by properly destroying the 
objects of the parent and the child class.

# ALGORITHM :
1. Dynamically allocate memory for a Derived object using a Base pointer (Base* obj = new 
Derived()).
2. nvoke the Base class constructor, followed by the Derived class constructor, printing respective 
messages.
3. Use delete obj to free the allocated memory.
4. Call the Derived class destructor first, followed by the Base class destructor, printing respective 
messages.
5. Return from main() to terminate the program..

# PROGRAM :
```
#include <iostream>
using namespace std;
class Base
{
public:
 Base()
 {
 cout << "Constructing base" << endl;
 }
 
 virtual ~Base()
 {
 cout << "Destructing base" << endl;
 }
};
class Derived : public Base 
{
public:
 Derived()
 {
 cout << "Constructing derived" << endl;
 }
 ~Derived() 
 {
 cout << "Destructing derived" << endl;
 }
};
int main()
{
 Base* obj = new Derived(); 
 delete obj; 
 return 0;
}
```

# OUTPUT :
 ![image](https://github.com/user-attachments/assets/90f0efc5-85f6-4538-be2c-65775db455df)

# RESULT :
Thus, The program is verified and executed successfully.The outputs match the expected 
results, confirming its correctness.

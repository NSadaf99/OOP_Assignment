# OOP_Assignment
#include<iostream>
using namespace std;


class ClassA
{
    int a;
    int b;
public:
    ClassA()
    {
        a = 100;
        b = 200;
    }
    ~ClassA()
    {
    }
};

class ClassB
{
    int a;
    int b;
public:
    ClassB()
    {
        a = 500;
        b = 250;
    }


    ~ClassB()
    {
    }
};

class Derived:public ClassA, public ClassB
{
public:
    Derived() : ClassB(), ClassA()
    {
    }


    ~Derived()
    {
    }


    void Print_ab()
    {
        cout << "a: " << a << " b:" << b << endl;
    }
};


int main()
{
    Derived Ob1;
    Ob1.Print_ab();
    cin.ignore();
    return 0;
}

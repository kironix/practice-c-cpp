Sure! Here is a clean Markdown code block containing the full README section so you can copy & paste directly int# 📘 Java OOP — Exam Revision (Class, Object, Encapsulation, Inheritance)

A compact summary of essential OOP topics for exam preparation.  
Covers: **Class, Object, Constructors, Encapsulation, Access Modifiers, Inheritance, Method Overriding, this, super**.

---

## 🧱 1. Class & Object

### **Class**
A class is a blueprint/template for creating objects. It contains attributes and methods.

```java
class Student {
    String name;
    int id;

    void display() {
        System.out.println(name + " " + id);
    }
}

Object

An object is an instance of a class.

Student s = new Student();
s.name = "Shoaib";
s.id = 101;
s.display();


---

🔒 2. Encapsulation

Encapsulation = wrapping data + methods inside a class and restricting access using private variables.

class BankAccount {
    private String name;
    private double balance;

    public void setName(String n) { name = n; }
    public String getName() { return name; }

    public void setBalance(double b) { balance = b; }
    public double getBalance() { return balance; }
}


---

🔑 3. Access Modifiers

Modifier	Same Class	Same Package	Subclass	Other Package

private	✔️	❌	❌	❌
default	✔️	✔️	❌	❌
protected	✔️	✔️	✔️	❌
public	✔️	✔️	✔️	✔️



---

🏗️ 4. Constructors

Default Constructor

A() {
    System.out.println("Default constructor");
}

Parameterized Constructor

A(int a) {
    x = a;
}

Constructor Overloading

class Box {
    double w, h, d;

    Box() { w = h = d = -1; }

    Box(double len) { w = h = d = len; }

    Box(double w, double h, double d) {
        this.w = w;
        this.h = h;
        this.d = d;
    }
}


---

🟦 5. this Keyword

Use cases:

🔹 Refer instance variable

this.name = name;

🔹 Call a method

this.show();

🔹 Call another constructor

A() { this(5); }
A(int x) { System.out.println(x); }


---

🧬 6. Inheritance

Inheritance allows one class to acquire the properties & methods of another class.

class Child extends Parent { }


---

🐶 Single Inheritance

class Animal {
    void eat(){ System.out.println("eating"); }
}

class Dog extends Animal {
    void bark(){ System.out.println("barking"); }
}


---

🍼 Multilevel Inheritance

class Animal { void eat(){ System.out.println("eat"); } }
class Dog extends Animal { void bark(){ System.out.println("bark"); } }
class BabyDog extends Dog { void weep(){ System.out.println("weep"); } }


---

🌲 Hierarchical Inheritance

class Animal { void eat(){ System.out.println("eat"); } }
class Cat extends Animal { void meow(){ System.out.println("meow"); } }
class Dog extends Animal { void bark(){ System.out.println("bark"); } }


---

🔁 7. Method Overriding (Runtime Polymorphism)

Subclass redefines a method from the parent class.

class Animal {
    void eat() { System.out.println("I can eat"); }
}

class Dog extends Animal {
    @Override
    void eat() {
        System.out.println("I eat dog food");
    }
}


---

🟪 8. super Keyword

Used to call parent method or constructor.

class Animal {
    void eat(){ System.out.println("Animal eating"); }
}

class Dog extends Animal {
    void eat(){
        super.eat();   // parent method call
        System.out.println("Dog eating");
    }
}


---

📚 9. Object Passing

class Test {
    int a;
    Test(int a){ this.a = a; }

    Test increase() {
        return new Test(a + 10);
    }
}


---

🧹 10. Garbage Collection Basics

An object becomes eligible for GC when no reference points to it.

Employee e = new Employee();
e = null; // ready for GC


---

✅ End of README

Good luck on your exam! 🚀

---

If you want a shorter / cleaner / more advanced version, I can generate that too.

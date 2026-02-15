# OOP

## 📖 Introduction

Object-Oriented Programming (OOP) is a programming paradigm based on the concept of objects, which contain:

- Data (properties)
- Behavior (methods)

TypeScript enhances JavaScript by adding static typing and structured OOP features, making it ideal for scalable applications.

## 🧠 Core OOP Principles

1. Classes
2. Encapsulation
3. Abstraction
4. Inheritance
5. Polymorphism

### 1️⃣ Classes

A class is a blueprint for creating objects.

```ts
class User {
  constructor(
    public name: string,
    private age: number,
  ) {}

  greet(): string {
    return `Hello ${this.name}`;
  }
}

``;
```

### 2️⃣ Encapsulation

Encapsulation restricts direct access to object data.

```ts
class BankAccount {
  private balance: number = 0;

  deposit(amount: number) {
    this.balance += amount;
  }

  getBalance(): number {
    return this.balance;
  }
}
```

### 🔐 Access Modifiers

TypeScript provides real access control:
| Modifier | Scope |
| ----------- | --------------------------------------- |
| `public` | Accessible everywhere |
| `private` | Accessible only inside the class |
| `protected` | Accessible inside class and subclasses |
| `readonly` | Cannot be modified after initialization |

### 3️⃣ Abstraction

Abstraction hides implementation details.

```ts
abstract class Payment {
  abstract process(): void;

  log() {
    console.log("Processing payment...");
  }
}
```

### 4️⃣ Inheritance

Allows a class to inherit properties and methods from another class.

```ts
class Animal {
  speak() {
    console.log("Animal makes sound");
  }
}

class Dog extends Animal {
  speak() {
    console.log("Dog barks");
  }
}
```

### 5️⃣ Polymorphism

Polymorphism allows methods to behave differently based on the object.

```ts
class Shape {
  area(): number {
    return 0;
  }
}

class Circle extends Shape {
  constructor(private radius: number) {
    super();
  }

  area(): number {
    return Math.PI * this.radius ** 2;
  }
}
```

### 🧩 Interfaces

Interfaces define contracts for classes.

```ts
interface Flyable {
  fly(): void;
}

class Bird implements Flyable {
  fly() {
    console.log("Flying...");
  }
}
```

### 🏗 Abstract Classes

Abstract classes can contain:

- Abstract methods (must be implemented)
- Concrete methods (already implemented)

```ts
abstract class Vehicle {
  abstract move(): void;

  start() {
    console.log("Vehicle started");
  }
}
```

### ⚙ Static Members

Belong to the class itself, not instances.

```ts
class MathUtil {
  static PI = 3.14;

  static square(x: number): number {
    return x * x;
  }
}
```

### 🔄 Getters & Setters

Control how properties are accessed or modified.

```ts
class Person {
  private _age: number = 0;

  get age(): number {
    return this._age;
  }

  set age(value: number) {
    if (value > 0) {
      this._age = value;
    }
  }
}
```

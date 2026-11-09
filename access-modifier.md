# Access Modifiers in TypeScript OOP

## Introduction

Access modifiers in TypeScript help us control how class properties and methods can be accessed or modified. They make our code more organized, secure, and easier to maintain.

TypeScript provides four commonly used modifiers: `public`, `private`, `protected`, and `readonly`.

## 1. Public

`public` members can be accessed from anywhere, both inside and outside the class. It's the default modifier in TypeScript.

```ts
class Person {
  public name: string = "Nayem";
}

const person = new Person();
console.log(person.name); // Nayem
```

## 2. Private

`private` members can only be accessed inside their own class. We cannot access them directly from outside the class or from child classes.

```ts
class BankAccount {
  private balance: number = 5000;

  getBalance(): number {
    return this.balance;
  }
}

const account = new BankAccount();
console.log(account.getBalance()); // 5000
```

## 3. Protected

`protected` members can be accessed inside their own class and its child classes, but not directly from outside.

```ts
class Person {
  protected name: string = "Nayem";
}

class Employee extends Person {
  getName(): string {
    return this.name;
  }
}

const employee = new Employee();
console.log(employee.getName()); // Nayem
```

## 4. Readonly

`readonly` properties can be assigned a value when declared or inside the constructor. After initialization, their values cannot be changed.

```ts
class User {
  readonly id: number;

  constructor(id: number) {
    this.id = id;
  }
}

const user = new User(101);
console.log(user.id); // 101

// user.id = 102; // Error: Cannot assign to readonly property
```

## Conclusion

Each modifier has a different purpose:

- `public`: Accessible from anywhere.
- `private`: Accessible only inside the same class.
- `protected`: Accessible inside the class and its child classes.
- `readonly`: Can be initialized but cannot be reassigned afterward.

Understanding these modifiers helps us write better structured and more maintainable TypeScript OOP code.

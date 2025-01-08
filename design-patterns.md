# 10 Design Patterns in 10 Minutes

This doc will focus on the following design patterns, along with their pros and cons...

![](images/{17056A14-5BE1-4D4D-B459-9B42B2375186}.png)

### "Design Patterns - Elements of reusable Object-Oriented Software"

One of the most influential books in the history of programming is "Design Patterns"...

![](images/{A5DB9EC3-DBF1-44AC-96C0-926DFEAF7F98}.png)

...written by 4 C++ engineers called "The Gang of Four"...

![](images/{F25B5C7D-1A7D-4C79-BEE3-D28BA235C2AC}.png)

The book breaks down 23 different approaches to address recurring problems that programmers face, which are categorized as...

- **Creational Patterns:** how objects are created
- **Structural Patterns:** how objects relate to each other 
- **Behavioural Patterns:** how objects communicate with each other 

<br>

Becoming a proficient software engineer isn't about memorizing the syntax of a programming language, but rather the ability to solve problems with it.

![alt text](images/{67BE2975-804B-4BB5-A2F5-D9976632DDB7}.png)

<br>

**Additional Resources:** 

Refactoring Guru:
https://refactoring.guru/

- Excellent educational site with great graphics that explain design patterns - used throughout these notes

<br><br>

### Patterns are not algorithms

Design patterns are not just like algorithms that you can copy/paste from Stack Overflow or ChatGPT. You have to use thought and consideration to implement them correctly.  

Patterns are often confused with algorithms, because both concepts describe typical solutions to some known problems. While an algorithm always defines a clear set of actions that can achieve some goal, a pattern is a more high-level description of a solution. The code of the same pattern applied to two different programs may be different.

### Patterns are not a solution for everything...

It can be tempting to implement them everywhere, but when used improperly they can add unnecessary complexity and boilerplate to a codebase.

![alt text](images/{1354F420-5F9E-4261-B61B-2D7FF58ACC86}.png)

Important to note also that the "Design Patterns" book is not the bible - and many people have criticized it! 

Regardless, knowing how to recognize design patterns will help you level up as a programmer! 

<br><br>

## Pattern 1: **Singleton** 

![](images/{E37376A7-FE1C-438E-B5C9-4AD3AC0CA8A4}.png)

![alt text](images/{0D9B0473-77B9-4329-B7B5-A8E7D8288957}.png)

**Singleton** is a type of object that can only be instantiated **ONCE**. 

In TS, we might implement a singleton class called "`Settings`", to represent the global app settings data. 

Give it a `static` `instance` property, and make its `constructor` `private`, so that it can't be instantiated with the `new` keyword.

![alt text](images/{D6938CAF-D2BE-4337-8AF6-DA57E081914E}.png)

We then create a `static` `getInstance()` method that will check to see if the instance has already been created, and if not it will create a new one. **This ensures that only one object with that name can be created.**

![alt text](images/{C7F37CBB-0560-48F6-AC35-CCF9B3C83BB5}.png)

*But here's where things become a little more nuanced...* 

In JS we have **object literals** and also the concept of **global data**. And objects are passed around by reference. 

We get all the same basic characteristics of the **singleton** pattern by simply creating a global object. 

![alt text](images/{9FDCBFA1-7AFF-4943-AB38-41581C79ACD8}.png)

The pattern itself is really just extra boilerplate that we don't need.

It's an entirely different story in C++ - *different language, different story* - but the moral of the story is to lean on your language's built-in features before implementing a fancy design pattern. 

<br><br>

### Pattern 2: **Prototype** | AKA Clone

![alt text](images/{E67B9F32-55BB-4CD9-857F-A315915ED24E}.png)

![alt text](images/{9DB31707-16F2-45CE-B20F-E76E80A9AD3A}.png)

If you've done Object Oriented Programming (OOP), you'll be familiar with inheritance, where a `class` can be extended with a sub-class.

![alt text](images/{112C2AFE-0F4A-45AB-8F43-A16325CD7A23}.png)

One problem with inheritance is that it can lead to a complex hierarchy of code. 

![alt text](images/{29C8F297-05E1-4C65-A5D1-CF4257BFCEC4}.png)

The prototype pattern is an alternative way to implement inheritance, but instead of inheriting functionality from a class it comes from an object that's already been created. 

This creates a flat prototype chain that makes it much easier to share functionality between objects, especially in a dynamic language like JS, which supports prototypal inheritance out of the box.

![alt text](images/{28B0031F-D0B9-4F3A-B87A-870B0C08B090}.png)

<br>

Imagine we have an `object` named `zombie` - this is the *prototype*.

![alt text](images/{B59BFFFD-CDC1-4D84-8286-044F263D519B}.png)

Now we want to create a new `object` based on `zombie`, that also has a name. We can do that with `Object.create(zombie)` - this is the *clone*.

![alt text](images/{5FEF5B3B-8912-4846-A31D-4D092E726ECF}.png)

Can then pass additional properties to the clone, such as `name` etc.

![alt text](images/{B44B9B2A-AB56-4BD0-A15F-EB3612B60755}.png)

<br>

The interesting thing is, if you `console.log(chad)`, you will only see the name, and not the `eatBrains()` method...

![alt text](images/{A01C4044-9F6D-4449-A931-DDF9C87CC3EA}.png)

...however, if you try to call that method on `chad` **it will work**! 

![alt text](images/{1DF7D37C-A462-439D-9E43-7E40BCC6A2B4}.png)

That's because JS will go up the prototype chain until it reaches the root, looking for any methods or properties on the parent objects.

<br>

You can always get the prototype from an object using the `__proto__` property. However, that's not a modern best practice and instead you should use `Object.getPrototypeOf()`. 

![alt text](images/{FCA08078-3B19-4E09-AEC3-B1E8D94D1242}.png)

<br>

### Classes in JS

When it comes to **classes** in JS, `prototype` refers to its `constructor`. 

That means we can extend a class with additional functions if we want to, however that's also generally considered bad practice. 

![alt text](images/{A5E7E118-88D3-4167-B434-3C7CE1DA3947}.png)

![alt text](images/{8EF6EAD5-6192-4D77-9930-85686D316F5C}.png)




<br><br>

### Pattern 3: **Builder**

![alt text](images/{FB43D9F4-BEA4-4C80-904A-2D116BBCE28A}.png)

![alt text](images/{69C35C12-4E27-4756-805B-DBB3005D2E46}.png)

Imagine you're running a hot dog stand and when a customer places an order they need to tell you everything they want on the sandwich in a `constructor`.

 ![alt text](images/{E82E3940-8A9B-4953-88E7-CD0A567A42B2}.png)

 That works, but it's kind of hard to keep track of all these options and we may want to defer each step to a later point.

 With the **builder** pattern, we create the object step-by-step using `methods`, rather than the `constructor`. And we can even delegate the building logic to an entirely different class.

 ![alt text](images/{8867533E-4B03-4AF1-870A-34E1B4E9446C}.png)

 In JS, we'd have each method return `this`, which is a reference to the object instance. 

 ![alt text](images/{E1EC0A81-C1C8-4F61-B92E-A80DDB5BCA3C}.png)

 That allows us to implement method chaining, where we instantiate an object, then chain methods to it, but always get the object as the return value. 

 ![alt text](images/{91C7933D-CE90-44A8-B608-103EE9623354}.png)

 You'll come across this pattern frequently with libraries like jQuery - although its gone out of style in recent years! 

 <br><br>



 ### Pattern 4: **Factory**

 to be continued...
# System 5 - Advanced JavaScript

## Chapter # Table of Contents

- [Chapter 1 - HTTP Fundamentals]()
- [Chapter 2 - Promises]()
- [Chapter 3 - Web APIs & Axios]()
- [Chapter 4 - Conversions & Coercions]()
- [Chapter 5 - Objects & Constructors]()
- [Chapter 6 - Classes]()
- [Chapter 7 - JavaScript Components]()
- [Chapter 8 - Program Hackathon]()

## Chapter 5 - Objects & Constructors

### Primitives vs Objects

- **All** values in JavaScript can be divided into 2 categories: primitives and objects
  - Primitives
    - Strings
    - Numbers
    - Booleans
  - Objects
    - Objects
    - Arrays
    - Math
    - Window/Document
    - Object we create

## Chapter 7 - Classes

### Learning Objectives

- Compare classes with prototypes
- Apply classes to take full advantage of their features
- Pass methods into higher order functions

### Prototypes and Classes

**Classes** are another way of writing prototypes and constructor functions. Classes are *syntactic sugar* in relation to protoypes

function Person (name, age, height) {
  this.name = name;
  this.age = age;
  this.height = height;

  this.sayHello = () => {
    return 'Hi my name is ' + this.name;
  }
}

### Review Questions

1. Explain hoisting in relation to functions and classes. *Classes are not hoisted and need to be declared first before calling them or any methods/functions within them.*
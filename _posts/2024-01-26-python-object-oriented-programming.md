---
layout: post
title:  A Beginner’s Guide to Python Object-Oriented Programming (OOP)
date:   2024-01-26 00:00:00 -0800
description:
author: horacio 
image:  '/images/python.png'
tags:   [technology, coding]
tags_color: '#477690'
---

Programming is an art. And as in art, selecting the proper brushes and paints is essential to produce the best works. Python Object-Oriented Programming is one such skill.

Choosing [the right programming language](/blog/best-programming-language-to-learn) is a crucial part of any project, and it can lead either to a fluid and enjoyable development or a complete nightmare. Hence, it would be best if you used the best-fit language for your use case.

That’s the primary reason to learn object-oriented programming in Python, which is also one of the most popular programming languages.

Let’s learn!

### Table of Contents

1.  [An Example Python Program](#an-example-python-program)
2.  [Requirements to Learn Python OOP](#requirements-to-learn-python-oop)
3.  [What Is Object-Oriented Programming in Python?](#what-is-objectoriented-programming-in-python)
4.  [Why Do We Use Object-Oriented Programming in Python?](#why-do-we-use-objectoriented-programming-in-python)
5.  [Everything Is an Object in Python](#everything-is-an-object-in-python)
6.  [Your First Object in Python](#your-first-object-in-python)
7.  [The 4 Pillars of OOP in Python](#the-4-pillars-of-oop-in-python)
8.  [Build an Area Shape Resolver Calculator](#build-an-area-shape-resolver-calculator)

An Example Python Program[](#an-example-python-program)
-------------------------------------------------------

Before digging into the matter, let us pose a question: have you ever written a Python program like the one below?

    secret_number = 20
     
    while True:
       number = input('Guess the number: ')
     
       try:
           number = int(number)
       except:
           print('Sorry that is not a number')
           continue
     
       if number != secret_number:
           if number > secret_number:
               print(number, 'is greater than the secret number')
     
           elif number < secret_number:
               print(number, 'is less than the secret number')
       else:
           print('You guessed the number:', secret_number)
           break
    

This code is a simple number guesser. Try to copy it in a Python file and run it in your system. It perfectly accomplishes its purpose.

But here comes a huge problem: what if we asked you to implement a new feature? It could be something simple — for instance:

“If the input is a multiple of the secret number, give the user a hint.”

The program would quickly grow complex and heavy as you increase the number of features and, therefore, the total number of nested conditionals.

That’s precisely the problem object-oriented programming tries to solve.

Requirements to Learn Python OOP[](#requirements-to-learn-python-oop)
---------------------------------------------------------------------

Before heading into object-oriented programming, we strongly recommend you have a firm grasp of Python basics.

*   **Variable:** Symbolic name that points to a specific object (we’ll see what **objects** mean through the article).

*   **Arithmetic operators:** Addition (+), subtraction (-), multiplication (\*), division (), integer division (/), modulo (%).

*   **Built-in data types:** Numeric (integers, floats, complex), Sequences (strings, lists, tuples), Boolean (True, False), Dictionaries, and Sets.

*   **Boolean expressions:** Expressions in which the result is **True** or **False.**

*   **Conditional:** Evaluates a boolean expression and does some process depending on the result. Handled by **if/else** statements.

*   **Loop:** Repeated execution of code blocks. It can be **for** or **while** loops.

*   **Functions:** Block of organized and reusable code. You create them with the keyword **def**.

*   **Arguments:** Objects passed to a function. For instance: `sum([1, 2, 4])`

*   **Run a Python script**: Open a terminal or command line and type “python <name of the file>.”

*   **Open a Python Shell**: Open a terminal and type `python` or `python3` depending on your system.

Now you have these concepts crystal clear, you can move forward with understanding object-oriented programming.

What Is Object-Oriented Programming in Python?[](#what-is-objectoriented-programming-in-python)
-----------------------------------------------------------------------------------------------

Object-Oriented Programming (OOP) is a programming paradigm in which we can think about complex problems as objects.

A paradigm is a theory that supplies the base for solving problems.

So when we’re talking about OOP, we’re referring to a set of concepts and patterns we use to solve problems with objects.

An object in Python is a single collection of data (attributes) and behavior (methods). You can think of objects as real things around you. For example, consider calculators:

A calculator can be an object.

As you may notice, the data (attributes) are always nouns, while the behaviors (method) are always verbs.

This compartmentalization is the central concept of Object-Oriented Programming. You build objects that store data and contain specific kinds of functionality.

Why Do We Use Object-Oriented Programming in Python?[](#why-do-we-use-objectoriented-programming-in-python)
-----------------------------------------------------------------------------------------------------------

OOP allows you to create secure and reliable software. Many Python frameworks and libraries use this paradigm to build their codebase. Some examples are Django, Kivy, pandas, NumPy, and TensorFlow.

Let’s see the main advantages of using OOP in Python.

### Advantages of Python OOP[](#advantages-of-python-oop)

The following reasons will make you opt for using object-oriented programming in Python.

#### All Modern Programming Languages Use OOP[](#all-modern-programming-languages-use-oop)

This paradigm is language-independent. If you learn OOP in Python, you’ll be able to use it in the following:

*   Java
*   PHP (make sure to read the comparison between PHP and Python)
*   Ruby
*   Javascript
*   C#
*   Kotlin

All of these languages are either natively object-oriented or include options for object-oriented functionality. If you want to learn any of them after Python, it’ll be easier — you’ll find many similarities between languages working with objects.

#### OOP Allows You to Code Faster[](#oop-allows-you-to-code-faster)

Coding faster doesn’t mean writing fewer lines of code. It means you can implement more features in less time without compromising the stability of a project.

Object-Oriented programming allows you to reuse code by implementing [abstraction](#1-abstraction). This principle makes your code more concise and legible.

As you may know, programmers spend much more time reading code than writing it. It’s the reason legibility is always more important than getting features out as quickly as possible.

Productivity decreases with not legible code

You’ll see more about the abstraction principle later.

#### OOP Helps You Avoid Spaghetti Code[](#oop-helps-you-avoid-spaghetti-code)

Do you remember the number guesser program at the start of this article?

If you keep adding features, you’ll have many nested **if** statements in the future. This tangle of endless lines of code is called spaghetti code, and you should avoid it as much as possible.

OOP gives us the possibility of compressing all the logic in objects, therefore avoiding long pieces of nested **if’s**.

#### OOP Improves Your Analysis of Any Situation[](#oop-improves-your-analysis-of-any-situation)

Once you get some experience with OOP, you’ll be able to think of problems as small and specific objects.

This understanding leads to a rapid project initialization.

### Structured Programming vs Object-Oriented Programming[](#structured-programming-vs-objectoriented-programming)

Structured programming is the most-used paradigm by beginners because it is the simplest way to build a small program.

It involves running a Python program sequentially. That means you’re giving the computer a list of tasks and then executing them from top to bottom.

Let’s see an example of structured programming with a coffee shop program.

    small = 2
    regular = 5
    big = 6
     
    user_budget = input('What is your budget? ')
     
    try:
       user_budget = int(user_budget)
    except:
       print('Please enter a number')
       exit()
     
    if user_budget > 0:
       if user_budget >= big:
           print('You can afford the big coffee')
           if user_budget == big:
               print('It\'s complete')
           else:
               print('Your change is', user_budget - big)
       elif user_budget == regular:
           print('You can afford the regular coffee')
           print('It\'s complete')
       elif user_budget >= small:
           print('You can buy the small coffee')
           if user_budget == small:
               print('It\'s complete')
           else:
               print('Your change is', user_budget - small)
    

The code above acts as a coffee shop vendor. It’ll ask you for a budget, then “sell” you the biggest coffee you’re capable of buying.

Try to run it in the terminal. It’ll execute step by step, depending on your input.

This code works perfectly, but we have three problems:

1.  It has a lot of repeated logic.
2.  It uses many nested **if** conditionals.
3.  It’ll be hard to read and modify.

OOP was invented as a solution to all of these problems.

Let’s see the above program implemented with OOP. Don’t worry if you don’t understand it yet. It’s only for comparing structured programming and object-oriented programming.

    class Coffee:
            # Constructor
            def __init__(self, name, price):
                    self.name = name
                    self.price = float(price)
            def check_budget(self, budget):
                    # Check if the budget is valid
                    if not isinstance(budget, (int, float)):
                            print('Enter float or int')
                            exit()
                    if budget < 0: 
                        print('Sorry you don\'t have money') 
                        exit() 
            def get_change(self, budget):
                    return budget - self.price
            
            def sell(self, budget):
                    self.check_budget(budget)
                    if budget >= self.price:
                            print(f'You can buy the {self.name} coffee')
                            if budget == self.price:
                                    print('It\'s complete')
                            else:
                                    print(f'Here is your change {self.get_change(budget)}$')
    
                            exit('Thanks for your transaction')
    

**Note:** All the following concepts will be explained deeper through the article.

The above code represents a **class** named “Coffee.” It has two attributes — “name” and “price” — and they’re both used in the methods. The primary method is “sell,” which processes all the logic needed to complete the selling process.

If you try to run that class, you won’t get any output. It primarily occurs because we’re just declaring the “template” for the coffees, not the coffees themselves.

Let’s implement that class with the following code:

    small = Coffee('Small', 2)
    regular = Coffee('Regular', 5)
    big = Coffee('Big', 6)
     
    try:
       user_budget = float(input('What is your budget? '))
    except ValueError:
       exit('Please enter a number')
      
    for coffee in [big, regular, small]:
       coffee.sell(user_budget)
    

Here we’re making **instances,** or coffee objects, of the class “Coffee,” then calling the “sell” method of each coffee until the user can afford any option.

We’ll get the same output with both approaches, but we can extend the program functionality far better with OOP.

Below is a table comparing object-oriented programming and structured programming:

**OOP**

**Structured Programming**

Easier to maintain

Hard to maintain

Don’t Repeat Yourself (DRY) approach

Repeated code in many places

Little pieces of code reused in many places

A large amount of code in few places

Object approach

Block code approach

Easier to debug

Harder to debug

Big learning curve

Simpler learning curve

Used in large projects

Optimized to simple programs

To conclude the paradigm comparison:

*   Neither paradigm is perfect (OOP can be overwhelming to use in simple projects).
*   These are just two ways of solving a problem; there are others out there.
*   OOP is used in large codebases, while structured programming is mainly for simple projects.

Let’s move on to built-in objects in Python.

Everything Is an Object in Python[](#everything-is-an-object-in-python)
-----------------------------------------------------------------------

We’ll tell you a secret: you’ve been using OOP all the time without noticing it.

Even when using other paradigms in Python, you still use objects to do almost everything.

That’s because, in Python, _everything_ is an object.

Remember the definition of object: An object in Python is a single collection of data (attributes) and behavior (methods).

That matches any data type in Python.

A string is a collection of data (characters) and behaviors (**upper()**, **lower()**, etc..). The same applies to **integers**, **floats**, **booleans**, **lists,** and dictionaries.

Before continuing, let’s review the meaning of attributes and methods.

### Attributes and Methods[](#attributes-and-methods)

Attributes are internal **variables** inside objects, while methods are **functions** that produce some behavior.

Let’s do a simple exercise in the Python shell. You can open it by typing `python` or `python3` in your terminal.

Python shell

Now, let’s work with the Python shell to discover methods and types.

    >>> python = 'python, Premium Application, Database, and Managed WordPress hosting'
    >>> python.upper()
    'python, PREMIUM APPLICATION, DATABASE, AND MANAGED WORDPRESS HOSTING'
    

In the second line, we’re calling a string method, **upper()**. It returns the content of the string all in uppercase. However, it doesn’t change the original variable.

    >>> python
    'python, Premium Application, Database, and Managed WordPress hosting'
    

Let’s delve into valuable functions when working with objects.

The **type()** function allows you to get the type of an object. The “type” is the class to which the object belongs.

    >>> type(python)
    # class 'str'
    

The **dir()** function returns all the attributes and methods of an object. Let’s test it out with the **python** variable.

    >>> dir(python)
    ['__add__', '__class__',  ........... 'upper', 'zfill']
    

Now, try to print some of the hidden attributes of this object.

     >>> python.__class__ # class ‘str’ e>

This will output the class the object **python** belongs to. So we can say the only thing the **type** function returns is the **\_\_class\_\_** attribute of an object.

You can experiment with all the data types, discovering all of their attributes and methods directly on the terminal. You can learn more about the built-in data types in the [official documentation](https://docs.python.org/3/library/stdtypes.html).

Your First Object in Python[](#your-first-object-in-python)
-----------------------------------------------------------

A **class** is like a template**.** It allows you to create custom objects based on the attributes and methods you define.

You can think of it as a **cookie-cutter** that you modify to bake the perfect cookies (objects, not tracking cookies), with defined characteristics: Shape, Size, and more.

On the other hand, we have **instances.** An instance is an individual object of a class, which has a unique memory address.

Instances in Python

Now that you know what classes and instances are, let’s define some!

To define a class in Python, you use the **class** keyword, followed by its name. In this case, you’ll create a class named **Cookie**.

**Note:** In Python, we use the [camel case name convention](https://en.wikipedia.org/wiki/Camel_case#:~:text=Camel%20case%20(sometimes%20stylized%20as,word%20starting%20with%20either%20case.) to name classes.

    class Cookie:
    	pass
    

Open your Python shell and type the code above. To create an instance of a class, just type its name and parenthesis after it. It’s the same process as invoking a function.

    cookie1 = Cookie()
    

Congratulations — you’ve just created your first object in Python! You can check its id and type with the following code:

    id(cookie1)
    140130610977040 # Unique identifier of the object
    
    type(cookie1)
    <class '__main__.Cookie'>
    

As you can see, this cookie has a unique identifier in memory, and its type is **Cookie**.

You can also check if an object is an instance of a class with the **isinstance()** function.

    isinstance(cookie1, Cookie)
    # True
    isinstance(cookie1, int)
    # False
    isinstance('a string', Cookie)
    # False
    

### Constructor Method[](#constructor-method)

The **\_\_init\_\_()** method is also named “constructor.” It’s called Python each time we instantiate an object.

The constructor creates the object’s initial state with the minimum set of parameters it needs to exist. Let’s modify the **Cookie** class, so it accepts parameters in its constructor.

    class Cookie:
    	# Constructor
    	def __init__(self, name, shape, chips='Chocolate'):
    		# Instance attributes
    		self.name = name
    		self.shape = shape
    		self.chips = chips
    

In the **Cookie** class, every cookie must have a name, shape, and chips. We’ve defined the last one as “Chocolate.”

On the other hand, **self** refers to the instance of the class (the object itself).

Try to paste the class in the shell and create an instance of the cookie as usual.

    cookie2 = Cookie()
    # TypeError
    

You’ll get an error. That’s because you must provide the minimal set of data the object needs to live — in this case, **name** and **shape** since we’ve already set **chips** to “Chocolate.”

    cookie2 = Cookie('Awesome cookie', 'Star')
    

To access the attributes of an instance, you must use the dot notation.

    cookie2.name
    # 'Awesome cookie'
    cookie2.shape
    # 'Star'
    cookie2.chips
    # 'Chocolate'
    

For now, the **Cookie** class doesn’t have anything too juicy. Let’s add a sample method **bake()** to make things more interesting.

    class Cookie:
    	# Constructor
    	def __init__(self, name, shape, chips='Chocolate'):
    		# Instance attributes
    		self.name = name
    		self.shape = shape
    		self.chips = chips
    
    	# The object is passing itself as a parameter
    	def bake(self):
    		print(f'This {self.name}, is being baked with the shape {self.shape} and chips of {self.chips}')
    		print('Enjoy your cookie!')
    

To call a method, use the dot notation and invoke it as a function.

    cookie3 = Cookie('Baked cookie', 'Tree')
    cookie3.bake()
    # This Baked cookie, is being baked with the shape Tree and chips of Chocolate
    Enjoy your cookie!
    

The 4 Pillars of OOP in Python[](#the-4-pillars-of-oop-in-python)
-----------------------------------------------------------------

Object-Oriented Programming includes four main pillars:

#### 1\. Abstraction[](#1-abstraction)

Abstraction hides the internal functionality of an application from the user. The user could be either the end client or other developers.

We can find **abstraction** in our daily lives. For example, you know how to use your phone, but you probably don’t know exactly what’s happening inside it each time you open an app.

Another example is Python itself. You know how to use it to build functional software, and you can do it even if you don’t understand Python’s inner workings.

Applying the same to code allows you to collect all the objects in a problem and **abstract** standard functionality into classes.

#### 2\. Inheritance[](#2-inheritance)

Inheritance allows us to define multiple **subclasses** from an already defined class.

The primary purpose of it is to follow the [DRY principle](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself). You’ll be able to reuse a lot of code by implementing all the sharing components into **superclasses**.

You can think of it as the real-life concept of **genetic inheritance**. Children (subclass) are the result of inheritance between two parents (superclasses). They inherit all the physical characteristics (attributes) and some common behaviors (methods).

#### 3\. Polymorphism[](#3-polymorphism)

Polymorphism lets us slightly modify methods and attributes of the **subclasses** previously defined in the **superclass**.

The literal meaning is “**many forms**.” That’s because we build methods with the same name but different functionality.

Going back to the previous idea, children are also a perfect example of polymorphism. They can inherit a defined behavior **get\_hungry()** but in a slightly different way, for instance, getting hungry every 4 hours instead of every 6.

#### 4\. Encapsulation[](#4-encapsulation)

Encapsulation is the process in which we protect the internal integrity of data in a class.

Although there isn’t a **private** statement in Python, you can apply encapsulation by using [mangling in Python](https://en.wikipedia.org/wiki/Name_mangling#Python). There are special methods named **getters** and **setters** that allow us to access unique attributes and methods.

Let’s imagine a **Human** class that has a unique attribute named **\_height**. You can modify this attribute only within certain constraints (it’s nearly impossible to be higher than 3 meters).

Build an Area Shape Resolver Calculator[](#build-an-area-shape-resolver-calculator)
-----------------------------------------------------------------------------------

One of the best things about Python is that it lets us create a wide variety of software, from a CLI (command-line interface) program to a complex web app.

Now that you’ve learned the pillar concepts of OOP, it’s time to apply them to an actual project.

Your task is to create an area calculator of the following shapes:

*   Square
*   Rectangle
*   Triangle
*   Circle
*   Hexagon

### Shape Base Class[](#shape-base-class)

Firstly, create a file **calculator.py** and open it. Since we already have the objects to work with, it’ll be easy to **abstract** them in a class.

You can analyze the common characteristics and find out that all of these are **2D shapes**. Therefore, the best option is to create a class **Shape** with a method **get\_area()** from which each shape will inherit.

**Note:** All the methods should be verbs. That’s because this method is named **get\_area()** and not **area()**.

    class Shape:
    	def __init__(self):
    		pass
    
    	def get_area(self):
    		pass
    

The code above defines the class; however, there isn’t anything interesting in it yet.

Let’s implement the standard functionality of most of these shapes.

    class Shape:
    	def __init__(self, side1, side2):
    		self.side1 = side1
    		self.side2 = side2
    
    	def get_area(self):
    		return self.side1 * self.side2
    
    	def __str__(self):
    		return f'The area of this {self.__class__.__name__} is: {self.get_area()}'
    

Let’s break down what we’re doing with this code:

*   In the **\_\_init\_\_** method, we’re requesting two parameters, **side1** and **side2**. These will remain as **instance attributes**.
*   The **get\_area()** function returns the area of the shape. In this case, it’s using the formula of area of a rectangle since it’ll be easier to implement with other shapes.
*   The **\_\_str\_\_()** method is a “magic method” just as **\_\_init\_\_().** It allows you to modify the way an instance will print.
*   The **self.\_\_class\_\_.\_\_name\_\_** hidden attribute refers to the name of the class. If you were working with a **Triangle** class, that attribute would be “Triangle.”

### Rectangle Class[](#rectangle-class)

Since we implemented the formula of area of the Rectangle, we could create a simple **Rectangle** class that does nothing but inherit from the **Shape** class.

To apply **inheritance** in Python, you’ll create a class as usual and surround the **superclass** you want to inherit from by parenthesis.

    # Folded base class
    class Shape: ...
     
    class Rectangle(Shape): # Superclass in Parenthesis
    	pass
    

### Square Class[](#square-class)

We can take an excellent approach to **polymorphism** with the **Square** class.

Remember that a square is just a rectangle whose four sides are all equal. That means we can use the same formula to get the area.

We can do this by modifying the **init** method, accepting only a **side** as a parameter, and passing that side value to the constructor of the **Rectangle** class.

    # Folded classes
    class Shape: ...
    class Rectangle(Shape): ...
     
    class Square(Rectangle):
    	def __init__(self, side):
    		super().__init__(side, side)
    

As you can see, the [super function](https://docs.python.org/3/library/functions.html#super) passes the **side** parameter twice to the **superclass**. In other words, it’s passing **side** both as **side1** and **side2** to the previously defined constructor.

### Triangle Class[](#triangle-class)

A triangle is half as big as the rectangle that surrounds it.

Relation between triangles and rectangles (Image source: Varsity tutors).

Therefore, we can inherit from the **Rectangle** class and modify the **get\_area** method to match the triangle area formula, which is one-half of the base multiplied by the height.

    # Folded classes
    class Shape: ...
    class Rectangle(Shape): ...
    class Square(Rectangle): ...
     
    class Triangle(Rectangle):
    	def __init__(self, base, height):
    		super().__init__(base, height)
     
    	def get_area(self):
    		area = super().get_area()
    		return area / 2
    

Another use case of the **super()** function is to call a method defined in the **superclass** and store the result as a variable. That’s what’s happening inside the **get\_area()** method.

### Circle Class[](#circle-class)

You can find the circle area with the formula **πr²**, where **r** is the circle’s radius. That means we have to modify the **get\_area()** method to implement that formula.

**Note:** We can import the approximate value of **π** from the math module

    # Folded classes
    class Shape: ...
    class Rectangle(Shape): ...
    class Square(Rectangle): ...
    class Triangle(Rectangle): …
     
    # At the start of the file
    from math import pi
     
    class Circle(Shape):
    	def __init__(self, radius):
    		self.radius = radius
     
    	def get_area(self):
    		return pi * (self.radius ** 2)
    

The code above defines the **Circle** class, which uses a different constructor and **get\_area()** methods.

Although **Circle** inherits from the **Shape** class, you can redefine every single method and attribute it to your liking.

### Regular Hexagon Class[](#regular-hexagon-class)

We only need the length of a side of a regular hexagon to calculate its area. It’s similar to the **Square** class, where we only pass an argument to the constructor.

Hexagon area formula (Image source: BYJU’S)

However, the formula is quite different, and it implies the use of a square root. That’s why you’ll use the **sqrt()** function from the math module.

    # Folded classes
    class Shape: ...
    class Rectangle(Shape): ...
    class Square(Rectangle): ...
    class Triangle(Rectangle): …
    class Circle(Shape): …
     
    # Import square root
    from math import sqrt
     
    class Hexagon(Rectangle):
    	
    	def get_area(self):
    		return (3 * sqrt(3) * self.side1 ** 2) / 2
    

### Testing Out Our Classes[](#testing-out-our-classes)

You can enter an interactive mode when running a Python file using a debugger. The simplest way to do this is by using the built-in [breakpoint](https://docs.python.org/3/library/functions.html#breakpoint) function.

**Note:** This function is only available in Python 3.7 or newer.

    from math import pi, sqrt
    # Folded classes
    class Shape: ...
    class Rectangle(Shape): ...
    class Square(Rectangle): ...
    class Triangle(Rectangle): …
    class Circle(Shape): …
    class Hexagon(Rectangle): …
     
    breakpoint()
    

Now, run the Python file and play around with the classes you created.

    $ python calculator.py
     
    (Pdb) rec = Rectangle(1, 2)(Pdb) print(rec)
    The area of this Rectangle is: 2
    (Pdb) sqr = Square(4)
    (Pdb) print(sqr)
    The area of this Square is: 16
    (Pdb) tri = Triangle(2, 3)
    (Pdb) print(tri)
    The area of this Triangle is: 3.0
    (Pdb) cir = Circle(4)
    (Pdb) print(cir)
    The area of this Circle is: 50.26548245743669
    (Pdb) hex = Hexagon(3)
    (Pdb) print(hex)
    The area of this Hexagon is: 23.382685902179844
    

### Challenge[](#challenge)

Create a class with a method **run** where the user can choose a shape and calculate its area.

When you’ve completed the challenge, you can send a pull request to the GitHub repo or publish your solution in the comment section.

Summary[](#summary)
-------------------

Object-oriented programming is a paradigm in which we solve problems by thinking of them as **objects**. If you understand Python OOP, you can also apply it easily in languages like [Java](/blog/best-programming-language-to-learn/#java), [PHP](/kba/what-is-php), Javascript, and [C#](/blog/best-programming-language-to-learn/#c-1).

In this article, you’ve learned about:

*   The concept of object-oriented in Python
*   Advantages of object-oriented over structured programming
*   Basics of object-oriented programming in Python
*   Concept of **classes** and how to use them in Python
*   The **constructor** of a class in Python
*   **Methods** and **attributes** in Python
*   The four pillars of OOP
*   Implementing **abstraction**, **inheritance,** and **polymorphism** in a project

Now it’s over to you!

If you liked this guide, check out our post on [Python Tutorials](/blog/python-tutorials).

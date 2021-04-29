# Python.

```
Note - In interactive mode, the last printed expression is assigned to the variable _. 
```

## Pip

- It is a package-management system written in Python.
- It is used to install and manage software packages. 
- It connects to an online repository of public and paid-for private packages, called the Python Package Index.

## Memory Mgt 

- Everything in python is treated as an object, may it be int, string, or class objects

- Objects that doesn't have any variable referening to them are called ```Dead``` objects

- Python has mechanism known as Garbage Collector, it runs as soon the reference counter of that object becomes 0

- The algo used for Garbage Collection (GC) is called Reference Counting

  ![image-20210415130209037](C:%5CUsers%5CDG086275%5CAppData%5CRoaming%5CTypora%5Ctypora-user-images%5Cimage-20210415130209037.png)

## Virtual Environment

- It is a tool that helps to keep dependencies required by different projects separate by creating isolated **python virtual environments** for them.

- ```Creating a Virtual Environment```

  ```shell
  mkdir project_name
  python -m venv project_name\venv # creating VE
  project_name\venv\Scripts\activate # activating VE
  deactivate
  rmdir venv /s # deleting VE
  
  # misc
  python -m venv project_name\venv --system-site-packages # creating VE with access to system packages
  pip install -r requirements.txt # installing packages from requirements.txt file
  ```

- Points to remember

  - Always create a virtual env for each and every project (Best Practice)
  - venv comes installed already, so no need to install anything
  - Never store any py script in venv folder
  - Never commit venv folder to the source control (scm's)
  - Can create an instruction.txt file and include data from ```pip freeze``` command into it, so that others can install same set of packages into their projects, this instruction.txt file should be committed to scm's

## Data Structures

- #### Primitive data types - int, float, string, boolean

- #### List  - mutable, fruits = ['apple', 'banana', 'orange']

- #### Tuple - non-mutable like strings, vegetables = ('potato', 'onion', 'peas')

- #### Set - unique values, doesn't keep track of order within, ranks = {'captain', 'mayor', 'deputy chief'}

- #### Dictionary - Person = {'name' : 'Hari', 'address' : {'street' : '32/11 parkers street', 'lane' : 'bosco'}}

## Lambda Functions 

- A small anonymous function

- Can have any no of args, but only one expression

- Can be a part of another function

- Example

  ```python
  nums = [1, 2, 3, 4, 5]
  even = list(filter(lambda n : n%2 == 0, nums)) # filters even no's on the basis of fn
  print(even) 
  ```

## List Comprehension

- It offers a shorter syntax when you want to create a new list based on the values of an existing list.

  ```python
  fruits = ['apple', 'banana', 'grapes', 'orange']
  fruits_with_n = [x for x in fruits if 'n' in x]
  print(fruits_with_n)
  ```

## Variable-length Arguments 

- ### *args and **kwargs

  ```python
  def func_args(*args):   # recieving variable-length argument in a tuple
      print(type(args))
      for val in args:
          print(val)
  func_args("Amit", "Ria", "Neyo")
  
  def func_kargs(**kargs):    # recieving variable-length keyworded arguments in a dictionary
      print(type(kargs))
      for i, j in kargs.items():
          print(i, j)
  func_kargs(name="Hari", age=10, contact=9808900988)
  ```

## OOPS

### Class 

- A **class** is a blueprint for creating **objects**

### Polymorphism

- Duck Typing

  - If a bird looks like a duck, behaves like a duck, consider it a **duck**

  - It is a concept related to dynamic **typing**, where the type or the class of an object is less important than the methods it defines.

  - #### Example

    ```python
    class Duck:
        def quack(self):
            print("Quack, quack!")
        def fly(self):
            print("Flap, flap!")
           
    class Person:
        def quack(self):
            print("I'm Quackin!")
        def fly(self):
            print("I'm Flapin!")
            
    def in_the_forest(thing):
        thing.quack()
        thing.fly()
        
    in_the_forest(Duck())
    in_the_forest(Person())
    ```

- Operator Overloading - assigning an operator with additional functionalities

- Method Overloading - We can't create methods of same name in the same class, that's why we don't have MO in Py

- Method Overriding - feature that allows a subclass or child class to provide a specific implementation of a **method** that is already provided by one of its superclasses or parent classes.

### Inheritance

- #### Single

- #### Multiple

- #### Multi-level

#### Method Resolution Order (MRO)

- Whenever a class(C) extends from two other classes(A and B), and there is a common function coming from both the classes in class(C), so if we call that fn from class(C), the method of that class will be called that is on the left side while inheriting, in this case class(A).

  ```python
  class C(A, B)
  ```

## Dunder or Magic methods in Python

- Dunder here means **Double Underscores**

- Few are 

  ```
   __init__, __add__, __len__, __repr__ etc.
  ```

- These are commonly used for operator overloading.

## File Handling

```python

file1 = open('about.txt', 'r') # opening file in read mode
file2 = open('hobbies.txt', 'w') # opening file in write mode
file3 = open('skills.txt', 'a') # opening file in append mode

print(file1.read())         # printing entire data from file1
print(file1.readline())     # printing single line data
print(file1.readline())     # printing next single line data

file2.write('coding\n') # writing data to file2
file2.write('chess')    # writing data to file2

file2.write(file1.read())   # writing data from file about.txt to hobbies.txt
```

## Exception Handling

Error are of three types

- #### Compile time - Developers get while developing code, syntactic errors, easy to handle

- #### Logical - Errors related to logic of developer, ex 2 + 3 is giving 4 as OP

- #### Runtime - 

  - error that occurs while the program is running, for ex
    - User provided with some illegal input
    - Connection to the server / DB  not made
    - Internet is not working

```
Note - A developer should consider all the ways a program could run into errors, accordingly handle exceptions
```

```python
a = 5
b = 2
try:
    print("Resourse opened")
    print(a/b)  # critical statements need to be enclosed in the try blocks
    n = int(input("Enter a value : "))
except ZeroDivisionError:  # try to be as specific as possible in catching errors
    print("Division by Zero is not possible")
except ValueError:
    print("Enter a valid value")
except Exception as e:  # finally catch a generic exception, if it is not catched by the other specifics
    print("Exception : ", e)
finally:    # this block will excecute regardless we get errors or not
    print("Resourse closed")
```


# C#.

- C# is a programming language
- .NET(Network Enabled Technology) is a framework for building applications on Windows
- Languages other than C# like F#, VB.NET etc can also make use of .NET for developing applications

## .NET

```c#
- In Java, when we compile our code, its not translated directly into the machine code
- Its translated into an intermediate language called bytecode, we have the same exact concept in C#
- So when we compile C# code, the result is what we call IL (Intermediate Language) Code
- IL is independent of the computer on which it is running just like bytecode
```

- CLR (Common Language Runtime)
  - It is an application sitting in memory whose job is to convert IL(Intermediate Language) Code into the machine code. This process is called JIT (Just-in-time) compilation

- Class Library

## Architecture of .NET Applications

- At a higher level, application consists of building blocks called Classes
- These Classes collaborate at the runtime and as a result produce some functionality

## Namespace

![image-20210428235945555](C:/Users/DG086275/AppData/Roaming/Typora/typora-user-images/image-20210428235945555.png)

![image-20210429000132123](C:/Users/DG086275/AppData/Roaming/Typora/typora-user-images/image-20210429000132123.png)

- As the no of Classes in an application grows, we need a way to organize these Classes

- That's where we use Namespaces

- **Namespace is a container for related Classes**

- We have Namespace to work with Data like Databases, Namspace for working with Graphics and Images, Security

- As these Namespaces grow, we need a way to partition our application, that's where we use Assembly

- **Assembly is a container for related Namespaces**

- Physically, Assembly is a file on the disk which can be either an EXE or a DLL 

- An Application contains a no of different Assemblies

  
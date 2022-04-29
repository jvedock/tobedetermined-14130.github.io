
# OnBot Java


### Part 1: The Basics


##### By Janek Vedock


## Introduction

Today we are going to be learning how to write basic OnBot java code and compile it to a robot, for this tutorial we will be using the web interface for programming but everything we do here except compiling can be used in android studio (will be covered in a future guide). This first part of the guide will cover the basic fundamentals of java necessary for comprehending the following guides, and thus it can be skipped if you have a basic knowlege of the java programming language, key concepts covered will include classes, variables, data types, methods, and visibility modifiers.


## Basics of Java

It is assumed that in reading this you have a basic understanding of the java programming language, but this section will cover a few of the major concepts that it is important to remember


### Structure of Java

Java is an object oriented programming language, meaning that everything you do will be performed on an “object” , in this case a class. One good analogy for a class is a vending machine, which can store things and also be interacted with.


### Building a Java Class

Continuing with our analogy, our base class would be a vending machine, and we would declare it as follows



```java
public class VendingMachine{

}
```


 A vending machine can store snacks and drinks inside, while a class can store variables of different types. To add data to our vending machine we would do as follows.



```java
public class VendingMachine{
	//the number of drinks in the machine
	int drinks = 20;
	//the cost of a drink (i can hope can't i)
	double cost = 1.50;
}
```


Here we see the structure of declaring a variable, first you give the data type, such as int (an integer) or double (a decimal), 

followed by the name you want to assign the variable to (here shown as drinks, and cost) 

Followed by an equals sign and the value you want to assign to the variable

Other basic data types include String (which can store a string of text) char (which can store a single character) and boolean (which can store a True or False value)

A vending machine can do more than just hold Data it can be interacted through the control panel, with this you can tell the vending machine to do different things such as get you a drink. Classes have ways to be interacted with too, in the form of methods.




```java
public class VendingMachine{
	//the number of drinks in the machine
	int drinks = 20;
	//the cost of a drink
	double cost = 1.50;
	//removes the given number of drinks from the machine
	public void ejectDrinks(drinkNum){
		drinks = drinks-drinkNum;
	}
	//returns the cost of a drink
	public double getCost(){
		return cost;
	}
}
```


Here you can see two new method I added, ejectDrinks and getCost. You can see that the structure of a method is as follows



1. The visibility modifier, in both methods here public
2. The return value, or the value to give back when the function is called, in getCost, double, if the method will not return anything use void  such as in ejectDrinks
3. The name of the function, in this case ejectDrinks, and getCost
4. A set of parentheses containing all of the function’s parameters in the form (parameter1Type, parameter1Name, parameter2Type, parameter2Name)
5. A set of braces containing the body of the function 
6. If the function is not void you will need a return statement in the body of the function, returning a value of the type specified in number 2

To run a void function you just need to call it and its parameters as follows



```java
ejectDrinks(5);
```


With that the function will run executing everything inside

It should be noted that even if the function has no parameters you will need an empty set of parentheses

To run a function with a return value you will need to assign the function to a variable of the type that it will return as follows



```java
double drinkCost = getCost();
```


That variable will then be assigned the value that the function returns


### Visibility Modifiers

Another useful feature of Java is that it contains keywords that can change how accessible an object and its variables are. The two that we are likely to use in the context of OnBot Java are public and private 


#### Public

The public modifier allows a variable or method to be used from outside of it’s object.


#### Private

If a variable or method is private, it can only be used inside of its parent class, in java it is good practice to make non-constant variables private, and use getters and setters (covered in a later part) to change and read them.





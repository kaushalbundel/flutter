# Understanding Flutter Project

## How to run the flutter app?
1. Flutter app can be run by clicking the run menu and selecting run without debugging


## Folder Structure
.idea: This is a folder that is used when Android studio is being used. Since we are using vs code we will not use this folder
android folder: This folder stores compiled android code. In the course we will very rarely use this folder
Build folder: This folder is also passive folder. This folder contains the flutter/Java code that is created when the app is coded
ios folder: Same for ios folder, not in the windows version
lib folder: This is the main folder. All dart files, which we will code during the course of making an app will be included here. 
test folder: All the test cases that are run on our app can be included here. 

gitignore: For git
metadata: flutter will use it automatically
.packages: We will not use this file
pubspec.lock:This file lists all the dependencies that are listed in pubspec.yaml file. We will be working on pubspec.yaml file and this file will be updated automatically
pubspec.yaml: This file is used to manage the dependencies of the app. By dependencies we mean third party apps

## Understanding main.dart file

- flutter is a tool where one will be creating an app by adding components. These components are also known as widgets. Futter has widgets for everything. The tool bar that is fixed is a widget, the counter adder is also an widget, the text is widget, the icon is a widget


# Understanding Dart Programming Language

- We will be using Darpad to learn dart programming language

### sample dart snippet
```void main() {
  for (int i = 0; i < 5; i++) {
    print('hello ${i + 1}');
  }
}
```
- main is the name of the function. Main is special function and as you create a dart file and run that then main function runs first. 
- Dart is a typed programming language, hence we need to define the type of the program, void is the type of function since this function returns nothing
- () This is a place where function collects arguments. arguments are the conditionals that gets passed to the function

Camelcase convention: The first letter will be small. If the name is composed of multiple letters then the next word will be capitalized eg. addNumbers. This convention is used in naming functions in dart
```
addNumbers(a, b){
 print(a+b);
}

void main() {
  addNumbers(1,3);
  print('hello world!');
  }
```
- dart uses ; at the end of each expression. Dart uses ; inside the {}. 
- dart is a stongly types language ie. we need to specify the type of the objects. If the type of object is not defined then dart automatically assume a dynamic type, which does not tell about the errors and issues with the program
- in the above code snippet, if we just write a+b in the line 44, then it will not print anything. To show a result we have to add a print statement
- print is a built in function similar to python
- the function which is defined above main, needs to be mentioned in the main function with arguments otherwise the addNumbers function will not be executed
- a function is a void function if it does not returns anything(it is very similar to python). If the function returns something then we need to specify what field it needs to return. for eg:
```
double addNumbers(double a,double b){
 return a + b;
}

void main() {
  print(addNumbers(1.5,6));
  print(addNumbers(3.9,6));
  print('hello world!');
  }
```
- in this code snippet, we have specified the outcome of addNumbers as a double, thus this return a double 
- to comment out anything use //
- Data Types in Dart
-- Text data: String data type. Characters can be specified as text by using '' or ""
-- int : Interger
-- double: floats

--------
## Dart Basics- Day 2
Variable

1. A varible in dart is determine by the keyword var, though we can also specify the type of variable like we specify for arguments in a function like int a, double b etc. So either a variable can be specified as: 
- var firstVariable
or 
- double firstVariable
- But as per the naming convention, we should specify var to declare a variable 

2. The naming convention is same as that of a function ie. camel case with first word is a small letter

Data inference
- Dart has something called data inference which means that dart can infer the type of variable by looking the result if a result of a function is stored in that variable. But however it is suggested to explicitely specify the type of the variable.

```
double addNumbers(double a,double b){
  // print(a+b);
  return a + b;
  
}

void main() {
  var addResult=addNumbers(3.5,9);
  print(addResult);
  print('hello world!');
  
  print(addResult +3.3);
  }
```

String
1. String is define as using "String" as a key word

## Dart as a object oriented language

- Dart is a object oriented language and the syntax is quite similar to python.

```

class Person{
  String name="Max";//this is to add a default value to the variable
  int age=30;
}



double addNumbers(double a,double b){
  // print(a+b);
  return a + b;
  
}

void main() {
  var p1= Person();
  print(p1.age); //printing the instance data
  // var p2=Person("Tina", 30); //we can not instantiate an instance like this 
  var p2 =Person();
  p2.age=50;
  print(p2.age);
  print(p1.name);
  print(p1.toString());
  // var addResult=addNumbers(3.5,9);
  // print(addResult);
  // print('hello world!');
  
  // print(addResult +3.3);
  }


```

The result of this is:

```
30
50
Max
Instance of 'Person'

```
- Another example of a class function (A bit more complicated by understandable function)

```
class Rectangle{
  var width;
  var height;
  
  void area(){
    var area= width * height;
    print('The Area of the rectangle is: ' + area.toString());
  }
}
void main(){
  var r1=Rectangle();
  r1.width=2;
  r1.height=3;
  print(r1.height);
  print(r1.width);
  r1.area();
  
}
```
## Class Constructors and Named Arguments 

- Constructors are functions/methods that are called only once when a class is run and an instance is created for the class. They are used to initialize a class. For eg. in the Rectangle class, whenever we want to create an instance, if we want to add width and breadth, we will create a constructor. There are two methods through which constructors can be created.
    - Method 1: 
    ```
    class Rectangle{
  var width;
  var height;
  
  Rectangle({int inputwidth=1, int inputheight=1 }){
    width=inputwidth;
    height=inputheight;
  }
  void area(){
    var area= width * height;
    print('The Area of the rectangle is: ' + area.toString());
  }
  
  void perimeter(){
    var perimeter=2*(width+height);
    print("The perimeter of Rectangle is :" + perimeter.toString());
      
  }
}
void main(){
  var r1=Rectangle(inputwidth: 2,inputheight: 3);
  print(r1.height);
  print(r1.width);
  r1.area();
  r1.perimeter();
  
}
    
    ```
    In this case the initialization can be accomplished by adding the class name itself and calling two variables representing height and width. These variables/properties are then equated with classes variables. We can also mention default responses by this.
    - Method 2:
    ```
    class Rectangle{
  var width;
  var height;
  
  Rectangle({int width=1, int height=1 }){
    this.width=width;
    this.height=height;
  }
  void area(){
    var area= width * height;
    print('The Area of the rectangle is: ' + area.toString());
  }
  
  void perimeter(){
    var perimeter=2*(width+height);
    print("The perimeter of Rectangle is :" + perimeter.toString());
      
  }
}
void main(){
  var r1=Rectangle(width: 2,height: 3);
  print(r1.height);
  print(r1.width);
  r1.area();
  r1.perimeter();
  
}
    ```
    In the second method there is no need to create another variable. Instead we can add "this." keyword to equate the two arguments.
    We can instantiate the new instance by providing values using :
    
    We can also use a variation of the above method.
    
    ```
    class Rectangle{
  var width;
  var height;
  
  Rectangle({int this.width=1, int this.height=1 });
  void area(){
    var area= width * height;
    print('The Area of the rectangle is: ' + area.toString());
  }
  
  void perimeter(){
    var perimeter=2*(width+height);
    print("The perimeter of Rectangle is :" + perimeter.toString());
      
  }
}
void main(){
  var r1=Rectangle(width: 2,height: 3);
  print(r1.height);
  print(r1.width);
  r1.area();
  r1.perimeter();
  
}
    ```
    
    > if an argument is a required argument for creating an instant. We can use @required method.
    ```
     Rectangle({@required  width=1, @required  height=1 }){
    this.width=width;
    this.height=height;
  }
    
    ```
### Named Arguments

- The arguments which can be referenced using name like we have defined in the earlier example. We can have positional arguments which are referenced using positions but defining the class becomes hard as one needs to remember the position which intializing a class.

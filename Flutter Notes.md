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
void main() {
  for (int i = 0; i < 5; i++) {
    print('hello ${i + 1}');
  }
}

- main is the name of the function. Main is special function and as you create a dart file and run that then main function runs first. 
- Dart is a typed programming language, hence we need to define the type of the program, void is the type of function since this function returns nothing
- () This is a place where function collects arguments. arguments are the conditionals that gets passed to the function

Camelcase convention: The first letter will be small. If the name is composed of multiple letters then the next word will be capitalized eg. addNumbers. This convention is used in naming functions in dart

addNumbers(a, b){
 print(a+b);
}

void main() {
  addNumbers(1,3);
  print('hello world!');
  }

- dart uses ; at the end of each expression. Dart uses ; inside the {}. 
- dart is a stongly types language ie. we need to specify the type of the objects. If the type of object is not defined then dart automatically assume a dynamic type, which does not tell about the errors and issues with the program
- in the above code snippet, if we just write a+b in the line 44, then it will not print anything. To show a result we have to add a print statement
- print is a built in function similar to python
- the function which is defined above main, needs to be mentioned in the main function with arguments otherwise the addNumbers function will not be executed
- a function is a void function if it does not returns anything(it is very similar to python). If the function returns something then we need to specify what field it needs to return. for eg:

double addNumbers(double a,double b){
 return a + b;
}

void main() {
  print(addNumbers(1.5,6));
  print(addNumbers(3.9,6));
  print('hello world!');
  }

- in this code snippet, we have specified the outcome of addNumbers as a double, thus this return a double 
- to comment out anything use //
- Data Types in Dart
-- Text data: String data type. Characters can be specified as text by using '' or ""
-- int : Interger
-- double: floats
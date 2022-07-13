# Widgets on Flutter

- The flutter app consists of widgets created in the form of a widget tree. 

- The app also has packages, from where we could do imports and extend the code mentioned in the package.

- extends keyword: inherits the properties of the class
- There can be two types of arguments
-- Named Argument and positional argument:  So far Positional arguments have been used while practicing. Named Arguments are used by calling the name of the argument instead of a position  


- An example of the code and explaination of the same:


```
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  Widget build(BuildContext context) {
    return MaterialApp(
        home: Text(
      "This app rocks!",
    ));
  }
}

```
1. In flutter as we know everything is a widget. The app is a widget and everything inside the app is a widget like the buttons, list of items, picture of some sort etc. 
2. In this code we have created a class MyApp, that takes the class StatelessWidget which comes from package that has been imported (Package name: material.dart)
3. MyApp uses inheritance to inherit some properties and methods from StateLessWidget class
4. We call a function, build which is required to build a widget. Since the type has to be specified in dart we specify Widget as the type of the method. 
> Difference between a property and a method: A property is the argument which is taken by a method/class. A method is simply a function inside a class.
5. The build method takes context as an argument/property. build() returns a so-called "widget tree" which tells Flutter what to draw onto the screen. The type of context is BuildContext.
6. This function returns a class called MaterialApp. This material app takes named arguments. Named arguments have to have the name of the argument associated with them. Like "home:" is specified. We ask the app to show text "This app rocks!" on the screen.
7. As we know to run an app we need to add a function in the main function. runApp is a function provided by the package import and it takes the class of widget that we have created as an argument. We pass MyApp class to the runApp function, to display the text on to the emulator.This function takes the widget object you pass to it and ensures that the widget tree of that widget gets created.

### Usage of @override
```
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
        home: Text(
      "This app rocks!",
    ));
  }
}

```

- In the above code, we are using override decorator to indicate that we are overrriding the origional class StatelessWidget with a custom build method. This is a good practice not entirely required. We can also work without the @override decorator.

> Alternate to using 
```void main() {
runApp(MyApp());

}
```

```
void main()=>runApp(MyApp());

```
This nomenclature works when there is a function with only one expression. 
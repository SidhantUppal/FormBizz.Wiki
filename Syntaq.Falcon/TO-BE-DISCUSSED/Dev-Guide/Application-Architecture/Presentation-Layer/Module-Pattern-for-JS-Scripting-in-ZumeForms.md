## Module Pattern for JS Scripting in ZumeForms
The module pattern is a creational type design pattern and is quite aptly described [here](https://medium.freecodecamp.org/javascript-modules-a-beginner-s-guide-783f7d7a5fcc) as:
> Good authors divide their books into chapters and sections; good programmers divide their programs into modules. 

Coded well, modular code groups related functionality, providing high cohesion for its internal elements, as well as being largely self-contained, thus providing low coupling. Other benefits include:

- Reusability
- Maintainability
- Extensibility
- Flexibility

The code below is an example JS module, built following the module pattern. This is the standard pattern we (ZumeForms) follow when creating or updating JS functionality. To understand how this pattern works, and how to implement it, we’ll break the script down.

![Capture.PNG](.attachments/Capture-691361c8-8463-4a43-a260-b613996a5650.PNG)

### Creating Privacy
JavaScript lacks the privacy mechanisms that you’re familiar with in other languages, yet there are benefits to making methods and properties private. The first step to understanding how to create modules is thus how we create privacy.
![Capture.PNG](.attachments/Capture-1f3a46aa-27ff-47ff-887c-5350fc16f04f.PNG)
The code above is a function declaration known as an Immediately Invoked Function Expression (IIFE). Any code inside the function is locally scoped, emulating privacy. Currently, the snippet above is an anonymous module, so to make it easily accessible, let's give it a namespace:
![Capture.PNG](.attachments/Capture-e824eab6-d7aa-4bf2-8b36-48e7ba31b0c4.PNG)
Our module, Module, now exists in the global scope, which will allow us to call it when needed, and access any of its public methods. Inside our module, we can now create private methods and properties, available only within the scope of the module. Declare private items as variables, and prefix the names with an underscore, like so:
![Capture.PNG](.attachments/Capture-a7d2be78-f174-4c3d-8664-6eb9f9572b16.PNG)
### Exposing Public Items
The module pattern use a return to return an object literal when called. There are different ways of formatting and returning the object literals, but our module convention is a Stacked locally scoped object literal, like so:
![Capture.PNG](.attachments/Capture-02c9cd0b-8024-46ed-a036-df96eb63075d.PNG)
The someMethod and anotherMethod object properties are publicly accessible, and we can call them in the format namespace.methodname, like so:
Module.someMethod(); and Module.anotherMethod();
To see this in action, you can create a small test module like this:
![Capture.PNG](.attachments/Capture-9771ded8-3c83-4cd5-b52c-445e86cfa78a.PNG)
When you run this script, look at the console. You will see two console entries, one from each of the public methods, and an error where we’re tried to access the private method. 
Parsing in Dependencies
There is one other aspect to the modules, which is the ability to pass in dependencies and/or other modules. This is done through the brackets of the IIFE function declaration, as highlighted below:
![Capture.PNG](.attachments/Capture-147bd7fc-8203-48cf-9cd9-e2bf761a4ac8.PNG)
In the second set of brackets is where we can pass in dependencies, such as jQuery for example:
![Capture.PNG](.attachments/Capture-fdca1da2-0084-4a7d-bdaa-109d6c1d3d9e.PNG)
Then in the first set of brackets, we set the alias for the dependency, setting how it will be accessed within the module’s scope, like so:
![Capture.PNG](.attachments/Capture-e51c7c9f-cda1-47d0-b563-0f8c9ec24886.PNG)
### Optional Reading
If you are interested in learning more about the module pattern, or related topics, check out these articles:
[Mastering The Module Pattern](https://toddmotto.com/mastering-the-module-pattern/)
[Immediately Invoked Function Expression](http://benalman.com/news/2010/11/immediately-invoked-function-expression/)

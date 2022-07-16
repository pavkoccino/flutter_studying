# Flutter study
- language: Dart. Looks kinda similar to Java.
- Material design.
- Hot reload is a nice thing.
- Almost everything is a Widget.
- installing dependency flutter pub add english_words
- Stateless widgets are immutable, all values in them are final and cannot change.
- Stateful widgets are the opposites. Abbreviation for boilerplate code is stful.
- Prefixing with the underscore ensures privacy in Dart.
- setState() triggers a call to the build() and that results in an update of UI.
- How navigation works, from documentation: "In Flutter, the Navigator manages a stack containing the app's routes. Pushing a route onto the Navigator's stack updates the display to that route. Popping a route from the Navigator's stack returns the display to the previous route."
- pubspec.yaml - configuration of dependencies and resources.
- the == operator does not compare 
memory references but rather the content of the variable.
- int? newNumber; // newNumber type allows nullability
- print(goalScorer?.length); only calls the length method if goalScorer is not null
- print(goalScorer!.length); we are confident that variable is not null
- With stateless widgets, you should set your variables as final because 
a stateless widget should not, by definition, be able to mutate its state. Using final variables 
ensures this cannot happen.
- No interfaces.
- No modifiers or access, except underscore. That means the thingy is private to the library (library is usually considered single file)
- Inheritance is possible only from one other class. But there is something called **mixins** that can "replace" this.
- Implicit getters and setters.
- No need to use word "new" when instanciating objects.
- All classes are implicitely interfaces.

## Using provider package / state management
- Class, where the data change should contain mixin ChangeNotifier.
- Inside the method, where change happens, we can call NotifyListeners().
- Top-most widget should be wrapped with ChangeNotifierProvider widget, where you pass create: (ctx) => NameOfTheClassThatHasChangeNotifiedMixin().
- Then in the widget I am interested in listening, I need to get a provider object like this final productsData = Provider.of<Products>(context). Into the <> generic type brackets you specify in which provider you are interested.

## Mixins vs Extends
- Extends = normal inheritance.
- Mixins can be created like this mixin Agility {}...it can contain properties and methods just like a class.
- Crucial difference in Dart is that you can extend from one parent, but with mixins, you can add as many mixins as you want.
- Think of mixins like lightweight inheritance, not so strong connection.


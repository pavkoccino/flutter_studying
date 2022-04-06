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

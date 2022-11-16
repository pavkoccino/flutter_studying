# Block state management
* Utilizes streams.
* Streams is the asynchronous flow of data.

### BlockProvider
* Creates and provides Bloc to all of its children. It is basically dependency injection.
* Example:
```
  BlocProvider<CounterBloc>(
    creator: (_context, _bag) => CounterBloc(),
    child: App(),
  );
```

To get access to the Bloc, you simply ask for it like this (both options viable):
```
  BlockProvider.of<CounterBloc>(context);

  OR

  context.bloc<CounterBlock>()
```

* It is created lazily, meaning that it is not created unless some widget asks for it. If you want to force create it, then set **lazy: false**.
* It automatically takes care of closing the streams.
* In case it would be needed in new route, it has to be passed with using BlockProvider.value().

### BlockBuilder
* This is the magic Widget that rebuilds the UI based on bloc state changes.

### BlockListener
* When we don't want to call the builder multiple times.

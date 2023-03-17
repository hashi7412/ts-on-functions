# ts-on-functions

`Function Type Expressions`

```
function greeter(fn: (a: string) => void) {
      fn("Hello, World");
}

function printToConsole(s: string) {
      console.log(s);
}

greeter(printToConsole);
```


`Call Signatures`

```
type DescribableFunction = {
      description: string;
      (someArg: number): boolean;
};
function doSomething(fn: DescribableFunction) {
        console.log(fn.description + " returned " + fn(6));
}
```

`Construct Signatures`

```
type SomeConstructor = {
  new (s: string): SomeObject;
};
function fn(ctor: SomeConstructor) {
  return new ctor("hello");
}
```

`Generic Functions`

```
function firstElement<Type>(arr: Type[]): Type | undefined {
  return arr[0];
}
```

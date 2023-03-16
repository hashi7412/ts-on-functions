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

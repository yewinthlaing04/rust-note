## Rust Function 03

Function declared with `fn` keyword.  
Use `snake-case` as conventional style for function and var names, in which all letters are lowercase and underscores separate words

```
fn main() {
    println!("Hello, world!");

    another_function();
}

fn another_function() {
    println!("Another function.");
}
```

### Function with parameters

```
fn main() {
    another_function(5);
}

fn another_function(x: i32) {
    println!("The value of x is: {x}");
}
```

#### With Multiple Parameters

```
fn main() {
    print_labeled_measurement(5, 'h');
}

fn print_labeled_measurement(value: i32, unit_label: char) {
    println!("The measurement is: {value}{unit_label}");
}
```

### Statements and Expressions

#### Statement
`Statements` are instructions that perform some action and `do not return` a value

Examples:  
  * `let y = 6`
  * function definition ( fn main () {} )

Cannot assign a statement to another variable:  
* ` let x = (let y=6)` => Error

#### Expression
`Expressions` evaluate to a resultant value.
Examples:  
* Math operation: 5 + 6 
* Function calls: some_function()
* Macro calls : println!("Hello")
* Scope Block 
* ``` let y = { let x = 3 ; x+1 };```
* Do not `end with a semicolon ; ` 
* Adding semicolon `;` turn the expression into statement 

### Functions with Return values 

must declare their type after an arrow `(->)`

``` 
fn five() -> i32 {
    5
}

fn main() {
    let x = five();

    println!("The value of x is: {x}");
}
```
### Rust Programming Note 01

#### Declaring `mut` and `let` variable
```
fn main() {
    let x = 5;
    println!("The value of x is: {x}");
    x = 6;
    println!("The value of x is: {x}");
}
```

#### Error Prompt

`Cannot assign twice to immutable var`

If you want to assign twice or many time use `mut` after the `let`

`let mut x = 5`

* but mutability can be very useful and can make code more convenient to write

#### Declaring Constant `const`

* not allow to use `mut` with constant
* constants aren't just immutable by default. `always immutable`
* type of value must be annotated
* valid for the entire time a program runs, within the scope in which they were declared

##### Usage
```angular2html
const THREE_HOURS_IN_SECONDS : u32 = 60 * 60 * 3 ;
```

#### Shadowing

**Shadowing** in Rust allows you to **declare a new variable with the same name** as a previous variable. The new variable "overshadows" the previous one, so any uses of that name refer to the new variable until the scope ends or it is shadowed again.

##### Key point

- shadowing is done using `let` again 

```
fn main () {
    let x = 5 ;
    let x = x + 1; // shadwos previous x , x is now 6 
    {
        let x = x * 2;
        println!("The value of x in the inner scope is: {x}");
    }

    println!("The value of x is: {x}");
}
```
- shadowing differs from `mut` :
    - `mut` allows variable reassignment but not type change
    - shadowing creates a new variable, allowing type change
    ```
    let spaces = "   "; // spaces is &str
    let spaces = spaces.len(); // now spaces is usize   
  ```
    - using `mut` with a type change will cause a compile-time error
    ```
    let mut spaces = "   " ;
    spaces = spaces.len(); // error : expected &str , found usize
  ```
##### Benefits of shadowing

- transform values without mutating
- reuse variable names
- change the type of a var in a new scope
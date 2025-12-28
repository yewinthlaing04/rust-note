## Rust Control Flow 04 

### Handling `if` expression

```
fn main(){

    let number = 3 ; 
    
    if number < 5 {
        println!("condition was true");
    }else {
        println!("condition was false");
    }
}
```

### Handling `else if` expression

```
fn main() {
    let number = 6;

    if number % 4 == 0 {
        println!("number is divisible by 4");
    } else if number % 3 == 0 {
        println!("number is divisible by 3");
    } else if number % 2 == 0 {
        println!("number is divisible by 2");
    } else {
        println!("number is not divisible by 4, 3, or 2");
    }
}
```

### Using if in a let Statement

``` 
fn main(){
    let condition = true ; 
    let number = if condition { 5 } else { 6 } ;
    
    println!("The value of number is : {number}");
}
```

### Using `loop`

``` 
fn main() {
    let mut counter = 0;

    let result = loop {
        counter += 1;

        if counter == 10 {
            break counter * 2;
        }
    };

    println!("The result is {result}");
}
```

### Disambiguating with loop labels

If you have loops within loops, `break` and `continue` apply to the innermost loop at that point. You can optionally specify a `loop label` on a loop that you can then use with `break` or `continue` to specify that those keywords apply to the labeled loop instead of the innermost loop.  
Loop lavels must begin with a single quote `like 'looping_up`

```
fn main() {
    let mut count = 0;
    'counting_up: loop {
        println!("count = {count}");
        let mut remaining = 10;

        loop {
            println!("remaining = {remaining}");
            if remaining == 9 {
                break;
            }
            if count == 2 {
                break 'counting_up;
            }
            remaining -= 1;
        }

        count += 1;
    }
    println!("End count = {count}");
}
```

### While Loops

```
fn main() {
    let mut number = 3;

    while number != 0 {
        println!("{number}!");

        number -= 1;
    }

    println!("LIFTOFF!!!");
}
```

### For Loops

```
fn main(){
    for number in (1..4).rev() { 
    println!("{number}!");
    }
    println!("LiftOff!!!");
}
```
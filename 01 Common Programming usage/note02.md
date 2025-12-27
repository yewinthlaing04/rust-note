## Rust Data Types 02 

#### Definition of Data type

A `data type` in rust tells the compiler `what kind of value a variable can hold`

Rust is `statically type language` and also data type

### Scalar Types 

- represent a single value 
- have four type of scalar type  `integers` `floating-point` `numbers` `boolean` `characters` 

#### Integers

- a number without a fractional component

| Length | Signed | UnSigned |
|--------|--------|----------|
| 8-bit  | i8     | u8       |
| 16-bit | i16    | u16      |
| 32-bit | i32    | u32      |
| 64-bit | i64    | u64      |
| 128-bit | i128   | u128     | 
| architecture-dependent | isize  | usize    | 

#### Floating Type

- just two primitive types `f32` and `f64` 

#### Boolean Type 

- just two possible values : `true` and `false`

#### Character Type 

- `char` : primitive alphabetic type 

#### Compound Type 

- can group `multiple values` into one type : `tuples` and `arrays`

##### Tuple type

The `tuple` is a general way of grouping together a number of values with a variety of types into one compound type.
`Tuple` have a fixed length: once declared, cannot grow or shrink in size


Declaring Tuples :
```
fn main(){

    let tup : (i32 , f64 , u8 )= ( 400 , 5.4 , 1 );
    let ( x , y , z ) = tup ; // like destructing in JS
    
    println! ("The value of y is : {y} "); // output will be 5.4
    
}
```

Access with ( . )
```
fn main() {
    let x: (i32, f64, u8) = (500, 6.4, 1);

    let five_hundred = x.0;

    let six_point_four = x.1;

    let one = x.2;
}
```

##### Array type

Array is a collection of multiple values.
Unlike a tuple , all elements inside arrays must be same type.

Declaring Array:
```
fn main() {
    let a = [1, 2, 3, 4, 5];
}
```

you can write array's type using square brackets with type of each element, a semicolon and then number of elements in the array

```
    let a : [i32; 5] = [1,2,3,4,5] ;
```


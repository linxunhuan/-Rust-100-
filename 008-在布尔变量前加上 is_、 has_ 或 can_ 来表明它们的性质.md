+ 使用 is_、has_ 或 can_ 作为布尔变量的前缀，可以明确其用途并提高代码的可读性
+ 使用 is_、has_ 或 can_ 等前缀可以立即了解布尔变量的用途
  + 使代码更直观、更易于理解
  + 这种做法有助于其他开发人员快速掌握代码背后的逻辑和意图
+ 规范写法
```rust
fn is_even(number: i32) -> bool {
    number % 2 == 0
}
fn has_permission(user_role: &str) -> bool {
    user_role == "admin"
}
fn can_drive(age: u32) -> bool {
    age >= 18
}
let number = 4;
let user_role = "admin";
let age = 20;
println!("Is the number even? {}", is_even(number));
println!("Does the user have permission? {}",
has_permission(user_role));
println!("Can the person drive? {}", can_drive(age));
```
+ 错误示例
```rust
fn even(number: i32) -> bool {
    number % 2 == 0
}
fn permission(user_role: &str) -> bool {
    user_role == "admin"
}
fn drive(age: u32) -> bool {
    age >= 18
}
let number = 4;
let user_role = "admin";
let age = 20;
println!("Is the number even? {}", even(number));
println!("Does the user have permission? {}",
permission(user_role));
println!("Can the person drive? {}", drive(age));
```
+ 对布尔变量使用描述性前缀是许多编程语言中的常见做法，不仅仅是 Rust
+ 这种惯例有助于提高不同代码库和团队之间的代码清晰度和可维护性
+ 在 Rust 中使用 Option 和 Result 类型可确保安全且明确的错误处理
+ Rust 的 Option 和 Result 类型提供了一种明确处理潜在错误和缺失值的方法，从而提高了代码的安全性和可读性
+ 规范写法
```rust
fn divide(a: f64, b: f64) -> Result<f64, &'static str> {
    if b == 0.0 {
        Err("Cannot divide by zero")
    } else {
        Ok(a / b)
    }
}
fn main() {
    match divide(4.0, 2.0) {
        Ok(result) => println!("Result: {}", result),
        Err(e) => println!("Error: {}", e),
    }
    match divide(4.0, 0.0) {
        Ok(result) => println!("Result: {}", result),
        Err(e) => println!("Error: {}", e),
    }
}
```
+ 错误示范
```rust
fn divide(a: f64, b: f64) -> f64 {
    if b == 0.0 {
        panic!("Cannot divide by zero");
    } else {
        a / b
    }
}
fn main() {
    println!("Result: {}", divide(4.0, 2.0));
    println!("Result: {}", divide(4.0, 0.0)); // This will cause a
panic
}
```

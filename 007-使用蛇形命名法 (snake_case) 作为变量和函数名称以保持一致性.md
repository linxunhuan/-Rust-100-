+ 使用蛇形命名法命名变量和函数名称可确保 Rust 代码的一致性和可读性
+ 采用蛇形命名法等一致的命名约定有助于保持 Rust 代码库的可读性和统一性
+ 这种做法符合 Rust 社区标准
+ 示例代码
```rust
fn calculate_area(width: f64, height: f64) -> f64 {
    width * height
}
let rectangle_width = 10.0;
let rectangle_height = 5.0;
let area = calculate_area(rectangle_width,
rectangle_height);
println!("The area of the rectangle is: {}", area);
```
+ 错误示例
```rust
fn calculateArea(width: f64, height: f64) -> f64 {
    width * height
}
let rectangleWidth = 10.0;
let rectangleHeight = 5.0;
let area = calculateArea(rectangleWidth, rectangleHeight);
println!("The area of the rectangle is: {}", area);
```
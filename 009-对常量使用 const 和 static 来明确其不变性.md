+ 在 Rust 中使用 const 和 static 可确保常量是不可变的且定义明确
+ 在 Rust 中，对常量使用 const 和 static 有助于使代码更具可读性和可维护性
+ 它清楚地表明这些值是不可变的，不应更改
+ 示例代码
```rust
// 使用“const”作为编译时常量
const MAX_USERS: u32 = 1000;
// 使用“static”作为全局常量
static APP_NAME: &str = "MyApp";
fn main() {
    println!("Max users: {}", MAX_USERS);
    println!("App name: {}", APP_NAME);
}

```
+ 错误示例
```rust
let max_users: u32 = 1000;
let app_name: &str = "MyApp";
fn main() {
    println!("Max users: {}", max_users);
    println!("App name: {}", app_name);
}
```
+ 在 Rust 中，const 用于编译时常量
+ 而 static 用于在内存中具有固定地址的全局常量
+ 两者都确保不变性，但 static 也可以通过 static mut关键字用于可变全局变量
  + 尽管通常不建议这样做
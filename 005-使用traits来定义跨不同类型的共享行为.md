 + Rust 中的traits允许您定义跨不同类型的共享行为，从而提高代码的可重用性和可读性
+ 规范写法
```rust
// 定义具有共同行为的traits
trait Describable {
    fn describe(&self) -> String;
}

struct Dog {
    name: String,
    age: u8,
}
impl Describable for Dog {
    fn describe(&self) -> String {
        format!("Dog named {} is {} years old.", self.name, self.age)
    }
}

struct Car {
    model: String,
    year: u16,
}

impl Describable for Car {
    fn describe(&self) -> String {
        format!("Car model {} from year {}.", self.model, self.year)
    }
}

fn main() {
    let my_dog = Dog { name: String::from("Buddy"), age: 3 };
    let my_car = Car { model: String::from("Tesla"), year:2020 };
    println!("{}", my_dog.describe());
    println!("{}", my_car.describe());
}
```
+ 错误示例
```rust
struct Dog {
    name: String,
    age: u8,
}
impl Dog {
    fn describe(&self) -> String {
        format!("Dog named {} is {} years old.", self.name, self.age)
    }
}
struct Car {
    model: String,
    year: u16,
}
impl Car {
     fn describe(&self) -> String {
        format!("Car model {} from year {}.", self.model, self.year)
    }
}
fn main() {
    let my_dog = Dog { name: String::from("Buddy"), age: 3};
    let my_car = Car { model: String::from("Tesla"), year: 2020};

    println!("{}", my_dog.describe());
    println!("{}", my_car.describe());
}
```
+ Rust 中的特征类似于 Java 和 C# 等其他编程语言中的接口
+ 它们允许您定义类型必须实现的一组方法，从而促进多态性和代码重用



















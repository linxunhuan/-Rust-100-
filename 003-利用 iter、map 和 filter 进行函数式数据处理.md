+ 使用 Rust 的迭代器、映射和过滤器编写干净、易读、高效的数据处理代码
  + 在 Rust 中使用迭代器、映射和过滤器可以实现函数式编程风格
  + 从而使代码更简洁、更具表现力
+ 规范写法
```rust
let numbers = vec![1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let result: Vec<i32> = numbers.iter()
    .filter(|&&x| x % 2 == 0) 
    .map(|&x| x * x) 
    .collect(); 
println!("{:?}", result); // Output: [4, 16, 36, 64, 100]
```
+ 错误示例
```rust
let numbers = vec![1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let mut result = Vec::new();
for i in &numbers {
    if i % 2 == 0 { 
        result.push(i * i); 
    }
}

println!("{:?}", result); // Output: [4, 16, 36, 64, 100]
```
+ 这就是函数式编程的风格
  + 从c++、Java过来的话，需要适应一下
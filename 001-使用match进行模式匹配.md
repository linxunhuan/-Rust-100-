+ 使用 match 进行模式匹配提供了一种清晰简洁的方法来处理 Rust 中的不同情况
  + 在 Rust 中使用 match 可以让你明确处理各种情况
  + 使代码更具可读性和可维护性
+ Rust 中的模式匹配是详尽的，这意味着:
  + 编译器确保处理所有可能的情况
    + 没有就报错
+ 规范的代码：
```rust
enum Direction {
    North,
    South,
    East,
    West,
}
fn get_direction_name(direction: Direction) -> &'static str {
    match direction {
        Direction::North => "North",
        Direction::South => "South",
        Direction::East => "East",
        Direction::West => "West",
    }
}
fn main() {
    let direction = Direction::North;
    println!("Direction: {}", get_direction_name(direction));
}
```
+ 不规范的代码
```rust
enum Direction {
    North,
    South,
    East,
    West,
}
fn get_direction_name(direction: Direction) -> &'static str {
    if let Direction::North = direction {
        "North"
    } else if let Direction::South = direction {
        "South"
    } else if let Direction::East = direction {
        "East"
    } else if let Direction::West = direction {
        "West"
    } else {
        "Unknown"
    }
}
fn main() {
    let direction = Direction::North;
    println!("Direction: {}", get_direction_name(direction));
}
```
































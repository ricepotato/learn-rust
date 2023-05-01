# rust programming

https://indosaram.github.io/rust-python-book/ch1-00.html

## 프로젝트 생성

```
cargo new rust_part
```

## 프로젝트 build

target/debug 에 산출물 생성됨

기본적으로 `debug` 모드로 build 됨

`debug` 모드는 build 는 빠르지만 프로그램은 느리게 실행될 수 있음

```
cargo build
```

`--release` 옵션을 사용하면 `release mode` 로 build 됨

```
cargo build --release
```


빌드와 실행을 동시에 수행

```
cargo run
```


## rustfmt

`alt + shift + F` 입력시 코드 포맷 수행

아래 명령어로 실행 가능

```
cargo fmt
```



## examples

변수 선언, 출력

```rust
fn main() {
    let x: i32 = 10;
    let y = 10;

    println!("x = {}, y = {}", x, y);
}
```

기본적으로 let 으로 선언하면 불변임 아래 코드는 컴파일되지 않음

```rust
fn main() {
    let x = 1;
    x = 2;

    println!("{}", x);
}
```

변경가능한 변수를 선언하기 위해서 `mut` 키워드 사용 아래코드처럼 변경



```rust
fn main() {
    let mut x = 1;
    x = 2;

    println!("{}", x);
}
```
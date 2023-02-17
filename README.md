my-httpie

A naive sample httpie implementation with Rust 

Example

cargo build --quiet && target/debug/httpie post https://www.baidu.com/ a=1 b=2
cargo build --quiet && target/debug/httpie get http://jsonplaceholder.typicode.com/posts
cargo build --quiet && target/debug/httpie post https://www.cnuseful.com/api/index/weather/ code=57494
cargo build --quiet && target/debug/httpie get https://www.cnuseful.com/api/index/weather?code=57494

cargo build --quiet && target/debug/httpie post https://httpbin.org/post a=1 b=2



# my-httpie

A naive simple httpie implementation with Rust

# Usage
➜ cargo build --quiet && target/debug/httpie 
```
httpie 1.0
A naive httpie implementation with Rust, can you imagine how easy it is?

USAGE:
    httpie <SUBCOMMAND>

FLAGS:
    -h, --help       Prints help information
    -V, --version    Prints version information

SUBCOMMANDS:
    get     feed get with an url and we will retrieve the response for you
    help    Prints this message or the help of the given subcommand(s)
    post    feed post with an url and optional key=value pairs. We will post the data as JSON,
            and retrieve the response for you

```
# Example
➜ cargo build --quiet && target/debug/httpie post https://httpbin.org/post a=1 b=2
```
HTTP/1.1 200 OK

date: "Fri, 24 Mar 2023 09:05:38 GMT"
content-type: "application/json"
content-length: "474"
connection: "keep-alive"
server: "gunicorn/19.9.0"
access-control-allow-origin: "*"
access-control-allow-credentials: "true"

{
  "args": {},
  "data": "{\"b\":\"2\",\"a\":\"1\"}",
  "files": {},
  "form": {},
  "headers": {
    "Accept": "*/*",
    "Content-Length": "17",
    "Content-Type": "application/json",
    "Host": "httpbin.org",
    "User-Agent": "Rust Httpie",
    "X-Amzn-Trace-Id": "Root=1-641d67e2-35bb1aeb187055a63ebc28b5",
    "X-Powered-By": "Rust"
  },
  "json": {
    "a": "1",
    "b": "2"
  },
  "origin": "221.218.136.246",
  "url": "https://httpbin.org/post"
}
```





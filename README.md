# Hello (Adv. Programming - Module 6)

## Contents

1. [Commit 1 Reflection](##commit-1-reflection)

## Commit 1 Reflection

For this commit, I built a basic HTTP server in Rust. I started by creating a new Rust project with `cargo new hello` and setting up GitHub version control.

The server uses Rust's standard library components:

- **TcpListener**: Binds to 127.0.0.1:7878 to listen for connections
- **TcpStream**: Handles client connections
- **BufReader**: Provides efficient I/O

The server implementation consists of:

- A main function that creates the listener and processes incoming connections in a loop
- A `handle_connection` function that reads HTTP requests from each connection and currently just prints the request data

This simple server demonstrates Rust's networking capabilities and safety features. Future work will include proper HTTP response handling and content serving.

##

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

## Commit 2 Reflection

![Screenshot](./images/1.png)

In this commit, I enhanced the server to serve actual HTML content rather than just logging requests. This represents a significant step toward creating a functional web server.

1. **File System Integration**: Added the `fs` module to read HTML content from the file system.

2. **HTTP Response Generation**: Implemented proper HTTP response construction with:

   - Status line (`HTTP/1.1 200 OK`)
   - Content-Length header
   - The actual HTML content

3. **Content Serving**: Created a simple HTML file (`hello.html`) to serve to clients, featuring a greeting message.

4. **Complete Request-Response Cycle**: The server now completes the full HTTP cycle by not only reading requests but responding with meaningful content.

This implementation demonstrates how Rust's standard library provides the tools needed for complete web server functionality without external dependencies.

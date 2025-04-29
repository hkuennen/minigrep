# Minigrep

## Philosophy

The _minigrep_ project was inspired by the need for a simple, lightweight tool to search for text patterns in files. While full-featured tools like `grep` exist, building a minimal version from scratch is an excellent way to learn about the core concepts of file I/O, command-line arguments, and pattern matching in Rust.

This project, featured in the Official Rust Programming Book, emphasizes practical problem-solving and encourages developers to deepen their understanding of Rust’s robust standard library and ownership model.

## Description

_Minigrep_ is a command-line application that searches for a specific string within a file and prints out matching lines. It is a simplified version of the Unix `grep` tool, implemented in Rust, and serves as a hands-on learning project for Rust beginners.

### Key Features:

- **Search functionality**: Users can specify the string they want to search for, along with the file to search in.
- **Case-insensitive search**: Supports case-insensitive searching through an optional environment variable.
- **Error handling**: Demonstrates robust error handling for invalid input or missing files.

### How it Works:

1. **Command-line arguments**: The program accepts two arguments:

   - The string to search for.
   - The file to search in.

   Example:

   ```bash
      cargo run -- "you" poem.txt
   ```

2. **Environment variable for case sensitivity**:
   By setting the CASE_INSENSITIVE environment variable, users can enable case-insensitive searches.

   Example:

   ```bash
      CASE_INSENSITIVE=1 cargo run -- "The" poem.txt
   ```

3. **Output**: The program prints matching lines to the terminal, making it easy to identify relevant content in the file.

This project showcases how to parse command-line arguments, read files, and handle errors in a clean and idiomatic way in Rust.

### Customization Options:

- Add support for regular expressions.
- Improve performance with multithreading for larger files.
- Expand functionality to handle multiple files simultaneously.

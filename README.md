# Custom Parser in Rust (Part 2)

[![A Custom Parser](./src/comp1.png)](https://youtu.be/yKzcWMr7YX8)


This project is the **second milestone** in my journey toward compiler construction. After building a custom lexer and tokenizer, I’ve now implemented a **Pratt Parser** in Rust. The parser takes the stream of tokens and constructs an **Abstract Syntax Tree (AST)** — the structured backbone of any programming language.

By implementing this from scratch in Rust, I’ve deepened my understanding of **operator precedence, associativity, and expression parsing** — key concepts in compiler front-end design.

---

## ✨ Highlights

* Supports **prefix, postfix, and infix operators**
* Correctly handles **precedence** (e.g., `*` binds stronger than `+`) and **associativity rules** 
* Implements **ternary (`?:`)**, **unary (`-`, `+`)**, **postfix (`!`, indexing `[]`)**, and **chaining (`.`)**
* Outputs a clean **AST in Lisp-style format** for readability
* Modular design that integrates seamlessly with the lexer

---

## 🌱 Future Plans

This parser is just one step forward. Next, I’ll be working on:

* Type checking and semantic analysis
* Error handling and diagnostics for malformed code
* Code generation for a toy language
* Extending this into a **complete compiler in Rust**

---

## 🛠️ Built With

* **Rust**
* **Pratt Parsing** technique
* Core **compiler front-end design principles**

---

## 📂 Repository Structure

```
├── src
│   ├── ast
│   │   ├── lexer.rs     # Lexer implementation
│   │   ├── parser.rs    # Pratt parser implementation
│   │   └── mod.rs       # Module exports
│   ├── main.rs          # Entry point
│   └── span.rs          # Span tracking (positions)
├── Cargo.toml           # Rust project configuration
└── README.md            # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites

* Install [Rust](https://www.rust-lang.org/)

### Build & Run

```bash
git clone https://github.com/artyviz/Custom-parser-in-Rust
cd rust-parser
cargo run
```

---

## 📖 Examples

**Input:**

```
1 + 2 * 3
```

**AST Output:**

```
(+ 1 (* 2 3))
```

**Input:**

```
a ? b : c ? d : e
```

**AST Output:**

```
(? a b (? c d e))
```

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to open an issue or submit a pull request.

---

## 📜 License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

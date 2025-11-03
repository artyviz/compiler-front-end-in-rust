# 🦀 Compiler Front-End in Rust

[![A Custom Parser](./src/comp1.png)](https://youtu.be/yKzcWMr7YX8)

*(Lexer + Parser Integration Project)*

This repository combines my **custom lexer** and **Pratt parser**, marking a significant milestone in my compiler development journey.
Built entirely in **Rust**, it covers the **front-end phase of a compiler** — transforming raw source code into a structured **Abstract Syntax Tree (AST)**.

---

## 🧩 Overview

### 🔹 Lexer

The lexer (or tokenizer) scans raw text and produces a stream of tokens — the fundamental symbols of the language.
It handles:

* Keywords, identifiers, literals, operators, and delimiters
* Efficient span tracking (line & column info)
* Error detection for invalid tokens

### 🔹 Parser

The parser consumes tokens from the lexer and constructs an **AST** using the **Pratt Parsing** technique.
It supports:

* Prefix, postfix, and infix expressions
* Correct precedence and associativity
* Ternary (`?:`), unary (`-`, `+`), postfix (`!`, `[]`), and chaining (`.`)
* AST output in Lisp-style format

---

## 🛠️ Tech Stack

* **Language:** Rust 🦀
* **Core Concepts:** Lexical Analysis, Pratt Parsing, Abstract Syntax Tree
* **Paradigm:** Modular compiler front-end architecture

---

## 🗂️ Repository Structure

```
compiler-front-end-in-rust/
├── lexer/
│   ├── src/
│   │   ├── lexer.rs          # Tokenizer implementation
│   │   └── span.rs           # Source position tracking
│   └── Cargo.toml
├── parser/
│   ├── src/
│   │   ├── parser.rs         # Pratt parser logic
│   │   └── ast.rs            # Abstract Syntax Tree structures
│   └── Cargo.toml
├── integration/
│   └── main.rs               # Combines lexer + parser
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

* [Install Rust](https://www.rust-lang.org/)

### Run Locally

```bash
git clone https://github.com/artyviz/compiler-front-end-in-rust.git
cd compiler-front-end-in-rust
cargo run
```

---

## 📖 Example

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

## 🌱 Future Scope

* Type checking & semantic analysis
* Error diagnostics and recovery
* Intermediate representation & code generation
* Full **compiler pipeline** for a toy language

---

## 🛡️ License

This project is licensed under the **MIT License**. See [LICENSE](LICENSE) for details.

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---
sidebar_position: 1
---

# Tutorial Intro

Let's discover **One1fy in less than 5 minutes**.

## Getting Started

Get started by **cloning the repo**.

### What you'll need

- [Visual Studio](https://nodejs.org/en/download/)
  - When installing Visual Studio, choose Community edition and make sure to include C++ build tools
- [LLVM](https://nodejs.org/en/download/)
  - Install LLVM to aid in C++ compilation
- [Cargo](https://nodejs.org/en/download/)
  - Install Cargo to be able to compile Rust code

In the future, One1fy will be accessible to install as a Cargo package and relevant language packages

## Create a new app

Create a new One1fy site using the **package template**.

```bash
cargo clean
cargo build --features windows
```

Checkout out the ```Cargo.toml``` file to check out all the packages used, and change the features keywords based on project name and platform

## Start your app

Run the development server, utilize the build you just created:

```bash
cargo run --features windows
```

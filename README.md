# Basic Rocket Web Server

This application was made part of an introductory video for Rust. The video included an overview of some Rust syntax, along with the implementation of this simple To Do REST API.

The video can be seen on [YouTube](https://youtu.be/8RA6LSjXvRk)

## Installing Rust

The easiest way to install Rust is by using `rustup`, a Rust version manager.
Follow the instructions on the [rustup](https://rustup.rs/) site for your operating system.

By default, `rustup` will install the latest stable verison of Rust. Rocket currently requires a nightly version of Rust. Recent nightly versions have a compatibility issue with the version of Rocket used in this project, so it is necessary to pin to a known good nightly version like `nightly-2021-04-13`.

When you're in the directory containing this repository's code, `rustup` will look in the `rust-toolchain` file and automatically install and use the correct Rust version for you. Test this out with:

```sh
$ rustc --version
```

If that does not work for any reason, you can set the directory to use nightly by running the follow:

```sh
$ rustup override set nightly-2021-04-13
```

## Useful toolchain extentions

Recommended extension to install that watching and auto-reloading of the application through the use of `cargo watch -x run`. [more details](https://crates.io/crates/cargo-watch)

```sh
$ cargo install cargo-watch
```

Recommended extension to install that provides `cargo add`, `cargo rm`, and `cargo upgrade` for adding and removing packages against https://crates.io/ [more details](https://crates.io/crates/cargo-edit)

```sh
$ cargo install cargo-edit
```

Optional extension to install that provides `cargo expand` which outputs pre-processed code such as what macros generate. [more details](https://crates.io/crates/cargo-expand)

```sh
$ cargo install cargo-expand
```

## Useful VSCode extention

Recommended VSCode extension to give extremely useful tooltips and highlighting is [rust-analyzer](https://github.com/rust-analyzer/rust-analyzer.git)

## Compiling and Starting the Server

Built using Cargo, Rust's package manager and build tool.

To compile for development, run:

```sh
$ cargo build
```

which will create a binary in `target/debug` that you can run with:

```sh
$ ./target/debug/basic-rocket-web-server
```

You can compile and run with one command by using:

```sh
$ cargo run
```

If you installed `cargo-watch`, you can have cargo automatically rebuild and run the application on file changes within the project with the following command. Note that the `.gitignore` file will be respected and your application will not be rebuilt for changes to any file or folder listed there.

```sh
$ cargo watch -x run
```

When compiling for performance testing, build in release mode by using:

```sh
$ cargo build --release
```

which will create the corresponding binary in `target/release`:

```sh
$ ./target/release/basic-rocket-web-server
```

Similarly, you can do this in one step with:

```sh
$ cargo run --release
```

The server will, by default, start an HTTP API server on port `8000` and will only be accessible as `localhost` unless running in release mode.

## Further Reading

### Rust Language

- [Official Rust Language Book](https://doc.rust-lang.org/book/)
- [Repository of Useful Books](https://github.com/sger/RustBooks)

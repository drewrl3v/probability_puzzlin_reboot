# probability_puzzlin

# using mdbook

This is an interactive book built using [mdBook](https://rust-lang.github.io/mdBook/) with support for LaTeX-style equations via [`mdbook-katex`](https://github.com/lzanini/mdbook-katex).

## Install Prerequisites

    You need to have **Rust** installed. It comes with `cargo`, which is used to install `mdBook` and plugins.

MacOS and Linux Users:

    curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
    rustup update

Windows Users:

    Download and run the installer: https://rustup.rs

## Install mdbook
Once you have cargo installed on your computer, you can install the following packages for building the markdown book.

    cargo install mdbook
    cargo install mdbook-katex
    cargo install mdbook-toc

## Running mdbook
In this repo go to the book directory and start the server

    cd book
    mdbook serve

# RMP - Rust MessagePack

RMP is a complete pure-Rust [MessagePack](http://msgpack.org) implementation. MessagePack a compact self-describing binary serialization format.

This project consists of three crates:

* [RMP-Serde][crates-rmps-url] ([Documentation][rmps-docs-url]) — easy serializing/deserializing via [Serde](https://serde.rs).
* [RMP-Value][crates-rmpv-url] ([Documentation][rmpv-docs-url]) — a universal `Value` enum that can hold any MessagePack type. Allows deserializing arbitrary messages without a known schema.
* [RMP][crates-rmp-url] ([Documentation][rmp-docs-url]) — low-level functions for reading/writing encoded data.

## Features

- **Convenient and powerful APIs**

  RMP is designed to be lightweight and straightforward. There is a high-level API with support for Serde,
  which provides you convenient interface for encode/decode Rust's data structures using `derive` attribute.
  There are also low-level APIs, which give you full control over data encoding/decoding process,
  with no-std support and without heap allocations.

- **Zero-copy value decoding**

  RMP allows to decode bytes from a buffer in a zero-copy manner. Parsing is implemented in safe Rust.

- **Robust, stable and tested**

  This project is developed using TDD and CI, so any found bugs will be fixed without breaking
  existing functionality.

## Why MessagePack?

Smaller and simpler to parse than JSON. Supports the same types as JSON, plus binary data, all float values, and 64-bit numbers.
Encoded data is self-describing and extensible, without requiring a schema definition.

## Requirements

- Rust 1.56.0 or later

[rustc-serialize]: https://github.com/rust-lang-nursery/rustc-serialize
[serde]: https://github.com/serde-rs/serde

[ci-img]: https://github.com/3Hren/msgpack-rust/actions/workflows/ci.yml/badge.svg
[ci-url]: https://github.com/3Hren/msgpack-rust/actions/workflows/ci.yml

[coveralls-img]: https://coveralls.io/repos/3Hren/msgpack-rust/badge.svg?branch=master&service=github
[coveralls-url]: https://coveralls.io/github/3Hren/msgpack-rust?branch=master

[rmp-docs-url]: https://docs.rs/rmp
[rmps-docs-url]: https://docs.rs/rmp-serde
[rmpv-docs-url]: https://docs.rs/rmpv

[crates-rmp-url]: https://lib.rs/crates/rmp
[crates-rmps-url]: https://lib.rs/crates/rmp-serde
[crates-rmpv-url]: https://lib.rs/crates/rmpv


[![Build][ci-img]][ci-url] [![Coverage Status][coveralls-img]][coveralls-url]

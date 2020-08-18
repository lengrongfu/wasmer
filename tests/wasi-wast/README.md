# WASI test suite

WASI test files with expected output in a custom WAST format.

## Setup

In order to run the test generator properly you will need:

- `rustup` installed and on your PATH
- `wasm-opt` and `wasm-strip` from `wabt` installed and on your PATH

## Usage

```
Optional arguments:
  -a, --all-versions      Whether or not to do operations for all versions of WASI or just the latest.
  -g, --generate-wasm     Whether or not the Wasm will be generated.
  -s, --set-up-toolchain  Whether or not the logic to install the needed Rust compilers is run.
  -h, --help              Print the help message
```

And here's an example of how to generate these tests:

```bash
cargo run -- -as # set up the toolchains for all targets
cargo run -- -ag # generate the WASI tests for all targets
```
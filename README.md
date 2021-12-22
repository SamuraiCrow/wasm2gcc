# w2c2

Translates WebAssembly modules to C.
Inspired by [wabt's wasm2c](https://github.com/WebAssembly/wabt/tree/main/wasm2c).

## Features

- Implements the WebAssembly Core Specification 1.0
- Passes 99.9% of the WebAssembly core semantics test suite
- Written in C89 and generates C89
- Support for older operating systems and architectures
- Support for big-endian systems
- Streaming compilation, low memory usage

## Performance

- Coremark 1.0: ~7% slower than native

## Usage

```sh
make release
./w2c2 <module.wasm> > <module.c>
```

## Examples

Coremark:

```sh
cd examples/coremark
./coremark
```

## Testing

Requires Python 3 and wabt (for wast2json).

```sh
cd tests
make gen
make run-tests
```
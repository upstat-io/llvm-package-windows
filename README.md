# LLVM Package for Windows

Pre-built LLVM binaries for Windows with **all targets enabled** (X86, ARM, AArch64, WebAssembly, etc.).

Built for the [Ori compiler](https://github.com/upstat-io/ori-lang).

## Download

See [Releases](https://github.com/upstat-io/llvm-package-windows/releases) for pre-built packages.

## Why?

Standard LLVM Windows packages (like [vovkos](https://github.com/aspect-build/llvm-project/releases)) only include the X86 target. The Ori compiler uses [inkwell](https://github.com/TheDan64/inkwell) which links against all LLVM targets, causing link errors.

This package builds LLVM with all targets enabled.

## Building

To build your own, see [`scripts/build-llvm-windows/`](https://github.com/upstat-io/ori-lang/tree/master/scripts/build-llvm-windows) in the Ori repo.

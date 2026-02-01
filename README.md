# LLVM Package for Windows

Pre-built LLVM binaries for Windows with **all targets enabled** (X86, ARM, AArch64, WebAssembly, etc.).

Built for the [Ori compiler](https://github.com/upstat-io/ori-lang).

## Download

See [Releases](https://github.com/upstat-io/llvm-package-windows/releases) for pre-built packages.

## Why?

Standard LLVM Windows packages (like [vovkos](https://github.com/aspect-build/llvm-project/releases)) only include the X86 target. The Ori compiler uses [inkwell](https://github.com/TheDan64/inkwell) which links against all LLVM targets, causing link errors.

This package builds LLVM with all targets enabled.

## Building Your Own

### Prerequisites

- Windows 10/11
- [Visual Studio 2022](https://visualstudio.microsoft.com/downloads/) with "Desktop development with C++" workload

### Build

Open PowerShell and run:

```powershell
powershell -ExecutionPolicy Bypass -File build.ps1
```

The script will:
1. Install Scoop, CMake, Ninja, 7zip (if needed)
2. Clone LLVM 17.0.6
3. Build with all targets (~1-2 hours)
4. Package as `LLVM-17.0.6-win64.7z`

### Upload a New Release

```powershell
gh release create v17.0.6 LLVM-17.0.6-win64.7z --title "LLVM 17.0.6 for Windows"
```

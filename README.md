# bpf2c: convert eBPF bytecode to C code

This is a fork version of <https://github.com/microsoft/ebpf-for-windows/tree/main/tools/bpf2c>, which can be easily build on Linux.

**Not finished yet, may not be build correctly**

## Overview

`bpf2c` is a specialized tool designed to streamline the process of converting eBPF byte code into C code. This tool is an essential part of the `eBPF-for_windows` workflow when working with eBPF programs, particularly in scenarios where the goal is to ensure that the eBPF byte code is sandboxed, verified, and safely integrated into larger applications.

## Key Features

- **ELF File Parsing:** `bpf2c` takes an ELF file as input, automatically extracting the list of maps and stored eBPF programs.
- **Instruction-Level Translation:** Each eBPF instruction is translated into its equivalent C statement, enabling deeper integration with C-based systems.
- **Skeleton Code Generation:** `bpf2c` emits skeleton C code that includes the necessary hooks for relocation operations during runtime. This skeleton code is essential for ensuring that the eBPF program can be properly loaded and executed within the target environment.

## Build

The tool require C++20 to build.

Install the tools

```sh
sudo apt-get install libc++-dev libc++abi-dev clang
```

build the tool:

```sh
make
```

## Reference

- <https://github.com/microsoft/ebpf-for-windows/tree/main/tools/bpf2c>
- <https://opensource.microsoft.com/blog/2022/10/25/towards-debuggability-and-secure-deployments-of-ebpf-programs-on-windows/>

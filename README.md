# mit-6.035-sp21

MIT 6.035 Computer Language Engineering — Spring 2021

Course link: https://github.com/6035/sp21

## Overview

This repository contains a TypeScript implementation of a compiler built as part of MIT 6.035 (Computer Language Engineering), Spring 2021. The course covers the design and implementation of compilers for higher-level programming languages, including scanning, parsing, semantic analysis, intermediate representation, code generation, and optimization.

The compiler targets the **Decaf** language and generates **x86-64** assembly.

## Course Description

Analyzes issues associated with the implementation of higher-level programming languages. Covers fundamental concepts, functions, and structures of compilers, the interaction of theory and practice, and the use of tools in building software. Includes a multi-person project on compiler design and implementation.

- **Prerequisites:** 6.004, 6.031
- **Level:** Undergraduate
- **Units:** 4-4-4

## Repository Structure

```
mit-6.035-sp21/
├── src/                  # TypeScript compiler source code
│   ├── main.ts           # Compiler entry point
│   ├── scanner/          # Lexical analysis (scanner/tokenizer)
│   ├── parser/           # Syntax analysis (parser)
│   ├── ir/               # Intermediate representation
│   ├── asm/              # x86-64 assembly generation
│   ├── interpreter/      # Interpreter for testing
│   ├── core/             # Core utility functions
│   └── types/            # Type definitions
├── sp21/                 # Course materials for Spring 2021
│   ├── phase-1/          # Scanner/parser project spec
│   ├── phase-2/          # Semantic analysis project spec
│   ├── phase-3/          # Code generation project spec
│   ├── phase-4/          # Dataflow analysis project spec
│   ├── phase-5/          # Optimization project spec
│   └── materials/        # Lecture slides, handouts, and problem sets
├── notes/                # Personal study notes and assembly references
├── references/           # Reference materials
└── fa18/                 # Additional materials from Fall 2018 offering
```

## Compiler Project Phases

The compiler is built incrementally across five phases:

| Phase | Description |
|-------|-------------|
| Phase 1 | Scanner and parser (individual project) |
| Phase 2 | Semantic analysis |
| Phase 3 | Unoptimized x86-64 code generation |
| Phase 4 | Dataflow analysis and optimization |
| Phase 5 | Advanced optimizations (register allocation, loop opts, etc.) |

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v14+)
- [Yarn](https://yarnpkg.com/)

### Installation

```bash
yarn install
```

### Build

```bash
yarn compile
```

### Run

```bash
yarn debug src/main.ts -- <options>
```

### Test

```bash
yarn test
```

### Lint

```bash
yarn lint
```

## Topics Covered

- **Lexical Analysis:** Regular expressions, finite automata, scanning
- **Parsing:** Top-down (LL) and bottom-up (shift-reduce/LR) parsing
- **Semantic Analysis:** Type checking, symbol tables, scope resolution
- **Intermediate Representation (IR):** Three-address code, control flow graphs
- **Code Generation:** x86-64 assembly, calling conventions, stack frames
- **Program Analysis:** Dataflow analysis, reaching definitions, liveness
- **Optimization:** Loop optimizations, constant folding, dead code elimination
- **Register Allocation:** Graph coloring, linear scan
- **Advanced Topics:** Instruction scheduling, parallelization

## Reference Materials

### Assembly

- [x64 Cheat Sheet](https://cs.brown.edu/courses/cs033/docs/guides/x64_cheatsheet.pdf)
- [x86-64 Architecture Guide](http://6.035.scripts.mit.edu/fa18/x86-64-architecture-guide.html)
- [Intel x64 Manual](https://software.intel.com/en-us/articles/intel-sdm)

### Recommended Textbook

> *Modern Compiler Implementation in Java (Tiger Book)*
> Andrew W. Appel and Jens Palsberg — Cambridge University Press, 2002

## License

ISC

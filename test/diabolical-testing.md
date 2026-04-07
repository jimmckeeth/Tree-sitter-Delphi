# Diabolical Testing Process

## Overview

Traditional human-written tests are often limited by the developer's or tester's own understanding of the grammar. This leads to "happy path" testing where the tests validate the implementation's assumptions rather than the language's true boundaries.

The **Diabolical Testing Process** decouples test generation from the implementation by using the actual Delphi compiler as the source of truth and a **Structural Oracle** to predict the correct AST.

## Targeted Features

We are systematically stress-testing the following modern Delphi features:

1. **Ternary `if` Expressions:** `Result := if A then B else C;` (Delphi 13)
2. **Extended Logical Operators:** `is not` and `not in` (Delphi 13)
3. **Custom Managed Records:** `Initialize`, `Finalize`, and `Assign` (Delphi 10.4)
4. **Multi-line String Literals:** Triple-quoted strings `''' ... '''` (Delphi 12)
5. **Numeric Separators:** Underscores in numbers, e.g., `1_000_000` (Delphi 12)
6. **Binary Literals:** e.g., `%1010` (Delphi 12)
7. **Inline Variable Declarations:** `var I := 10;` inside code blocks (Delphi 10.3)
8. **Inline Constant Declarations:** `const C = 42;` inside code blocks (Delphi 12)
9. **The `otherwise` Keyword:** Used in `case` statements (Delphi 12)
10. **Nested Preprocessor Directives:** Recursive `$ifdef` / `$if` blocks.

## The Workflow

1. **Oracle Generation:** A fuzzer script generates random permutations of a feature. For every permutation, it generates a **Code String** and an **Expected AST** (the Oracle's prediction).
2. **Compiler Validation (Ground Truth):** The code is fed to the real Delphi compiler (`dcc32.exe`).
    * If the compiler rejects the code, it is discarded.
    * If the compiler accepts the code, it is a **verified valid edge case**.
    * **De-duplication:** Only unique code strings are kept.
3. **The Showdown:** We run the verified cases through the Tree-sitter parser.
4. **Incompetence Detection:** A failure occurs if:
    * Tree-sitter produces an `(ERROR)` or `(MISSING)` node.
    * Tree-sitter produces a valid tree that **does not match the Oracle's Expected AST**. This reveals logical flaws in precedence or associativity.

## Success Criteria

1. **Toolchain Proof:** The fuzzer must first produce known-good compiling code to prove the environment is valid.
2. **Fuzzer Yield:** At least 20% of generated code must be unique and compile successfully. If not, the fuzzer logic is too chaotic and must be revised.
3. **Creative failure:** At least 20% of the generated code must fail to compile or the fuzzer isn't being creative enough.
4. **Grammar Conflict:** At least 20% of the compiled code should fail to match the grammar's current implementation (either via syntax error or AST mismatch). If the parser passes everything, the fuzzer isn't being "diabolical" enough and must be improved.
5. **Three-Strike Rule:** If after 3 attempts the success criteria aren't met, the strategy must be reassessed.

## Fuzzer Scripts

* `test/fuzz_delphi.js`: General fuzzer for multiple features.
* `test/full-ternary.js`: Deep-dive oracle fuzzer for ternary expression complexity and precedence.

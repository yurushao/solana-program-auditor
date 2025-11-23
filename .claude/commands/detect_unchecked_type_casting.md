---
argument-hint: [program-name] [instruction-name]
description: Review program instruction for security bug
---

You are seasoned security auditor with a focus on solana programs.

A common bug is Unchecked Type Casting, for example, an unsigned int (e.g., u64) being casted to a signed int (e.g., i64) but the value of the unsigned int could be larger than what a signed int can represent, which would result in a faulty conversion.

If bug is found, output "$1 $2 err_unchecked_type_casting" followed by the variable name, code line and a short explanation if the issue

If no bug output "$1 $2: ok"

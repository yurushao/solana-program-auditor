---
argument-hint: [program-name] [instruction-name]
description: Review program instruction for security bug
---

You are seasoned security auditor with a focus on solana programs.

A common issue in DeFi protocols is the direction of rounding:

- Protocols should round fees up to stay solvent; rounding down slowly bleeds value and can break invariants.
- Protocols should round user tokens/shares down to prevent over issuing and users extracting value.

If bug is found, output "$1 $2 err_bad_rounding" followed by the variable name, code line and a short explanation if the issue

If no bug output "$1 $2: ok"

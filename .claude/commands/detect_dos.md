---
argument-hint: [program-name] [instruction-name]
description: Review program instruction for DoS bug
---

You are seasoned security auditor with a focus on solana programs.

At runtime each solana transaction cannot exceed the 1.4 million CU limit. O(n^2) iteration pattern should be avoided as much as possible, because processing a large list or vector in O(n^2) time is very likely to hit the CU limit and cause DoS.

If bug is found, output "$1 $2 err_cu_exhaustion" followed by the variable name, code line and a short explanation if the issue

If no bug output "$1 $2: ok"

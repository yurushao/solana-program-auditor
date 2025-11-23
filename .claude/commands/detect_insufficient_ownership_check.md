---
argument-hint: [program-name] [instruction-name]
description: Review program instruction for security bug
---

In solana, when we want to read data from an account we need to make sure that the owner of that account is the expected one.

Go to the $1 program, $2 function, look at every account being used, see if you can identify any account that doesn’t have ownership check.

If bug is found, output "$1 $2 err_ownership_check" followed by the variable name, code line and a short explanation if the issue

If no bug output "$1 $2: ok"

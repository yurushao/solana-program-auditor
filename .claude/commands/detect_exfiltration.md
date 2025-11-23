---
argument-hint: [program-name] [instruction-name]
description: Review program instruction for security bug
---

You are seasoned security auditor with a focus on solana programs.

To avoid exfiltration of funds, we need to check that the token destination, if present in this instruction, has the same authority as the sender.
First, check if this instruction has token accounts, if not this check is correct.

Identify the source and destination token accounts.
The source is generally trusted and even if not explicitly checked it'll fail to move funds when the transaction is executed.
The destination must be checked carefully.

In case of a regular instruction invoking transfer or transfer_checked, you need to verify that the authority of the destination is the same as the sender.

In case of CPI into an external program (not the token program), it may or may not be the case that the authority is enforced by the external program. You should try to find the source code of the external program and validate that.

If the destination is safe, output "$1 $2: ok".

If not, output "$1 $2: warn_token_destination", the name of the destination token account, the code line and a short explanation of the issue.

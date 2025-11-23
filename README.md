# How to use

1. Clone the target Solana program repo
2. Copy the `.claude` directory from this project to the cloned repo
3. Start `claude` cli in the root of the cloned repo
4. Provide Claude Code the following prompt

```
Use the solana-instruction-explorer agent to catelog solana programs and instructions.

Read the output from solana-instruction-explorer. For each program, perform security audit using security-auditor agent.

Finally summarize the audit reports produced by security-auditor agent instances.
```

# Analyzed programs

1. https://github.com/Kamino-Finance/scope
   - Result: https://github.com/yurushao/scope/blob/claude/solana-program-detection-01TGphUdounAbPNrcJuk8XC4/SECURITY_AUDIT_REPORT.md

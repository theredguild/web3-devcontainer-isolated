# Web3 DevContainer - Isolated

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?hide_repo_select=true&ref=main&template_repository=theredguild/web3-devcontainer-isolated)
[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/theredguild/web3-devcontainer-isolated)

⚠️ **WARNING**: This environment is designed for analyzing potentially malicious code. Use extreme caution.

## What is this?

A maximum security isolation environment for analyzing potentially malicious smart contracts, exploit code, and untrusted bytecode. Provides zero-trust malware analysis capabilities.

## What's inside?

**Analysis Tools (Minimal Set):**
- Basic hex analysis utilities
- Python 3 with minimal libraries (pyevmasm, eth-abi, eth-utils)
- File examination tools
- Pattern searching capabilities

**Maximum Security:**
- Complete air-gapping (zero network access)
- Read-only filesystem (cannot modify anything)
- Severe resource restrictions (512MB RAM, 1 CPU core)
- Ultra-restrictive seccomp profile (kills most system calls)
- Ephemeral storage only (all data disappears on exit)
- Built from scratch image (minimal attack surface)

## When to use this?

- Malware analysis of smart contracts
- Exploit code examination
- Zero-day vulnerability research
- Forensic investigation of compromised contracts
- Academic malware research
- Bug bounty hunting with suspicious contracts

## How to use?

Click a badge above to launch instantly, or clone this repo and open in VS Code with the Dev Containers extension.

**Critical limitations:**
- Cannot execute any code (analysis only)
- Cannot modify files
- No network access
- All outputs are temporary
- Very limited toolset

Basic analysis workflow:
```bash
# Verify isolation status
/tmp/isolation-status.sh

# Basic file analysis
/tmp/basic-analysis.sh suspicious-contract.sol

# Manual examination
cat contract.sol
hex-analyze contract.sol
python3 -c "import analysis_script"
```

## Need something different?

Check the [Web3 DevContainer Hub](https://github.com/theredguild/web3-devcontainer-hub) for development, secure, or audit environments.
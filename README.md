# A-Hackers-Guide Homebrew tap

Homebrew formulae for [sys1](https://github.com/A-Hackers-Guide/sys1), which pools the spare power of every computer into one cloud.

```bash
brew install a-hackers-guide/tap/sys1
```

This installs both apps:

| | |
|---|---|
| `sys0` | the client: lends this machine's spare power to a pool |
| `sys1` | the node: runs a pool and its dashboard |

Keep a node running in the background:

```bash
brew services start sys1
```

Works on macOS (Apple Silicon and Intel) and Linux (x86-64, ARM64, ARMv7).

## How this tap stays current

[`scripts/update-formula.sh`](scripts/update-formula.sh) writes `Formula/sys1.rb` from the SHA-256 checksums published with each sys1 release. A [workflow](.github/workflows/update.yml) runs it every hour, commits any change, and then installs and tests the formula on macOS and Linux.

Problems? Open an issue in the [main repository](https://github.com/A-Hackers-Guide/sys1/issues).

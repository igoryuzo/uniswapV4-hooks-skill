# V4 Hooks Skill for Claude Code

> **https://v4hooks.dev**

A community-driven Claude Code skill that helps developers build **secure** V4 hooks. This skill embeds security best practices, vulnerability patterns from real audits, and battle-tested code patterns directly into your AI-assisted development workflow.

## Why This Exists

V4 hooks are powerful but dangerous. A single vulnerability can drain user funds. "Vibe coding" smart contracts without security expertise leads to exploits.

This skill ensures that when you use Claude to develop V4 hooks, it:
- **Knows the threat model** before writing any code
- **Warns about dangerous patterns** like NoOp rug pulls
- **Provides secure code templates** based on audited implementations
- **Enforces security checklists** before deployment

Built from 20+ pages of documentation including:
- Official Uniswap V4 security framework
- Certora & ABDK audit reports
- Real exploit patterns (NoOp rug pulls)
- 50+ production hook examples

## Installation

### Using npx (Recommended)

```bash
npx skills add https://github.com/igoryuzo/uniswapV4-hooks-skill
```

### Manual Installation

1. Clone the repository:
```bash
git clone https://github.com/igoryuzo/uniswapV4-hooks-skill.git
```

2. Add to your Claude Code skills directory or configuration.

## Usage

Once installed, the skill activates automatically when you:

- Mention "uniswap", "v4", "hooks", "PoolManager", "beforeSwap", "afterSwap"
- Work with files containing hook contracts
- Ask Claude to create or review hook code

### Example Prompts

```
"Create a dynamic fee hook that increases fees during high volatility"

"Review this hook for security vulnerabilities"

"Help me implement a points reward system for swaps"

"What are the risks of using beforeSwapReturnDelta?"
```

### Explicit Invocation

```
"Using the uniswap-v4-hooks skill, create a limit order hook"
```

## What's Covered

### Security Patterns
- Access control (PoolManager verification)
- Delta accounting rules
- msg.sender identification via trusted routers
- Overflow prevention in price math
- Reentrancy protection

### Vulnerability Awareness
- NoOp/BeforeSwapReturnDelta rug pull attacks
- Fee calculation errors (from Certora audit)
- Timestamp validation issues (from ABDK audit)
- Token type hazards (rebasing, fee-on-transfer)

### Code Templates
- Base hook structure
- Permission flag configuration
- Testing patterns (Foundry invariant/fuzz)
- Router verification implementation

### Risk Assessment
- Self-scoring framework (0-33 scale)
- Audit requirement tiers
- Pre-deployment checklist

## Project Structure

```
uniswapV4-hooks-skill/
├── SKILL.md          # The skill definition (loaded by Claude Code)
├── README.md         # This file
├── CONTRIBUTING.md   # Contribution guidelines
├── LICENSE           # MIT License
└── examples/         # Example hooks (coming soon)
```

## Contributing

We welcome contributions! This is a community effort to make V4 hook development safer for everyone.

### Ways to Contribute

1. **Add vulnerability patterns** - Found a new attack vector? Document it.
2. **Improve code templates** - Better patterns from your audits or production experience.
3. **Add examples** - Real-world hook implementations with security annotations.
4. **Fix errors** - Spot something wrong? Open a PR.
5. **Expand coverage** - New V4 features, edge cases, or integration patterns.

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

### Security Disclosures

If you discover a security issue in the skill guidance itself (advice that could lead to vulnerabilities), please:

1. **Do NOT open a public issue**
2. Email the maintainers directly (add contact)
3. Allow time for correction before public disclosure

## Sources & Attribution

This skill distills knowledge from:

- [Uniswap V4 Documentation](https://docs.uniswap.org/contracts/v4/overview)
- [Uniswap V4 Security Framework](https://docs.uniswap.org/contracts/v4/security)
- [Certora TWAMM Audit](https://github.com/akshatmittal/v4-twamm-hook)
- [ABDK Consulting TWAMM Audit](https://github.com/akshatmittal/v4-twamm-hook)
- [NoOp Rug Pull Analysis](https://ivikkk.medium.com/uniswap-v4-noop-or-how-to-build-a-rug-pull-hook-4d80924286be)
- [Awesome Uniswap Hooks](https://github.com/fewwwww/awesome-uniswap-hooks)
- [Cyfrin Updraft Course](https://updraft.cyfrin.io/courses/uniswap-v4)

## Roadmap

- [ ] Add example hook implementations with inline security comments
- [ ] Create hook-specific sub-skills (dynamic fees, TWAMM, limit orders)
- [ ] Add formal verification guidance (Certora, Halmos)
- [ ] Integration with static analysis tools
- [ ] Automated security scoring based on code analysis

## License

MIT License - see [LICENSE](LICENSE)

## Disclaimer

This skill provides guidance based on known best practices and audit findings. It does **not** guarantee security. Always:

1. Get professional audits for production hooks
2. Start with limited TVL and monitoring
3. Have incident response procedures ready
4. Consider bug bounties for high-value hooks

The maintainers are not responsible for vulnerabilities in hooks developed using this skill.

---

**Built for the V4 hooks community. PRs welcome.**

**Website:** https://v4hooks.dev
**GitHub:** https://github.com/igoryuzo/uniswapV4-hooks-skill

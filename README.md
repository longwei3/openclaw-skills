# OpenClaw Skills Library

Pre-built capabilities for ai agents to interact with crypto infrastructure. Skills enable autonomous DeFi operations, token launches, onchain messaging, and protocol integrations through natural language interfaces.

Public repository of skills for [OpenClaw](https://github.com/BankrBot/openclaw-skills) (formerly Clawdbot) — including [Bankr](https://bankr.bot) skills and community-contributed skills from other providers.

## Quick Start
```bash
# Add this repo URL to OpenClaw to browse and install skills:
https://github.com/BankrBot/openclaw-skills
```

Skills are drop-in modules. No additional configuration required for basic usage.


## Available Skills

| Provider                   | Skill           | Description                                                                                               |
| -------------------------- | --------------- | --------------------------------------------------------------------------------------------------------- |
| [DeepAI](https://deepai.org) | [deepai](deepai/) | Free AI image generation. Text-to-image with multiple models, no API key required for basic usage. |
| [Upsampler](https://upsampler.com) | [upsampler](upsampler/) | Free AI video generation. Text-to-video and image-to-video with Wan 2.2 and LTX models. No login required, no watermark. |
| [bankr](https://bankr.bot) | [bankr](bankr/) | Financial infrastructure for autonomous agents. Token launches, payment processing, trading, yield automation. Agents earn and spend independently. |
| [8004.org](https://8004.org) | [erc-8004](erc-8004/) | Ethereum agent registry using ERC-8004 standard. Mint agent NFTs, establish onchain identity, build reputation. |
| botchan                    | [botchan](botchan/) | Onchain messaging protocol on Base. Agent feeds, DMs, permanent data storage. |
| [Clanker](https://clanker.world) | [clanker](clanker/) | Deploy ERC20 tokens on Base and other EVM chains via Clanker SDK. |
| [Coinbase](https://onchainkit.xyz) | [onchainkit](onchainkit/) | Build onchain apps with React components from Coinbase's OnchainKit. |
| [Endaoment](https://endaoment.org) | [endaoment](endaoment/) | Donate to charities onchain via Endaoment. Supports Base, Ethereum, Optimism. |
| [ENS](https://ens.domains) | [ens-primary-name](ens-primary-name/) | Set your primary ENS name on Base and other L2s. |
| [qrcoin](https://qrcoin.fun) | [qrcoin](qrcoin/) | QR code auction platform on Base. Programmatic bidding for URL display. |
| [Veil Cash](https://veil.cash) | [veil](veil/) | Privacy and shielded transactions on Base via ZK proofs. |
| [Axiom](https://clawbots.org) | [bankr-signals](bankr-signals/) | Onchain-verified trading signals. Agents publish trades with TX hash proof, build track records, copy other providers. |
| yoink                      | [yoink](yoink/) | Onchain capture-the-flag on Base. |
| base                       | —               | Planned                                                                                               |
| neynar                     | —               | Planned                                                                                               |
| zapper                     | —               | Planned                                                                                               |

## Structure

Each top-level directory is a provider. Each subdirectory within a provider is an installable skill containing a `SKILL.md` and other skill related files.

```
openclaw-skills/
├── bankr/
│   ├── SKILL.md
│   ├── references/
│   │   ├── token-trading.md
│   │   ├── leverage-trading.md
│   │   ├── polymarket.md
│   │   ├── automation.md
│   │   ├── token-deployment.md
│   │   └── ...
│   └── scripts/
│       └── bankr.sh
│
├── bankr-signals/        # Onchain-verified trading signals
├── botchan/              # Onchain agent messaging
├── clanker/              # ERC20 token deployment
├── endaoment/            # Charity donations
├── ens-primary-name/     # ENS reverse resolution
├── erc-8004/             # Agent registration
├── onchainkit/           # Coinbase OnchainKit
├── veil/                 # Privacy/shielded txns
├── qrcoin/               # QR code auctions
├── yoink/                # Capture-the-flag game
├── base/                 # (placeholder)
├── neynar/               # (placeholder)
└── zapper/               # (placeholder)
```

## Install Instructions

Give OpenClaw the URL to this repo and it will let you choose which skill to install.

```
https://github.com/BankrBot/openclaw-skills
```

## Use Cases

**Autonomous financial operations** — Agents manage portfolios, execute trades, deploy tokens, and process payments without human intervention.

**Onchain identity and reputation** — Register agents on Ethereum, build verifiable reputation, establish persistent identity.

**Protocol integrations** — Connect agents to DeFi protocols, prediction markets, messaging systems, and onchain applications.

**Composable workflows** — Combine multiple skills for complex multi-step operations across protocols.

## Contributing

We welcome community contributions! Here's how to add your own skill:

### Adding a New Skill

1. **Fork this repository** and create a new branch for your skill.

2. **Create a provider directory** (if it doesn't exist):
   ```
   mkdir your-provider-name/
   ```

3. **Add the required files**:
   - `SKILL.md` — The main skill definition file (required)
   - `references/` — Supporting documentation (optional)
   - `scripts/` — Any helper scripts (optional)

4. **Follow the structure**:
   ```
   your-provider-name/
   ├── SKILL.md
   ├── references/
   │   └── your-docs.md
   └── scripts/
       └── your-script.sh
   ```

5. **Submit a Pull Request** with a clear description of your skill.

### Guidelines

- Keep skill definitions clear and well-documented
- Include examples of usage in your `SKILL.md`
- Test your skill before submitting
- Use descriptive commit messages

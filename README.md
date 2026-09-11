# SkillAsset Hackathon Submission

Public, non-sensitive submission materials for SkillAsset.

SkillAsset is a confidential AI skill marketplace. Creators publish private AI workflows as callable skills. Users can run a skill and receive the result, while the underlying prompt, workflow, and orchestration logic stay private on the server.

Live site: https://app.skillasset.cc

## GWDC 2026 Korea Focus

This repository is prepared for the GWDC 2026 Korea hackathon.

Recommended track:

**TRON Challenge A: Multi-Vendor TRON Energy Rental Procurement and Cost-Comparison Assistant**

Why this direction fits SkillAsset:

- The challenge needs an assistant that collects requirements, compares external providers, explains tradeoffs, and recommends a plan.
- SkillAsset already focuses on private server-side AI workflows, callable skills, and usage-based settlement.
- A TRON Energy procurement assistant can be delivered as a SkillAsset skill: users get the comparison result, while the sourcing, normalization, and planning workflow stays private.

## What SkillAsset Demonstrates

- Confidential AI workflow execution
- Public skill discovery and calling
- Server-side black-box runtime
- Wallet-based user identity path
- Usage-based accounting model
- Creator revenue accounting concept
- TRON Nile Testnet integration path for wallet and stablecoin settlement flows

The current public production app is an early testnet-stage product. For hackathon review, the safest interpretation is:

> SkillAsset is the platform layer. The hackathon build should specialize one Skill into a TRON Energy rental procurement assistant.

## Proposed Hackathon Demo

Demo name:

**SkillAsset TRON Energy Desk**

User flow:

1. User opens SkillAsset and connects a wallet.
2. User selects the TRON Energy Desk skill.
3. User enters:
   - Required Energy amount
   - Rental duration
   - Recipient address
   - Budget
   - Latest acceptable delivery time
4. The skill compares multiple quote sources.
5. The skill normalizes units and terms.
6. The skill compares:
   - Single-provider plans
   - Split-order plans
7. The skill returns:
   - Recommended plan
   - Alternative plans
   - Full fee breakdown
   - Selection rationale
   - Infeasibility explanation when no plan meets constraints

## Repository Contents

```text
skillasset-hackathon/
├── README.md
├── docs/
│   ├── architecture.md
│   ├── demo-script.md
│   └── security-and-sanitization.md
├── screenshots/
│   └── README.md
├── .gitignore
└── LICENSE
```

This repository intentionally does not include the production source code, database files, deployment scripts, private environment files, wallet secrets, API keys, server runtime payloads, or unpublished skill content.

## Links

- Product: https://app.skillasset.cc
- Blog: https://app.skillasset.cc/blog.html
- Chinese article: https://app.skillasset.cc/zh/blog/selling-prompts-is-broken.html
- GWDC Hackathon: https://www.gwdc.net/hackathon.html

## Current Status

- Public app is live.
- Public market currently shows early example skills.
- Hackathon-specific TRON Energy Desk should be treated as the focused challenge implementation direction.
- TRON Nile Testnet is the target/current testnet path for wallet and settlement integration.

## Sensitive Information Policy

Do not commit:

- `.env` files
- private keys or seed phrases
- production database files
- server credentials
- deployment scripts with host/user details
- API keys
- private prompts
- encrypted skill payloads
- user data or transaction exports

See [docs/security-and-sanitization.md](docs/security-and-sanitization.md).

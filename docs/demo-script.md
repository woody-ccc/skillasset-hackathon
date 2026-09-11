# Demo Script

This script is intended for a short hackathon demo or judge walkthrough.

## 30-Second Pitch

SkillAsset turns private AI workflows into callable skills.

For the GWDC TRON challenge, we use SkillAsset as the platform layer for a TRON Energy rental procurement assistant. A user describes how much Energy they need, how long they need it, and their constraints. The skill compares provider quotes, evaluates single-provider and split-order plans, and returns a transparent cost breakdown.

The user receives the decision, but the sourcing and comparison workflow stays private.

## Demo Flow

### 1. Open SkillAsset

Open:

https://app.skillasset.cc

Show:

- Public skill marketplace
- AI Chat
- Wallet-based user path
- Blog explaining why prompt-selling is structurally weak

### 2. Explain the Challenge Fit

GWDC TRON Challenge A asks builders to create a multi-vendor TRON Energy rental procurement and cost-comparison assistant.

SkillAsset is a strong base because the challenge is fundamentally an AI workflow:

- collect requirements
- gather quotes
- normalize terms
- compare plans
- explain the recommendation
- keep the workflow private

### 3. Show the Proposed Skill

Demo skill name:

**TRON Energy Desk**

Example user input:

```text
I need 120,000 Energy for a TRC-20 transaction batch.
Rental duration: 1 hour.
Recipient address: TXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Budget: 35 TRX equivalent.
Latest delivery time: within 5 minutes.

Compare available providers and tell me whether a single-provider order or split order is better.
```

Expected answer structure:

```text
Recommended plan
- Provider(s)
- Energy amount
- Duration
- Delivery estimate
- Total cost

Alternatives
- Single-provider option
- Split-order option

Cost breakdown
- Rental fee
- Service fee
- On-chain fee
- Total

Rationale
- Why this plan meets the user's constraints
- What tradeoffs were rejected
```

### 4. Explain Privacy

The user gets the procurement result.

They do not get:

- provider scoring logic
- quote normalization rules
- private prompt
- internal planning workflow

This is the core SkillAsset idea.

### 5. Explain Testnet Status

SkillAsset is at early testnet stage. TRON Nile Testnet is the target/current path for wallet and settlement flow validation.

The hackathon build should focus on Challenge A's acceptance criteria:

- at least two real quote sources
- normalized provider terms
- single-provider vs split-order comparison
- full fee breakdown
- clear recommendation and infeasibility handling

## Judge Q&A Notes

### Is this just a prompt marketplace?

No. Users do not buy or receive prompts. They run a server-side skill and receive the output.

### Why does this need Web3?

The product needs wallet identity, stablecoin settlement, creator accounting, and eventually auditable on-chain payment flows. The TRON Energy Desk use case is also directly tied to TRON resource optimization.

### What is public in this repository?

Only safe submission materials: product summary, architecture, demo script, and sanitization notes.

### What is intentionally not public?

Production code, private workflows, environment variables, deployment details, keys, databases, and user data.

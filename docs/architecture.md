# Architecture Overview

This document describes the public, non-sensitive architecture of SkillAsset and the proposed hackathon adaptation.

## Product Layer

SkillAsset separates the visible user experience from the private workflow that powers each skill.

```text
Creator
  -> publishes a private workflow
  -> SkillAsset stores and executes it server-side
  -> user calls the public skill
  -> user receives the output, not the original workflow
```

## Runtime Model

High-level flow:

1. User selects a public skill.
2. User sends a request.
3. The server assembles the context.
4. The skill workflow runs inside the server runtime.
5. The AI provider returns output and usage data.
6. SkillAsset records the usage and cost categories.
7. The user receives the final answer.

The browser does not receive the protected workflow.

## Hackathon Adaptation: TRON Energy Desk

For GWDC TRON Challenge A, SkillAsset can specialize one skill into a TRON Energy rental procurement assistant.

```text
User request
  -> Energy requirement parser
  -> quote source adapters
  -> quote normalization
  -> constraint solver
  -> cost breakdown
  -> recommended plan
```

### Inputs

- Required Energy amount
- Rental duration
- Recipient address
- Budget
- Latest acceptable delivery time

### Quote Data

The Challenge A acceptance criteria require real quote sources from at least two providers.

The public repository does not include provider API keys or private provider credentials. In a demo build, source adapters should read from public endpoints or from approved test credentials configured outside the repository.

### Plan Comparison

The assistant should compare:

- Single-provider plan
- Multi-provider split plan
- Feasible alternatives
- No-plan explanation if constraints cannot be met

### Cost Breakdown

The result should show:

- Rental fee
- Service fee, if any
- On-chain fee, if any
- Total cost
- Provider terms
- Selection rationale

## Security Boundary

This public repository only describes architecture and demo behavior.

It does not contain:

- Production backend source
- database files
- environment variables
- deployment configuration
- wallet private keys
- API keys
- protected skill payloads
- private prompts or workflows

## Why This Matters

Selling raw prompts is weak because the asset is exposed once the buyer sees it. SkillAsset takes the opposite approach: the user can call the capability, while the creator's original workflow remains private.

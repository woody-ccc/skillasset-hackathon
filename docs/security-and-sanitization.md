# Security and Sanitization Notes

This repository is public by design.

It is intentionally limited to safe hackathon submission materials. It should never become a mirror of the production SkillAsset repository.

## Do Not Commit

- `.env` or `.env.*`
- private keys
- seed phrases
- API keys
- database files
- production logs
- deployment scripts with server details
- SSH config
- wallet configuration
- production contract administration data
- raw user records
- transaction exports containing private user data
- private prompts
- protected skill payloads
- encrypted production skill bundles

## Allowed Content

- Project summary
- Architecture diagrams or descriptions
- Demo script
- Public product screenshots after review
- Public website links
- Public blog links
- Public challenge references
- Non-sensitive roadmap notes

## Screenshot Rules

Before adding a screenshot:

1. Remove wallet addresses unless they are public demo addresses.
2. Remove user balances unless they are fake demo values.
3. Remove admin panels.
4. Remove server URLs, internal IDs, and logs.
5. Remove any private skill text.
6. Check that browser tabs, bookmarks, and extensions do not reveal private information.

## Public Repository Purpose

This repository exists to help judges, ecosystem teams, and collaborators understand the project without exposing production internals.

If detailed technical review is required, provide a separate private walkthrough or limited-access review package.

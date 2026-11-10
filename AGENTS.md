# AGENTS.md

## Project overview

This repository is a Cursor plugin for the remote Coralogix MCP server. It packages a local plugin configuration, prompt/skill definitions, and rules used by Cursor to connect to Coralogix observability tooling.

Key files:
- `mcp.json` — default MCP server configuration for the plugin
- `rules/` — Cursor rule files used to guide agent behavior
- `skills/` — reusable, user-facing setup/configuration skills
- `.cursor-plugin/` — local plugin assets copied into Cursor for testing
- `README.md` — user-facing setup and usage docs

## Working conventions

- Prefer small, targeted edits that preserve the plugin’s existing structure.
- Keep configuration changes aligned with the remote MCP model and Cursor plugin conventions.
- If a change affects local installation or plugin packaging, validate with `make dev`.
- Do not duplicate the official product documentation; link to it instead when useful.
- Preserve the existing minimal, practical style used in this project.

## Local development and validation

Use these commands from the repo root:

```bash
make dev
make unlink
```

`make dev` copies the plugin into Cursor’s local plugin directory for testing, then reload Cursor and run `/cx-setup`.

## Commercial licensing guidance for reseller and business models

This project may be used in commercial, SaaS, nonprofit, and partner contexts. Treat the following as operational guidance for product and partner design, not formal legal advice.

### 1) SaaS and software licensing patterns

- `SaaS subscription`: best for ongoing access, support, and feature updates.
- `Per-seat`: useful for internal teams and small business deployments.
- `Usage-based`: appropriate when consumption varies strongly by volume, transactions, or API calls.
- `Annual enterprise`: common for midsize and large organizations with SLAs and onboarding.

### 2) Nonprofit and authorized charitable organizations

- Prefer discounted or nonprofit tiers with clear eligibility checks.
- Require a documented nonprofit status, grant or institutional relationship, or authorized charitable-use declaration when applicable.
- Separate nonprofit commercial use from internal operational use to avoid policy ambiguity.
- Keep renewal and support terms simple, especially for mission-driven organizations.

### 3) SMEs and PYMEs

- Use simpler licensing bundles: starter, growth, and enterprise tiers.
- Bundle onboarding and support into a managed-services add-on where necessary.
- Offer annual contracts with monthly billing options for cash-flow flexibility.
- Keep reseller and white-label terms explicit for partner-led deployments.

### 4) SAS / SaaS company reseller model

- Define reseller margin, support responsibilities, and customer ownership clearly.
- Keep the reseller agreement separate from the end-user license agreement.
- State whether the reseller may white-label, integrate, or provide managed services.
- Include support escalation paths, uptime commitments, and data-handling responsibilities.

### 5) Resale and partner channel model

- Put distribution terms in a channel or reseller agreement.
- Clarify: pricing, territory, customer assignment, renewal rights, and refund policy.
- Maintain audit rights for license compliance and usage metrics.
- Ensure no transfer of IP or data ownership without explicit authorization.

### 6) Recommended default approach

For most business use cases, the cleanest model is:
- `Core SaaS subscription` for end users or organizations
- `Partner reseller agreement` for third-party sellers
- `Nonprofit/impact discount tier` for eligible charitable or public-interest organizations
- `Enterprise add-ons` for SLAs, support, and custom deployment needs

## Important reminder

Final legal terms, contract structure, and local compliance must be reviewed by qualified counsel. This guidance is intended to support product and partner strategy, not replace a legal review.

---
title: 'KNEL — Shared Services Proposal (Draft)'
menu: 'KNEL — Shared Services Proposal (Draft)'
---

# KNEL — Shared Services Proposal (Draft)

Purpose
- Establish KNEL as the shared-services backbone across all LLCs with simple, auditable intercompany practices, minimal overhead, and portfolio-level visibility.

Scope (current)
- Identity/Access: OIDC SSO for all Cloudron apps (Gitea, Redmine, Matomo, Documenso, others).
- ERP/CRM: Dolibarr per-LLC, plus KNEL, Board, and Family Office instances.
- Infra: Cloudron automation for DNS/SSL/backups/upgrades; infra base cost ≈ $100/month.

Architecture and Operating Model
- Tenancy: Keep Dolibarr single-tenant per LLC. KNEL provides shared services to each LLC.
- Roles: Standardize groups/roles: Owner, Operator, Contributor, Viewer. Map these to OIDC groups.
- Inventory: Maintain a simple CMDB list of Cloudron apps with tags: `biz=<slug>`, `env=prod|staging`, `slo=tier-1|2|3`, `cost_center=KNEL:<sku>`.
- Backups/DR: Define RPO/RTO by tier (suggested: Tier‑1 RPO 6h, RTO 4h; Tier‑2 RPO 24h, RTO 1d; Tier‑3 best effort). Quarterly restore tests.

Intercompany Accounting (Lightweight)
- Historical investments: Track RackRental/Suborbital large balances as intercompany loans to be repaid before any distributions. For small/legacy domain fees, waive or treat as immaterial.
- Base infra cost ($100/mo): Keep at KNEL until a business generates revenue above a defined threshold; then begin simple recharges. Example threshold: revenue ≥ $500/mo → recharge a flat $10–$20/mo.
- Price book: Publish a KNEL internal price list (flat rates) for common services (e.g., “Cloudron app slot,” “Matomo property,” “Gitea org,” “Documenso seats”). Keep rates nominal; objective is accountability, not profit.
- Dolibarr: KNEL is Supplier; each LLC is Customer. Use one recurring invoice per LLC per month (may be $0 if below threshold) plus ad‑hoc for exceptional items.
- Approvals/Aging: 1‑step approval; monthly statement pack; soft remediation (freeze non‑critical services after 60 days, with manual override).

Cloudron/Infra Practices
- App tagging and nightly inventory export (CSV/JSON) for reconciliation. Manual mapping acceptable initially.
- Change mgmt: Simple maintenance window and Markdown change log with Git tags.
- Monitoring: Monthly uptime report by tier; backup success rates.

Analytics and Documents
- Matomo: Per‑business site IDs with a portfolio roll‑up dashboard (visits, conversions, goal completions, top referrers). 12–24 month retention.
- Documenso: Template library for JV, Intercompany Agreement, SOW, NDA (prioritize later). Standardize signer roles.
- Redmine: Single instance with per‑LLC projects. Standard issue types; optional time-tracking for KNEL billable support if needed.

Governance and Review
- CPA review: Have CPA review intercompany policy and price book prior to significant revenue.
- Security: OIDC is the single source of truth. Quarterly access reviews of groups/roles per LLC.
- Policy docs: Versioned in IBP (public) with links out to canonical legal repos.

Open Decisions (for you)
- Accounting basis (cash vs accrual) and CPA preferences.
- Revenue threshold and flat recharge amounts per LLC.
- Exact RPO/RTO by tier and which apps are Tier‑1.
- Documenso template prioritization order.
- Redmine time-tracking usage for KNEL support.

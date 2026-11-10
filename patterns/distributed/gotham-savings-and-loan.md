# Gotham Savings & Loan: the canon

The running example of the notebook's tutorials. Gotham S&L is a fictional bank in a
city you already know is fictional; every incident is a composite, and the problems are
real. This page is the single source of truth for the bank's architecture and incident
history. Series pages cite it; if a page contradicts it, the page is wrong.

## House rule

Money moves exactly once, or someone has a very bad week.

## The architecture

- **The ledger** - the core banking system. The one source of truth, and the one system nobody is allowed to break.
- **The payments gateway** - cards, transfers, standing orders. Talks to external networks that answer late, twice, or not at all.
- **Onboarding and origination** - account opening and loan origination. Workflows that run for days and touch a dozen systems, some of them other companies'.
- **Statements and archival** - the read path for seven years of history.
- **The agent desk** - the new initiative: LLM agents assisting operations, onboarding, and reconciliation.

## Incident history

Recorded as the series publishes; each entry links the page that dissects it.

| Incident | Dissected in |
|----------|--------------|
| (none recorded yet) | |

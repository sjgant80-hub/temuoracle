# TemuOracle

**Live:** [sjgant80-hub.github.io/temuoracle](https://sjgant80-hub.github.io/temuoracle/)

**The same enterprise software, for the price your wallet recognised.**

A sovereign single-file hub that indexes the entire Fall* enterprise suite — every NetSuite / Oracle Corp surface, replaced by a tool that runs from `file://`, stores in IndexedDB, and costs nothing forever.

Prime 521 · MIT · ◊·κ=1

---

## For end-users

TemuOracle is the launchpad for 17 sovereign enterprise tools. Open the page, see the stack, click a card, you're in.

The architecture mirrors a real ERP stack:

- **DATA** — FallBase (Oracle Database)
- **LEDGER** — FallLedger (Oracle GL / NetSuite ledger)
- **CRM / OPS / MKTG** — FallAccount, FallForce, FallReach, FallCRM, FallSalesCRM, FallList, FallSlot, FallForm, FallFlow, FallInvoice, FallAP, fallcore-factory, FallAccount Trades
- **APP BUILDER** — FallBuild (Oracle APEX)
- **REPORTING** — FallReport (Oracle Analytics / Hyperion)

Press **Ctrl+K** for the Ω autopilot. Type what you want to do ("overdue invoices", "post a journal entry", "cashflow this month") and TemuOracle routes you to the right tool. No tutorial, no setup.

Every tool card has a live-status dot. Green = online. The manifest export gives you a portable JSON of the whole suite — primes, URLs, descriptions — for audit or fork.

The brand is forkable. Settings → engine name. Default ships as TemuOracle; change it to FallEnterprise or anything you like. The engine slug stays `temuoracle` either way.

### What it replaces

| Oracle slot | Annual cost | TemuOracle |
|---|---|---|
| Oracle Cloud Suite | premium enterprise pricing / user | Free forever |
| NetSuite ERP | mid-market SaaS pricing / user | Free forever |

## For developers

Single HTML file. Vanilla JS. No build step. No npm. Runs from `file://`.

- **Prime:** 521
- **Tool slug:** `temuoracle`
- **Version:** 1.0.0
- **Pattern:** same as FallStudio — a hub that indexes phase tools — applied to the enterprise wedge instead of the studio wedge.

### Stack

- Cascade T0/T2/T3 per estate doctrine. T0 keyword router handles everything offline; T3 (BYOK Anthropic/Gemini/OpenAI/OpenRouter) parses arbitrary intent into `{tool, hint}` JSON.
- KONOMI sovereign shim baked at end of script.
- fallmesh BroadcastChannel on `fall-signal`, prime 521.
- postMessage API: `action: 'ping' | 'list' | 'route'`. `list` returns all 17 tool ids. `route` runs the T0 router on a query.
- PWA manifest via data: URL — installable.
- IndexedDB persistence for settings (brand override + BYOK keys).
- Live status pings via `fetch(..., {mode:'no-cors'})` HEAD-style.

### Trademark / parody posture

"TemuOracle" puns Temu (trademark of PDD Holdings) and Oracle (trademark of Oracle Corporation). The name is parody commentary on enterprise software pricing — the joke is that the same software fits in a single HTML file with the same price tag your wallet recognises from Temu. Not affiliated with, endorsed by, or connected to either company. This is sovereign MIT software.

### File layout

```
temuoracle/
  index.html      single-file hub
  README.md       this file
  LICENSE         MIT
  .nojekyll       Pages legacy deploy
```

### Build / deploy

No build. Open `index.html`. For Pages: push to `sjgant80-hub/temuoracle`, deploy type **legacy** (`.nojekyll` is already in place).

### Estate seal

◊·κ=1 · prime 521 · MIT

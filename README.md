---
title: "Polkadex Orderbook Frontend Documentation"
description: "Browse the real engineering docs for Polkadex's non-custodial orderbook trading frontend: architecture, deployment, backend contract, bridge, and faucet."
---

# Orderbook Frontend (OFE)

The Polkadex Orderbook trading interface — a non-custodial, orderbook-based DEX
frontend. Next.js 15 App Router, in a Turborepo monorepo, deployed to a
standalone server behind nginx and Cloudflare.

This site aggregates the engineering documentation that already lives across
the [`Orderbook-Frontend`](https://github.com/Polkadex-Substrate/Orderbook-Frontend)
monorepo into one browsable, searchable place.

## Start here

| Doc | What it covers |
|---|---|
| [Architecture](/architecture) | How the pieces fit, where data comes from, the traps |
| [Deployment](/deployment) | VPS deploy, nginx, Cloudflare, maintenance mode, announcements |
| [Backend Contract](/backend-contract) | What the frontend expects of the backends and the chain |
| [Chart Package](/chart) | The `@orderbook/chart` package and its datafeed contract |
| [Bridge: Adding a Token or Chain](/bridge/adding-new-token-or-chain) | Extending the Hyperbridge-backed bridge |
| [Bridge: API-Driven Config Plan](/bridge/api-driven-config-migration-plan) | Moving bridge config off hardcoded lists |
| [Faucet Flow](/faucet/faucet-flow) | Testnet faucet: routing, state, and backend API |

## Workspaces

```
apps/
  hestia/            the trading app - the only app
packages/
  core/              chain + backend access, providers, hooks, helpers
  chart/             candle/depth chart (lightweight-charts)
  format/            number formatting
```

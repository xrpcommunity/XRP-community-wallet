<p align="center">
  <img src="public/logo-black.png" alt="Ripple Community Wallet" width="180" />
</p>

<h1 align="center">Ripple Community Wallet</h1>

<p align="center">
  <strong>A fully decentralized wallet - built by the community, for the community.</strong>
</p>

<p align="center">
  <a href="https://xrp.community">Website</a> &nbsp;·&nbsp;
  <a href="https://wallet.xrp.community">Web wallet app</a> &nbsp;·&nbsp;
  <a href="https://docs.xrp.community">Documentation</a> &nbsp;·&nbsp;
</p>

> **Placeholder.** The links above are temporary placeholders. Before publishing,
> replace `https://xrp.community` with the real website, web app, documentation, and
> community channel URLs. You can remove this block once the links are finalized.

---

## About

Ripple Community Wallet is a non-custodial wallet for the XRP ecosystem and
compatible networks. Private keys and your seed phrase never leave your device:
everything is stored encrypted locally, in the user's browser. There are no
servers holding funds and no intermediaries — you are in full control of your
assets.

The project is built by the community and for the community: open source,
transparent decisions, no hidden telemetry, and no collection of personal data.

## Features

- **Non-custodial storage.** The seed phrase and keys are encrypted locally and
  stored in IndexedDB; a user password is required to unlock.
- **Wallet creation and import.** Generate and restore a wallet from a seed
  phrase (BIP39 / BIP32 standards).
- **Hardware wallets.** Ledger support for XRP via WebHID.
- **Multi-chain.** XRP Ledger and EVM networks in a single interface: native
  coins, a curated ERC-20 list, and support for custom tokens.
- **Send and receive.** Transfers with address validation and QR codes for
  receiving funds.
- **Portfolio.** Aggregated balance across networks and tokens with up-to-date
  prices.
- **Transaction history.** A list of operations with links to block explorers.
- **Staking.** A section for participating in community staking.
- **Internationalization.** 11 languages, including RTL (Arabic); the language is
  detected automatically from browser settings.
- **Responsive UI.** Mobile / tablet / desktop, light and dark themes.

## Supported networks

| Network | Ticker | Explorer |
|---------|--------|----------|
| XRP Ledger | XRP | https://livenet.xrpl.org |
| Ethereum | ETH | https://etherscan.io |
| BNB Smart Chain | BNB | https://bscscan.com |
| Polygon | MATIC | https://polygonscan.com |

## Tech stack

React 18 · TypeScript (strict) · Vite · React Router · TanStack Query · Zustand ·
Tailwind CSS · Radix UI · i18next · `xrpl` / `ripple-keypairs` · `viem` ·
`@scure/bip39` · `@noble/hashes` · IndexedDB (`idb`).

## Local development

### Requirements

- Node.js >= 20
- pnpm >= 9

### Workspace dependencies

This app is part of the Ripple Community monorepo and relies on shared workspace
packages: `@rc/types`, `@rc/ui`, `@rc/i18n`, `@rc/api-client`, and `@rc/config`
(the latter provides the base `tsconfig`). These packages must be available to
build — run the commands from the monorepo root, or make sure the `@rc/*`
packages are present in your environment.

### Commands

```bash
# Install dependencies
pnpm install

# Dev server (Vite) — http://localhost:5173
pnpm dev

# Production build into ./dist
pnpm build

# Preview the production build locally
pnpm preview

# Unit tests (Vitest)
pnpm test

# Type checking
pnpm typecheck
```

## Project structure

```
src/
  app/        — application root, providers, routing
  features/   — feature modules (onboarding, send, receive,
                portfolio, history, staking, settings, ...)
  layouts/    — page layouts
  lib/        — crypto, network logic (chains), explorers, theme, wallet
public/       — static assets (logos, favicon)
```

## Security

- Keys and the seed phrase are never sent to a server and are stored only in
  encrypted form on the device.
- Wallet access is protected by a password; unlocking happens locally.
- Before using real funds, always back up your seed phrase in a safe place —
  recovery is only possible with it.

## Community and license

This project is built by the XRP community. Ways to contribute, feedback
channels, and license terms will be published on the project website.
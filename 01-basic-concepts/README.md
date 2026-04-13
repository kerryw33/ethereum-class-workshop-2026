# Lesson 01 — Basic concepts

This directory is **lesson 1** in the workshop monorepo. It is a [Scaffold-ETH 2](https://scaffoldeth.io) application used for introductory Solidity, tests, and local dapp development.

## Start here (lesson hub)

**[→ wiki/README.md](./wiki/README.md)** is the main entry for this lesson: setup in the monorepo, the **Simple Staking** practical (TODOs and test commands), and links to the [FinHubSA Simple Staking wiki](https://github.com/FinHubSA/ethereum-class-workshop-2025/wiki/Simple-Staking-Example).

Supporting pages:

- [wiki/setup.md](./wiki/setup.md) — prerequisites, remotes, and where the contracts live  
- [wiki/simple-staking-example.md](./wiki/simple-staking-example.md) — TDD notes and the full task checklist  

---

## Acknowledgements — Scaffold-ETH 2

This lesson is built with **[Scaffold-ETH 2](https://scaffoldeth.io)** — an open-source toolkit for Ethereum dapps (smart contracts plus a Next.js frontend). The upstream project and docs are the authoritative reference for the stack.

<h4 align="center">
  <a href="https://docs.scaffoldeth.io">Documentation</a> |
  <a href="https://scaffoldeth.io">Website</a>
</h4>

🧪 Scaffold-ETH 2 makes it easier to write contracts, deploy them, and build UIs that talk to the chain.

⚙️ Built with Next.js, RainbowKit, Hardhat, Wagmi, Viem, and TypeScript.

- ✅ **Contract hot reload**: the frontend tracks contract changes as you edit.  
- 🪝 **[Custom hooks](https://docs.scaffoldeth.io/hooks/)**: React hooks around [wagmi](https://wagmi.sh/) with TypeScript-friendly contract calls.  
- 🧱 [**Components**](https://docs.scaffoldeth.io/components/): common web3 UI pieces.  
- 🔥 **Burner wallet & local faucet**: fast iteration on a local chain.  
- 🔐 **Wallet providers**: connect and switch networks from the app.

![Debug Contracts tab](https://github.com/scaffold-eth/scaffold-eth-2/assets/55535804/b237af0c-5027-4849-a5c1-2e31495cccb1)

Course context: practicals align with ideas from **[Speedrun Ethereum](https://speedrunethereum.com)** and related workshop material; the lesson-specific steps and staking exercise are documented in **[wiki/README.md](./wiki/README.md)**.

## Requirements

- [Node.js (>= v18.18)](https://nodejs.org/en/download/)  
- [Yarn](https://yarnpkg.com/getting-started/install) (this package uses Yarn 3; see `.yarnrc.yml`)  
- [Git](https://git-scm.com/downloads)  

## Quickstart (Scaffold-ETH 2)

From **this folder** (`01-basic-concepts/`):

1. Install dependencies:

   ```bash
   yarn install
   ```

2. Terminal 1 — local chain:

   ```bash
   yarn chain
   ```

3. Terminal 2 — deploy:

   ```bash
   yarn deploy
   ```

4. Terminal 3 — Next.js app:

   ```bash
   yarn start
   ```

Open [http://localhost:3000](http://localhost:3000). Use **Debug Contracts** to call your contracts. Configure networks and behaviour in `packages/nextjs/scaffold.config.ts`. Hardhat settings live in `packages/hardhat/hardhat.config.ts`.

Run contract tests:

```bash
yarn test
```

For the staking lesson only:

```bash
yarn workspace @se-2/hardhat test test/StakingContract.ts
```

(or `cd packages/hardhat && yarn test test/StakingContract.ts` — see the wiki).

**Where to edit**

- Contracts: `packages/hardhat/contracts`  
- Deploy scripts: `packages/hardhat/deploy`  
- Frontend entry: `packages/nextjs/app/page.tsx` — [Next.js routing docs](https://nextjs.org/docs/app/building-your-application/routing/defining-routes)  

## Documentation

- **This lesson**: [wiki/README.md](./wiki/README.md)  
- **Scaffold-ETH 2**: [docs.scaffoldeth.io](https://docs.scaffoldeth.io) and [scaffoldeth.io](https://scaffoldeth.io)  

## Contributing to Scaffold-ETH 2

Scaffold-ETH 2 welcomes contributions. See the upstream [CONTRIBUTING.md](https://github.com/scaffold-eth/scaffold-eth-2/blob/main/CONTRIBUTING.md).

# Ethereum class workshop (2026)

Monorepo for the **Fintech and Cryptocurrencies** Ethereum practicals. Each numbered folder is a full **[Scaffold-ETH 2](https://scaffoldeth.io)** app (Hardhat + Next.js) you run on its own.

## Documentation

- **[Course wiki →](wiki/README.md)** — setup notes, Solidity basics, and copied practicals (staking, NFT, UI). Start here for reading and navigation.
- **Lesson wikis** — each lesson has extra paths and checklists:
  - [Lesson 01](01-basic-concepts/wiki/README.md)
  - [Lesson 02](02-non-fungible-tokens/wiki/README.md)
  - [Lesson 03](03-ui-non-fungible-token/wiki/README.md)

## Lessons

| # | Folder | Focus |
|---|--------|--------|
| 1 | [`01-basic-concepts/`](01-basic-concepts/) | Staking contract, tests, re-entrancy |
| 2 | [`02-non-fungible-tokens/`](02-non-fungible-tokens/) | ERC-721, minting, transfers |
| 3 | [`03-ui-non-fungible-token/`](03-ui-non-fungible-token/) | Approvals, My NFTs UI, Sepolia |

Work through them in order. Open the lesson **README** in each folder for Scaffold-ETH quickstart and links.

## Quick start (any lesson)

```bash
cd 01-basic-concepts   # or 02-… / 03-…
yarn install
```

Then, in separate terminals from that same folder:

```bash
yarn chain
yarn deploy
yarn start
```

Open [http://localhost:3000](http://localhost:3000).

## Requirements

- **Node.js** ≥ 18.18 (see each lesson’s `package.json` / README)
- **Yarn** (lessons use Yarn 3)
- **Git**

## Contact

**Takunda Chirema** — [takunda.chirema@uct.ac.za](mailto:takunda.chirema@uct.ac.za)

Course material builds on work by **Sabine Schaler** and the [FinHubSA ethereum-class-workshop-2025](https://github.com/FinHubSA/ethereum-class-workshop-2025/wiki) wiki, mirrored and adapted in [`wiki/`](wiki/).

## Links

- [Scaffold-ETH 2 docs](https://docs.scaffoldeth.io)
- [Solidity docs](https://docs.soliditylang.org/)

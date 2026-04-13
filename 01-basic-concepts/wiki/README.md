# Lesson 01 — Wiki

This folder holds lesson-specific notes that mirror and adapt the [Simple Staking Example](https://github.com/FinHubSA/ethereum-class-workshop-2025/wiki/Simple-Staking-Example) wiki from the FinHubSA `ethereum-class-workshop-2025` course.

## Contents

- **[Setup for this lesson](./setup.md)** — how to work inside this monorepo lesson folder.
- **[Simple Staking Example — practical & TODOs](./simple-staking-example.md)** — test-driven workflow, contract overview, and the full checklist of tasks from the wiki.

## Quick start

From the repository root:

```bash
cd 01-basic-concepts
yarn install
```

Run the staking tests. From `01-basic-concepts`:

```bash
yarn workspace @se-2/hardhat test test/StakingContract.ts
```

If that fails in your environment, run Hardhat in the hardhat package:

```bash
cd packages/hardhat
yarn test test/StakingContract.ts
```

Or run all Hardhat tests from `01-basic-concepts`:

```bash
yarn test
```

## Source

Original tutorial wiki: [Simple Staking Example · FinHubSA/ethereum-class-workshop-2025](https://github.com/FinHubSA/ethereum-class-workshop-2025/wiki/Simple-Staking-Example).

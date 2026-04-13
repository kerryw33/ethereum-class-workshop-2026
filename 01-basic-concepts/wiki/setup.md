# Setup — Lesson 01 (Basic concepts)

This lesson is the Scaffold-ETH 2 app inside `01-basic-concepts/`. The parent repository is a **monorepo**: each top-level folder (for example `01-basic-concepts/`) is a self-contained lesson.

## Prerequisites

- [Node.js](https://nodejs.org/en/download/) (>= 18.18)
- [Yarn](https://yarnpkg.com/getting-started/install) (this project uses Yarn 3; see `.yarnrc.yml` in the lesson folder)
- [Git](https://git-scm.com/downloads)

## 1. Open the lesson package

From the **monorepo root** (the folder that contains `01-basic-concepts/`):

```bash
cd 01-basic-concepts
```

All commands below assume your current working directory is `01-basic-concepts/` unless noted.

## 2. Install dependencies

```bash
yarn install
```

## 3. Git remotes (optional, if you fork the monorepo)

If the course maintainers publish the monorepo under an organization and you work from your own fork:

1. Check remotes:

   ```bash
   git remote -v
   ```

2. Point `origin` at **your** GitHub repository (the URL you copied when you created the fork):

   ```bash
   git remote set-url origin <your-fork-url>
   ```

3. Add the course repository as `upstream` so you can fetch updates:

   ```bash
   git remote add upstream <course-monorepo-url>
   git remote -v
   ```

You should see `origin` (your fork) and `upstream` (the source you pull from). Do not force-push to `upstream` if you do not own it.

### Note on branches vs. this layout

The [original FinHub wiki](https://github.com/FinHubSA/ethereum-class-workshop-2025/wiki/Simple-Staking-Example) used a branch named `basic-concepts-tut` inside a single workshop repository. In **this** monorepo, the same practical lives in `01-basic-concepts/`; use your normal branch workflow (for example `main` or a feature branch) instead of checking out `basic-concepts-tut`.

## 4. Daily development (optional)

Typical Scaffold-ETH 2 flow from `01-basic-concepts/`:

1. Terminal 1 — local chain:

   ```bash
   yarn chain
   ```

2. Terminal 2 — deploy contracts:

   ```bash
   yarn deploy
   ```

3. Terminal 3 — Next.js app:

   ```bash
   yarn start
   ```

Open [http://localhost:3000](http://localhost:3000) and use **Debug Contracts** to interact with deployed contracts.

For **this practical**, focusing on tests is enough:

```bash
yarn workspace @se-2/hardhat test test/StakingContract.ts
```

Equivalent from the hardhat package directory:

```bash
cd packages/hardhat
yarn test test/StakingContract.ts
```

## 5. Where the code lives

| What | Path |
|------|------|
| Staking contract | `packages/hardhat/contracts/StakingContract.sol` |
| Attacker (re-entrancy demo) | `packages/hardhat/contracts/AttackerContract.sol` |
| Tests | `packages/hardhat/test/StakingContract.ts` |

See [simple-staking-example.md](./simple-staking-example.md) for the step-by-step TODO list.

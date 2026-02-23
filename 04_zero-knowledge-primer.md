# Zero Knowledge: Proofs, SNARKs, STARKs, Rollups — A Basic Primer for the Uninitiated

*Originally published on Blockstrata.co by Bruce Milligan — October 2022*

> **"ZK SNARKs are as important a technological breakthrough as blockchains themselves"**
> — Vitalik Buterin, September 2022

If Vitalik is correct, shouldn't you know a bit more about them, just in case? Spend 8–10 minutes here to get you started.

---

> **TLDR:** zk-proofs were the original mathematical innovation. zk-rollups can help batch transactions and scale blockchains. zk-SNARKs and zk-STARKs are both methods of implementing zk-rollups. zk-SNARKs were originally used to facilitate private transactions on Zcash. Several projects are now working with zk-rollups in a race to scale blockchains, particularly Ethereum. zkEVM is the latest development, allowing smart contracts to be included rather than just simple transactions. A future state can be imagined with hundreds of thousands or even millions of transactions settling via multi-layered, connected zk-rollup blockchains.

---

## What is Zero Knowledge?

"ZK" is shorthand for **zk-proofs** — a breakthrough mathematical approach to sharing information. A zk-proof is defined as:

> "A method by which one party (the prover) can prove to another party (the verifier) that a given statement is true, while the prover avoids conveying any additional information apart from the fact that the statement is indeed true."

A quick metaphor: imagine you are looking at a 'Where's Wally?' children's puzzle and want to prove to a friend you know where Wally is without revealing how to find him. Your friend looks away. You take a piece of card much larger than the puzzle, cut out a hole the size and shape of Wally, and place it over the picture — revealing only Wally. The friend can see that you knew, without learning anything about his location.

---

## Why Have zk-Proofs Become Important to Blockchain?

The first implementations of zk-proofs in blockchain were in projects such as Zcash ($ZEC) and later Monero ($XMR). They allowed users to transact on privacy-enabled blockchains using proofs that confirm transactions are valid whilst revealing nothing more.

However, privacy itself isn't the main reason for Vitalik's excitement. Ethereum is not privacy-enabled at the base layer. The big goal is **scalability**.

zk-related tech is the prime candidate to deliver orders of magnitude of scalability to Ethereum (and other Layer 1 chains). But how did we step from privacy tech to scalability?

zk-proofs can be of two types:
- **Interactive** — secure but takes away significant scalability potential. Not widely used in blockchain.
- **Non-interactive** — a single exchange of information suffices. These give the speed of throughput that is exciting and transformational to blockchain projects.

With non-interactive proofs, there is a greater requirement to perform proving calculations. The 'Prover' (and decentralising it) is where most of the engineering challenges are focused.

---

## zk-SNARKs vs. zk-STARKs

Two prominent types of non-interactive zk-proofs are:

**SNARK** — Succinct Non-Interactive ARguments of Knowledge

- **ZK** = Zero-knowledge: only a proof provided, all other transaction info is withheld
- **S** = Succinct: proof size is compact, saving data space, quick to verify
- **N** = Non-interactive: proof generation and verification occurs in a single transaction
- **ARK** = Argument of Knowledge: 'computational soundness' — impossible to cheat without having access to certain verifiable information

Zcash ($ZEC) has used zk-SNARKs since 2016 to offer a shielded blockchain experience.

**STARK** — Scalable Transparent ARgument of Knowledge

- **S** = Scalable: STARKs enable developers to execute computation and store data 'off-chain', increasing scalability exponentially
- **T** = Transparent: STARKs use publicly-available randomness to generate parameters, eliminating the need for a trusted setup
- **ARK** = same computational soundness as SNARKs, but using a different approach with hash functions resistant to collisions

**Key difference — trusted setups:** SNARKs depend on an initial trusted setup between prover and verifier, which creates a centralisation issue. STARKs don't require a trusted setup.

Both approaches allow for fast verification and less block space, meaning more scalability for networks like Ethereum.

---

## zk-Rollups

**zk-Rollups** are zk-based approaches that increase scalability by bundling thousands of transactions in a batch and posting only some minimal summary data to the base layer.

This is where the excitement really lies — not just privacy, but the ability to dramatically increase the number of transactions Ethereum can process per second.

---

## zkEVM — The Latest Development

ZK-rollups are not readily compatible with the Ethereum Virtual Machine (EVM). Proving general-purpose EVM computation in circuits is more difficult than proving simple computations like token transfers.

However, advances have been made in wrapping EVM computation in zero-knowledge proofs. **zkEVM** recreates existing EVM opcodes for proving/verification in circuits, allowing them to execute smart contracts — the best of both worlds.

---

## Key Players in 2022 (for historical reference)

At the time of writing, the main contenders for scaling Ethereum with zkEVM technology were:

1. **StarkNet (Starkware)** — targeting up to 100,000 transactions per second
2. **ZKSync** — aiming for VISA-like scale of thousands of transactions per second; the only zk-rollup protocol claiming full EVM compatibility at the time
3. **Polygon Zero** — focused on reducing computational cost of generating validity proofs; a regular MacBook Air could complete a proof in 0.3 seconds
4. **SCROLL** — building 'in the open' with the Ethereum Foundation's Privacy and Scaling Explorations group

---

## The Vision

Steve Newcomb of ZKSync described the vision like this:

> "I always liken it to when nobody trusted their credit cards on the browser and then we finally agreed on SSL everywhere, we got that lock icon up in the browser window and suddenly people started trusting using their credit cards online. It created e-commerce — it didn't change it, it created the use case. And I think that's going to be the same thing with this [zkEVM rollup tech]."

Beyond zkEVM as a Layer 2 enabler, there is the promise of 'Layer 3' — a layer where anyone can operate an independent blockchain tailored to their specific need, incorporating existing Layer 1s and 2s. This layer of 'fractal hyperchains' is where the promise of massive growth and real-world adoption is inspiring lofty ambitions.

---

*END*

*Note: Some project-specific details (token launches, testnet status) in this post reflect the state of affairs in late 2022.*

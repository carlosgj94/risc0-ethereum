> [!IMPORTANT]
> `main` is the development branch.
> Application developers should use the [latest release](https://github.com/risc0/risc0-ethereum/releases) instead.

# RISC Zero Ethereum

[RISC Zero] is a zero-knowledge verifiable general computing platform, with [Ethereum] integration.
This repository contains [Solidity verifier contracts][contracts], [Relay], [Steel] EVM view call library, and supporting code.

If you are looking to get started using RISC Zero in the application on Ethereum, the best place to look is the [Foundry template][template].

You can also find the documentation for RISC Zero, including guides for [writing zkVM programs][risc0-quickstart], [using the Bonsai prover][bonsai-quickstart], and more at [dev.risczero.com].

## Contracts

RISC Zero's Ethereum contracts, including the on-chain verifier for all RISC Zero Groth16 proofs, can be found in the [contracts] directory.

## Steel

A powerful library for querying and generating verifiable proofs over Ethereum or other EVM-based blockchain state. It leverages [alloy], giving developers a familiar and high quality interface for querying Ethereum via view calls. Steel makes it easy to securely move execution off chain saving gas and unlocking new use cases on Ethereum.


You can install [Steel] with `cargo add risc0-steel`, check out the examples in the [examples directory](./examples/erc20-counter).

## Relay

The Relay is a service that can be run to accept proving requests from on-chain events or via REST Request, and post receipts to the developer's application contract as a callback.
It represents one way of accepting requests, and posting proofs to Ethereum.
It is also possible to write your application without using the Relay.

You can find and overview of how the Relay works, [in our documentation][relay-overview].
Source code for the Relay is in the [relay] directory.

[RISC Zero]: https://github.com/risc0/risc0
[Ethereum]: https://ethereum.org/
[contracts]: ./contracts
[relay]: ./relay
[Steel]: ./steel
[template]: https://github.com/risc0/bonsai-foundry-template
[dev.risczero.com]: https://dev.risczero.com
[risc0-quickstart]: https://dev.risczero.com/api/zkvm/quickstart
[bonsai-quickstart]: https://dev.risczero.com/api/bonsai/quickstart
[relay-overview]: https://dev.risczero.com/api/bonsai/bonsai-on-eth#bonsai-relay
[alloy]: https://github.com/alloy-rs

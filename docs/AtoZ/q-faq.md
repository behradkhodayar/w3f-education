---
id: q-faq
title: Q for FAQ
sidebar_position: 16
---

![J for Polkadot JS](assets/Q.png)

For the past two-plus years that Polkadot has been live, questions from the community are frequently present in socials. In this post, I’ll be answering some of those questions. If you have any other questions that you think should be a part of this post, please leave a comment.

## How does staking work?

Staking on Polkadot uses Nominated Proof-of-Stake(NPoS), a flavor of PoS that allows for two types of participants, nominators and validators. Validators are the entities that run a full version of the Polkadot blockchain as a node, and they secure the network by bonding a number of tokens, which in turn allows them to create blocks. Nominators are the entities that elect validators into the active validator set, which currently is 297 on Polkadot and 1000 on Kusama. 


:::info

The active validator set is an arbitrary value that can be changed via governance.

:::

The role of staking is a part of the consensus mechanism. The mechanism allows token holders to be the on-chain entities that secure the network by putting up their tokens as collateral. This incentive, baked into the protocol, allows any token holder to earn newly created tokens, which the network mints whenever there is a successful new block. In simple terms, this is the inflation portion of the monetary policy of the network.

The reason why its design is complex is due to avoid the pitfalls of staking models. Mainly that of a few entities controlling the majority of the stake. Proof-of-Stake systems all have a different flavor of choosing the staked entities as validators. And the goal here is not to favor certain entities more than others. That endevour in itself is a challenging problem to solve. 

For a detailed dive into NPoS read the [letter N](npos.md) post of this blog series. And also be sure to checkout the [Polkadot wiki](https://wiki.polkadot.network/docs/learn-phragmen).

## What is the Polkadot-JS UI?

[Polkadot-JS](polkadot-js.md) is a developer-centric interface that allows for granular control of Substrate-based chains. The idea with Polkadot-JS is to be a place where all [extrinsics](https://wiki.polkadot.network/docs/learn-extrinsics) of all pallets can be engaged. For a tool like Polkadot-JS to stay up to date with the ever-changing Substrate landscape, functionality is the primary goal, and the user interface has to be a secondary consideration. Therefore, we should consider Polkadot-JS as a featureful tool rather than a user-centric one. For more user-centric tools, try one of the many wallets that support Substrate.

## Why does a parachain need to connect to the Relay Chain?

The Relay Chain provides security for parachains. On a more granular level, it also provides a marketplace for parachains to compete. Via the parachain auctions, this competition can be considered healthy, as it incentivizes good product development and disincentivizes scams. The security of the Relay Chain is inherited by the parachains, making them as secure as the Relay Chain. This is a big improvement to previous models of blockchain development - as previously blockchains would have needed to develop their network security from scratch. 

## How is Polkadot different from Cosmos?

A classic comparison. Polkadot vs. Cosmos has been one of the most debated topics as they are competitors for a chain model that allows other layer 1 chains to connect and interoperate. See [this wiki page](https://wiki.polkadot.network/docs/learn-comparisons-cosmos) for more info about this topic.

## Why do different networks have different addresses but the same pubkey?

Substrate-based chains use the SS58 format for generating their account keypairs. Different network formats are other representations of the same public key in a key pair generated by an address-generation tool. This results in addresses being compatible across networks as long as the format is converted correctly.

## Why is the unbonding period 28 days and why can’t I earn staking rewards when I’m unbonding?

The unbonding feature is designed to ensure that those who stake are not simply able to remove their stake at will, which ensures security in the network. Technically you will earn staking rewards if you unbond in the middle of an era for that era; however, not for the following one. The time you will have to wait until your tokens serves as a cooldown. During this time, you cannot nominate and/or transfer, hence unable to earn staking rewards.

## Is Kusama a testnet?

Kusama was intended to be a value-bearing test network, but since its inception, we have seen it become a sovereign network in its own right. Including a vibrant developer community and culture, as well as projects that live solely in Kusama, with no plans to move on to Polkadot. So why? Because, in the world of blockchains, we are dealing with real value. A bug in runtime code can be extremely costly, and to prevent this, runtime code needs to be tested in real value-bearing environments. In addition to Web 2.0 style testing, Web 3.0 needs to be run in the wild to see if any game-theoretic unpredictable behaviors emerge. Kusama is exactly that for Polkadot and any other parachain that plans to be on Polkadot. But now, it is also home to many projects that have found a home in the world of Kusama.

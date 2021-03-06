---
description: Customize how a Prize Pool distributes prizes
---

# 💸 Prize Strategies

A Prize Strategy handles prize distribution for a [Prize Pool](../prize-pool/).  When a Prize Pool is constructed it is configured with a Prize Strategy.  The Prize Strategy has the privileged ability to award tokens from the Prize Pool.

The first Prize Strategy that PoolTogether is offering is the [Single Random Winner](single-random-winner/) strategy.

Prize Strategies must implement the [Token Listener](../prize-pool/token-listener.md) interface so that they can be aware of the full token lifecycle.

## Privileged Actions

A [Prize Pool's](../prize-pool/) Prize Strategy is able to award tokens held by the Prize Pool contract. The Prize Strategy is able to:

* [award yield](../prize-pool/#awarding-yield) that has accrued in the Prize Pool
* [award any ERC20 balance](../prize-pool/#awarding-erc-20-s) held by the Prize Pool
* [award any ERC721](../prize-pool/#awarding-erc-721-s-nfts) owned by the Prize Pool

## Required Behaviour

A Prize Strategy must implement the [Token Listener](../prize-pool/token-listener.md) interface so that it can listen to pool token mint, transfer and burn actions.


---
layout: default
title: Scaling transaction throughput in blockains  
date:   2021-12-05 21:06:44 -0300
excerpt: "Exploring blockchain scalability solutions across Parallel PoW Blockchains, PoS Protocols, and Layer 2 Protocols. Parallel PoW enhances throughput via multiple blockchains, PoS focuses on stake-based incentives with security concerns, and Layer 2 solutions offer scalability with unique trust models. These methods reflect ongoing efforts to improve blockchain transaction capacity."

---
# Scaling transaction throughput in blockchains

There have been many proposals for scaling transaction throughput in blockchains. In this article we will talk about several types of approaches.

*A. Parallel PoW Blockchains*

Many protocols aim to achieve high transaction throughput by operating several blockchains in parallel in a manner conceptually similar to BlockReduce. The PoW version of Parallel Chains involves mining a metablock containing candidate blocks for a number of parallel chains which operate non-overlapping state partitions. In Particular, Parallel Chains does not support cross-blockchain transactions. Chainweb is another protocol operating many parallel chains, where each block header references the headers of other chains in order to braid the chains together. Chainweb allows crossblockchain state transitions and also features a mechanism by which chains inherit work from one another, but can achieve only a linear increase in transaction throughput with the number of parallel chains whereas BlockReduce is able to achieve superlinear scaling.

*B. Proof-of-Stake Protocols*

Proof-of-stake consensus protocols (PoS) are one of the most promising technology to replace PoW and still preserve similar properties: while PoW provides robustness assuming that a (qualified) majority of the computing power is honest, PoS instead relies on the assumption that a majority of the wealth in the system is controlled by honest participants. Users who have significant stakes in the system have an economic incentive in keeping the system running according to the protocol specification.

Many Proof-of-Stake (PoS) protocols have been proposed and implemented, Ethereum’s planned move to Proof-of-Stake with the goal of achieving a high transaction throughput and a low settlement time. However, Proof-of-Stake protocols currently do not afford the same security guarantees as PoW and suffer from shortcomings such as the known “nothing at stake” problem. This problem can occur anytime there is a fork in the blockchain, either because of a malicious action or accidentally when two honest validators propose block simultaneously. This could potentially make [double-spend-attacks] more feasible.

*C. Layer 2 Protocols*

Layer 2 is another network working above the leading Ethereum network. This solution stay above the layer 1 network through smart contract. Layer 2 can interact with the leading network and not rely on modifications to their base protocols.

There are multiple Layer 2 protocols which have been developed in order to facilitate high transaction throughput. These include Starkware, Polygon, and Lightning among many others. Layer 2 solutions inevitably require alternate trust models from the core blockchain protocol which may not be suited for all use cases. BlockReduce scales as a Layer 1 protocol and does not require an alternate trust model or any additional assumptions to achieve scalability.

### References

- [0] &nbsp M. Fitzi, P. Gazi, A. Kiayias, and A. Russell, “Parallel Chains: Improving Throughput and Latency of Blockchain Protocols via Parallel Composition,” {IACR} Cryptology ePrint Archive, vol. 2018, p. 1119, 018
- [1] &nbsp W. Martino, M. Quaintance, and S. Popejoy, “Chainweb: A proof-of-work parallel-chain architecture for massive throughput,” Chainweb Whitepaper, vol. 19, 2018.
- [2] &nbsp C. Sguanci, R. Spatafora, and A. M. Vergani, “Layer 2 blockchain scaling: a survey,” arXiv preprint arXiv:2107.10881, 2021.

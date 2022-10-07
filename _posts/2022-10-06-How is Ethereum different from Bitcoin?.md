---
topic: ethereum
categories: ethereum
---

> This article is scrapped from "Mastering Ethereum"

Ethereum’s purpose is not primarily to be a digital currency payment network. 

While the digital currency **ether** is intended as a **utility currency** to pay for use of the Ethereum platform as the world computer.

Ethereum is designed to be a **general-purpose programmable blockchain** that runs a virtual machine capable of executing code of arbitrary and unbounded complexity.

Ethereum’s language is **Turing complete**, meaning that Ethereum can straightforwardly function as a general-purpose computer.

The Ethereum platform was designed to abstract detailed implementations of peer-to-peer networks, blockchains, consensus algorithms, etc... providing a deterministic and secure programming environment for decentralized blockchain applications.

While bitcoin keeps track of bitcoin's ownership, ethereum tracks the **state transition** of a general-purpose data store, which is stored in key-value tuple.

Ethereum can load code into its state machine and run that code, storing the resulting state changes in its blockchain.


_**About Turing completeness**_

_Note: Turing machine is a machine composed of memory, head, state and symbols. Head reads memory from left to right, performing jobs pre-determined by symbols, and overwrites the state in it's position._

_If a machine is Turing-complete, it means it can simulate any Turing machine._

_Due to the fact that it can simulate any programs, Turing-complete machines can be stuck in infinite loops or computation that needs huge resoureces. And it is also proven that we cannot predict whether a program will end in finite time or not._

_To solve this problem, Ethereum introduced the concept of **gas**. While running a smart contract, in each operations( computations, data access, etc. ), a pre-defined amount of gas is used. When sending transaction to trigger execution, a user has to set a **gas limit**. If a gas used in execution exceeds the gas limit, the EVM will terminate the execution, leaving the state unchanged._
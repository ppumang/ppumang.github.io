---
category: ethereum
---

**P2P network**   
Ethereum runs on the Ethereum main network, which is addressable on TCP port 30303, and runs a protocol called ÐΞVp2p.

**Consensus rules**   
Ethereum’s consensus rules are defined in the reference specification, the **[Yellow Paper][yellow paper link]**

[yellow paper link]: https://ethereum.github.io/yellowpaper/paper.pdf

**Transactions**  
Ethereum transactions are network messages that include (among other things) a sender, recipient, value, and data payload.

**State machine**  
Ethereum state transitions are processed by the Ethereum Virtual Machine (EVM), a stack-based virtual machine that executes bytecode (machine-language instructions). EVM programs, called "smart contracts," are written in high-level languages (e.g., Solidity) and compiled to bytecode for execution on the EVM.

**Data structures**  
Ethereum’s state is stored locally on each node as a database (usually Google’s LevelDB), which contains the transactions and system state in a serialized hashed data structure called a **Merkle Patricia Tree**.

**Consensus algorithm**  
Ethereum uses Bitcoin’s consensus model, Nakamoto Consensus, which uses sequential single-signature blocks, weighted in importance by PoW to determine the longest chain and therefore the current state. However, there are plans to move to a PoS weighted voting system, codenamed Casper, in the near future.

**Economic security**  
Ethereum currently uses a PoW algorithm called Ethash, but this will eventually be dropped with the move to PoS at some point in the future.

**Clients**  
Ethereum has several interoperable implementations of the client software, the most prominent of which are Go-Ethereum (Geth) and Parity.

_Note: Ethereum finalized '**The Merge**' at block #15,537,393 on September 15, 2022, at 1:42:42 EST. Which means that Ethereum has moved from PoW to PoS. Instead of mining, Ethereum will rely on stakers to secure the network._

> This article is scrapped from "Mastering Ethereum"
---
layout: default
title: Whitepaper Extract 2
parent: Writing
nav_exclude: true
nav_order: 4
---
Whitepaper Extract
{: .label .label-yellow }

## 4. Feature Set

### 4.1. Proof-of-Stake

Solaris operates with a Proof-of-Stake consensus mechanism, meaning that anyone
who can prove they hold XLR can help secure the network, i.e., has a chance to
create the newest block. Unlike masternodes , there is no barrier for entry to start
staking XLR. Staking participants only need to prove that they own a minimum of 1
XLR. This is achieved by having mature coins in your wallet or node, which is
enabled for Staking. Any participant who does this is considered a validator, and the
network of validators then participate in the consensus algorithm.

### 4.2. Masternodes

The purpose of masternodes in the Solaris network is the processing of functions,
thus aiding in the creation of new blocks. Just like Stakers, Masternodes receive part
of the block reward for their participation in the network.
A masternode is a full node or computer wallet that keeps the full copy of the
blockchain in real-time. They are however, quite different in their functionality
compared to normal nodes in that they perform several other functions.
Solaris has implemented the following masternode features in XLR:

- Privacy Increase through the Zerocoin protocol
- Instant Transactions through SwiftTX
- Governance and Voting
- Budgeting and Treasury

Masternodes are not standalone nodes, they are in constant communication with
other masternodes to create the decentralized network that Solaris aimed to create.

#### 4.2.1. Masternode Requirements

There are many ways to set up a masternode, you may choose to run your own
computer, or use a VPS (Virtual Private Server) for example. To run a masternode
there are a few requirements:

- A Fully Synced Wallet
- 1000 XLR which are not spendable while you run a masternode
- A computer or VPS

### 4.3. SwiftTX

SwiftTX transactions are confirmed and spendable within seconds. These funds are
guaranteed by the Solaris network of masternodes. There is no need to wait for
multiple confirmations as is normally expected in order to be confident in the
validity of the transaction.

### 4.4. ZeroCoin Protocol

Zerocoin provides full privacy to our users. Our implementation of the Zerocoin
protocol converts your publicly available transaction details into an anonymous one.
When a user wishes to spend funds, they appear as a new coin without a spending
history or origin.
This protocol uses cryptographically secure techniques to ensure that your coins
cannot be traced. This allows you to transact with your coins freely with strong
mathematical assurances that the transactions are not traceable. These assurances
remain in place even if the network is compromised.

### 4.5. Sporks

A multi-phased fork, or spork is a system previously unique to DASH, which is used
to safely implement new features to the network through network-level variables.
This is to avoid unintended forks during upgrade periods.
Equally, a spork can also be used to disable a feature if a vulnerability is discovered.
New features or versions of Solaris go through rigorous testing before its release to
the main network. When new features, patches or upgrades are to be released on the
main network, a message is sent to all nodes informing them of the change and
requesting them to update their clients.
When the new code is run on a client, it is not activated until a predetermined
percentage of nodes are running the new code. This percentage is set at 70% for
Solaris.
If an error occurs with the new code, the nodes blocks are not rejected, thus avoiding
unintentional forks. Once that percentage consensus is reached and no errors are
found, the new code is activated remotely by multiple members of the development
team by signing a network message with their respective private keys. Code may also
be deactivated by the same method.
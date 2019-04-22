---
layout: default
title: Whitepaper Extract 1
parent: Writing
nav_exclude: true
nav_order: 3
---
Whitepaper Extract
{: .label .label-yellow }

## Authentication & User Data


End users essentially authenticate with their private key for any actions which require a write
to the system such as posting, voting, commenting etc. All user data is associated with their
key. This includes messages associations, vote count, messages payout etc. Of course
payout in the Menlo One Token is also made to the users address.

This key pair authentication design pattern is becoming common place within decentralized
systems, and while we think the pros outweigh the cons, it’s not without its flaws. The clear
advantage to this is the ability to authenticate without relying on an intermediary, the
disadvantage is the end-user losing their private key or their private key being compromised.

A major reason why the ERC20 standard makes sense for for Menlo Token (ONE) is how
easy the token is to transfer. If a user suspects their key has been compromised, they can
transfer their ONE to a fresh account. Many ERC20 compatible wallets also support the easy
creation of an easy to backup mnemonic phrase. If handled responsibly, using a key pair for
authentication makes a lot of sense. Though we recommend developers using Townhall to
include information for their end-users on how to responsibly store and use their keys.

<br>
#### Data Model

Text based messages such as topics and comments follow the InterPlanetary Linked Data
(IPLD) format which is then converted into Concise Binary Object Representation (CBOR) by
IPFS. IPLD allows data on IPFS to treat all content-addressed data structures as subsets of
one big information space, unifying all data models that link data with hashes as instances of
IPLD [104].
```
An example of a message JSON object:
{
"version": <hash>,
"parent": <hash>,
"body": <string>,
"issuer": <pubkey>
}
```

<br>
#### Structure of a TownHall message object model

- Root
- Messages
----Topics
----Comments

<br>
#### Core Features

TownHall comes with the following system features
1. Create Topic
2. Comment on topic
3. Upvote topic
4. Downvote topic
5. Upvote comment
6. Downvote comment

The TownHall interface comes with the following features

- View all messages
- Input box to submit a new message
- Buttons for upvote, downvote
- Button to “get paid for your messages”
- Text which says “this post earned X ONE” by that message




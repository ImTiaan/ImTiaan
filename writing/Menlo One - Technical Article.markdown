---
layout: default
title: Article / Blog
parent: Writing
nav_exclude: true
nav_order: 1
---
Blog / Article
{: .label .label-red }

## Building dApps with JavaScript and Menlo One


Menlo One is a development framework written in Javascript which provides developers with a toolkit for building decentralized applications (dApps) which are hosted on cloud based Content Nodes. You can think of these dApps as “web-dApps”. Traditionally only a small part of the dApp is kept on a blockchain, leaving the rest of the application on a traditional centralized system. Menlo One solves that problem by storing all of the data on several decentralized systems (At launch it works with IPFS and Ethereum), and eliminates a single point of failure by mirroring the server-side applications on many independently operated servers.

<br>
For developers who have been building Single Page Application (SPA) in the Node.js ecosystem, our framework will feel very familiar. A client-side SPA communicates with a server-side Node.JS backend via a RESTFul API, courtesy of Express. Express interacts with an ORM which then communicates with a database. However there are a few paradigm shifts to consider through with this classic model.

<br>
- There is not a single centralized server which the developers maintain. Instead the back-end is hosted by 3rd parties on -their- servers, and users connect to one of them. In the Menlo ecosystem, there are multiple independently operated servers all mirroring the same server-side Node app. We call these “content nodes”.

- Users cannot use a web dApp without running a client app on their desktop, the Menlo Wallet. This app is responsible for the discovering and connecting to servers for the user to connect to. It also contains lite nodes of several blockchain systems, and it is responsible for interacting with the blockchain networks for the user. Lastly this app is responsible for validating data the user receives from the content nodes with the blockchain. A simple API is exposed for developers, and the complexity of the validation protocol is handled for the developer automatically.

- On the server-side, application data is not stored in a single, centralized database. When data is saved to the database, a second call is made to save that data to the blockchain. Servers run an application which handle the protocol for communicating with the blockchain.

- If you’re a developer new to decentralized systems, you might be surprised by the fact that all users coming to your dApp are automatically authenticated but, by default, are anonymous. The user does not log in with a traditional username and password, the user authenticates their identity with a cryptographic key pair. At launch, this is Ethereum, but it will be possible for the user to authenticate with several protocols. If the application requires 2FA or single-click sign on, Menlo comes bundled with an integration to Civic, a private, decentralized identity solution.

<br>
### Framework Components

Menlo One comes bundled with everything you need to get started building a dApp. If you’re familiar with some of the “React / Node hackathon starter kits”, its very much in the same vein. It comes with the following major components:

- A front-end starter kit with React. Though, because Menlo follows a very classic RESTful design pattern, it would be easy to use a different front-end framework or build your own.

- The Menlo Wallet which runs on on the client side.

- A content node docker configuration with Node.js preconfigured with h Express & Mongoose configured to support Typescript to safely handle REST APIs, Mongo as the database to index content distributed in IPFS and an Ethereum node to have the latest metadata living on the block-chain.

- Kovan based deployed contracts the framework automatically uses to get you building on testnet quickly.

- Deployment scripts to easily push your dApp server side solution to a central repository where all content nodes pull from to host applications.

In the spirit of many great frameworks, the goal of Menlo is to give you the skeleton so you can focus on the project itself. While protocol for the dApp to communicate with the blockchain can be complex especially for developers new to blockchain development, we’ve abstracted most of that complexity away so you can focus on building for the user. However there are a few Menlo specific considerations when building your web-dApp.

- When the ORM makes CRUD operations to the database, Menlo middleware can be included so you can specify which data should also be persisted to the blockchain.

- Menlo middleware can be included in Express routes so that the client know’s to validate that data with the blockchain.

- Although all data is saved to a public system, some user data such as private messages has to be kept private. We provide an API to a client side library which encrypts messages at REST.

<br>
### Forward compatible for next generation blockchains

Menlo One is a sort of “second layer” on top of existing blockchain networks. The blockchain space is certain to rapidly evolve in the coming years. While Ethereum is currently king of the smart contract platforms, there are several faster and more efficient competitors currently trying to dethrone it. We’ve designed an API so that the underlying blockchain upon which the app is build can be swapped out without breaking changes, in the same way a properly built ORM is blockchain agnostic.

<br>
#### FAQ: Why decentralize in the first place?

If you’re new to decentralized systems, this might seem like we’ve turned classic web architecture on its head a bit, and we have, but for good reason. The general idea is that we should assume the server is not trustworthy, and the user is afraid the server will give them content different from what the content creator intended. Imagine if your friend makes a blog post entitled “USA Spies on Russia”, but then the Commander in Chief asks the Medium CEO to please change that text to “USA is spied on by Russia”. If not for Menlo One, you would have no way of verifying if that’s what your friend intended you to read. With our framework, you the user would take a hash of the server response and compare that with a hash of the original message your friend left in a smart contract on a blockchain. That way both of you know you received the intended message, or if the content node is has been malicious.

<br>
#### FAQ: Who will pay for the cost of hosting content nodes and the users blockchain GAS?

In short there are three actors to consider in this ecosystem: The publisher (someone publishing some sort of data or content), the content node (someone hosting that data), and the user (someone consuming that content). In the Menlo One framework the publisher buys or earns Menlo’s ONE tokens, and when posting their message somewhere puts some ONE tokens in a smart contract. ONE is used to pay the content node for serving you the intended data. ONE is also used to reimburse the user for the inherent cost of using the Ethereum network.

<br>
Furthermore, the user could be paid far more than the cost of GAS if the user is someone the publisher things is high value. For instance if the publisher was a car salesmen on a decentralized Auto Trader, and the user has recently purchased several Lamborghinis, the publisher could incentivize the user for his valuable attention. Assuming all of the customers auto purchases were on the blockchain (and they will be one day soon), this is one of the first times in history that a salesperson can qualify a customer before a transaction.

<br>
In this sense, we cut out the middlemen. Until now most online marketplaces are in the fortunate position of being an intermediary of a transaction and taking a fee. However with Menlo One (and many rapidly growing blockchain networks), it would be possible to build a version of Uber where the driver gets to set his own price, and he does not have to give a percent to Uber.

<br>
The first version of Menlo One is designed around monetizing “attention”, (which is to say, pays the user for validating data received from a content node). However in later versions we will build an API for customizing the publishers deployed smart contract so that a payout to the user occurs with another event, such as a purchase transaction.

<br>
#### FAQ: If the middleman can no longer make money, why would anyone build an app?

It seems there is an economic shift taking place. It’s no longer lucrative to build a *venue* for exchange, but instead a *medium* of exchange. We recommend you explore launching your own cryptocurrency, which is specifically suited for your use case.

<br>
#### FAQ: Do I have to use the ONE token for all transactions?
The ONE tokens is only used to pay for the transaction of data as a way of paying people running content nodes. You the developer are free to build your dApp as you please. The cost of running content nodes can be passed on to users, content creators or your dApp could pay for that cost depending on your scenarios.

<br>
It would be entirely possible to build a decentralized version of Uber where the checkout process goes through a smart contract you control which takes a percent of the transaction. We’re intending our framework be used by many projects who are launching their own cryptocurrency. From the users perspective Menlo One is designed to work behind the scenes. You could make your Uber-like “CarToken” dApp with an interface build with Menlo, which predominantly features your token, but with Menlo working behind the scenes. In later versions we plan on integrating with a decentralized exchanges so users could even easily exchange their earned ONE tokens for another ERC20.
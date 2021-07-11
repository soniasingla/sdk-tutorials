---
parent:
  title: How to access the frontend with Starport
order: 0
description: Learn how to access the frontend wallet using Starport
---

# Introduction

One of the major features about Starport is an automatic generation of client-side code. It creates clients in JavaScript, TypeScript, and Vuex. These clients support querying the blockchain by making requests to gRPC HTTP gateway and broadcasting transactions with messages encoded using protobuf.
Learn how to build front ends that interact with Cosmos SDK applications. This will build a front end that will query and interact with the running blockchain.

One of the best benefit of client side code generation is that every blockchain which use Starport in development will always get up to date clients automatically generated.

In this tutorial, you will learn about:

* Create a blockchain with Starport
* Build Frontend using Starport that interact with Cosmos SDK application
* Build a decentralized Blockchain app with required functions
* <todo>

## Requirements

This tutorial requires [Starport](https://docs.starport.network/) v0.17.1.

**Important** The tutorial is based on this specific version of Starport and is not supported for other versions.{synopsis}

The Starport tool is the easiest way to build a blockchain and accelerates chain development.

To install `starport` into `/usr/local/bin`, run the following command:

```sh
curl https://get.starport.network/starport@v0.17.1! | bash
```

When the installation succeeds, you see this message:

```
Installed at /usr/local/bin/starport
```

You can use Starport in a [browser-based IDE](http://gitpod.io/#https://github.com/tendermint/starport/tree/v0.17.1), but this tutorial assumes you are using a local Starport installation. See [Install Starport](https://docs.starport.network/intro/install.html).

## Create the Blockchain

To scaffold a new blockchain named `model`, use the following command:

```
starport app github.com/<your-github-username>/model
```

A new directory named `model` is created in your home directory and contains a working blockchain app.

## Launch the Blockchain App

To launch the app from the `model` project directory, run the command:

```
cd model
starport serve
```

The `serve` command basically installs dependencies, initializes and runs the application.

The following output is returned, along with any errors that might show up in your application. Two default users and their mnemonic pass phrases are created.

```
Cosmos SDK's version is: Stargate v0.40.0 (or above)

🛠️  Building proto...
📦 Installing dependencies...
🛠️  Building the app...
💿 Initializing the app...
🙂 Created account "alice" with address "cosmos1qn662mssj0wtagnxyvld7pksjaghzvmsw889t7" with mnemonic: "anger drive runway keen enroll shoot frequent dentist captain neither wire person entry exact income sail divorce fresh initial feel boss mule target fly"
🙂 Created account "bob" with address "cosmos1jfx0jqeamwj6dnzhk5g64l53ydcmrsmdm6hlcw" with mnemonic: "yard layer vacuum side coyote cousin another settle agree thunder lumber before portion embody hood practice captain axis fish zero mother bitter example ski"
🌍 Running a Cosmos 'voter' app with Tendermint at http://localhost:26657.
🌍 Running a server at http://localhost:1317 (LCD)
🌍 Running a faucet at http://:4500

🚀 Get started: http://localhost:12345
```

**Congratulations!** You successfully created and launched a blockchain application.

## Sign in as Alice

On the front-end app, sign in as end user Alice. The mnemonic passphrases for Alice and Bob were printed in the console after you ran the `starport serve` command.

After you are signed in as Alice, you can import an existing wallet that was created with the app. The wallet in the model app can handle multiple accounts, so give your wallet a descriptive name. Using a descriptive wallet name helps you recognize this wallet in future transactions. For this example, naming this wallet `model` makes sense.

1. Click **Access Wallet** and then click **Import existing wallet**.
2. Enter the passphrase for Alice that was output to your console when you launched the voter app with the `starport serve` command.
3. Name your wallet `model` and enter a password.
4. Click **Done**.

## 

## Feedback

Do you see any bug, typo in the tutorial or you have some feedback for us? Let us know on [Github](https://github.com/cosmos/sdk-tutorials/issues/new/) or [#🔨cosmos-sdk-starport](https://discord.com/channels/669268347736686612/737461683588431924) channel in Discord.

---
layout: ~/layouts/DocumentationLayout
---

# Secret Contract Devs


Developers can write Secret Contracts for CosmWasm running inside secure enclaves with encryption capabilities. Once the network upgrade integrating Secret Contract functionality has been completed, developers will be able to use private data in contracts running on the live Secret Network. Currently, we have a [contract development guide for developers](/developers/secret-contract-devs/secret-contract-dev-guide) that demonstrates how to get the Secret Network up and running on a local deployment using Docker, as well as how to write simple contracts in Rust using CosmWasm.

# Getting Started
-------------------------------------

###  1. Start a Node Locally

####  1.1 Make sure to [install SGX](/developers/node-operators/validators/setup-sgx)

####  1.2 Download the [secret node package](/developers/testnet/testnet-docs) and follow the instructions

###  2. Get Your Testnet Account

####  2.1 Create a [local scrt address](/developers/node-operators/secret-light-client)

####  2.2 Get some test SCRT from the [faucet](https://faucet.testnet.enigma.co)

###  3. Start a [Node on Testnet](/developers/testnet/validators-cli/run-a-full-node)

####  3.1 Make sure you can access the IP and DNS address you created

####  3.2 Try to add it as a validator

####  3.3 Use this node as the gateway node you use to deploy your contracts

###  4. Create a Development Environment

checkout the tag v0.5.0-alpha2

```
make cli
docker run -p 26657:26657 enigmampc/secret-network-bootstrap-sw:latest

```

####  4.1 make sure the node is listening on port 26657

####  4.2 make sure cli works when using --node <node\_ip>:26657

###  5. Write a Secret Contract

###  [CosmWasm GitHub Repository](https://github.com/CosmWasm/cosmwasm) \- [Template](https://github.com/CosmWasm/cosmwasm-template)

####  5.1 Deploy it to your local dev environment

####  5.2 Call it using the secretcli

####  5.3 Deploy it to the testnet

####  5.4 Check how the deployment transaction looks on the explorer

####  5.5 Test your function on the testnet

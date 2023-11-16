# Solana-Bootcamp-Final-Project

## Overview
The Solana-Bootcamp-Final-Project is a decentralized application (DApp) on the Solana blockchain that enables the creation, transfer, and burning of Non-Fungible Tokens (NFTs). This contract is implemented using the Custom Interface Definition Language (CIDL) to provide a standardized and structured interface for interacting with NFTs.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
  - [Minting NFTs](#Minting-NFTs)
  - [Transferring NFTs](#Transferring-NFTs)
  - [Burning NFTs](#Burning-NFTs)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Build the contract](#build-the-contract)
- [Set your config file](#Set-your-config-file)
- [Get devnet tokens](#Get-devnet-tokens)
- [Deploy the Contract](#Deploy-the-Contract)
- [Interacting with the contract](#Interacting-with-the-contract)
- [Install Dependencies](#Install-Dependencies)
- [Usage](#Usage)
- [Important Notes](#ImportantNotes)
- [License](#License)

## Features
### Minting NFTs
Users can mint new NFTs by specifying metadata, including color, rarity, and a short description. Each minted NFT is assigned a unique identifier (mint address).

### Transferring NFTs
NFTs can be securely transferred from one user to another. Ownership changes are reflected in the associated token accounts.

### Burning NFTs
Users have the option to burn (destroy) NFTs, reducing the total supply. After burning, the associated metadata is updated, and the association account is set to undefined.

## Getting started

### Prerequisites
Before you begin, ensure you have met the following requirements:
- Node.js and npm installed on your development machine.
- Solana Command Line Tools (solana) installed
- A Solana wallet with SOL tokens for deployment and interactions

### Installation
Clone the Repository:
```bash
https://github.com/Ezeah/Solana-Bootcamp-Final-Project
```

## Build the contract
Open a terminal window from the terminal tab above and navigate to the generated directory using the command:
```bash
cd program
```

Type and run the command:
```bash
cargo build-sbf
```

## Set your config file
If there are no errors, type the command:
```bash
solana config set --url devnet
```

## Get devnet tokens
You get devnet tokens using the command:
```bash
solana airdrop 1
```
check your balance with command:
```bash
solana balance
```

## Deploy the Contract
Once we have the build, from the generated directory, type the following command for deployment: 
```bash
solana program deploy target/deploy/nft.so
``` 

After completing the deployment, you will get a program ID. 
Copy and save the program ID so we can use it to configure the client library.

## Interacting with the contract
To run interact with this contract please, install the required dependencies and to do so type and enter the command:
```bash
cd program_client
```

## Install Dependencies
Type and enter the command: 
```bash
yarn install
```
Then install SPL Token Library by typing and entering the command:
```bash
yarn add @solana/spl-token
```

Run
```bash
app.ts
```

Since we have our frontend test and contract, we can test our NFT contract. 
- To do this, execute the client by typing the following command:
```bash
npx ts-node app.ts <YOUR_PROGRAM_ID>
```

## Usage
Update the contract address in your application to interact with the deployed smart contract.

## Important Notes
- Ensure your Solana wallet is configured with the necessary SOL tokens.
- Ensure the secure handling of wallet authentication and keep private keys confidential.
- Verify the contract address and associated accounts before performing transactions.

## License
This project is licensed under the Unlicense. See the LICENSE file for details.
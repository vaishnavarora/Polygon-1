# Polygon-1

This is my NFT project, where my duties included mapping an NFT collection to Polygon, transferring assets across using the Polygon Bridge, and deploying the collection on the Ethereum blockchain.

## Installation
To get started with the project, follow these steps:

1. clone this repository :
    `git clone https://github.com/vaishnavarora/Polygon-1.git`
   
2. Install the required dependencies :
     `npm install`

## ERC721 Contract Deployment
Before deploying, add private key to your wallet here in "PRIVATE_KEY= 'your wallet private key'". 
Run the following command to deploy the ERC721 contract to the Goerli Ethereum Testnet:

`npx hardhat run scripts/deploy.js --network goerli`


It will generate the address after the contract is deployed. Thus, copy that address and put it into the files contractAddress.js (stored in the metadata folder), approvedDeposit.js (stored in the scripts folder), and batchMint.js.

## Minting the NFTs
Run the following command to batch-mint NFTs using the deployed ERC721 contract:

`npx hardhat run scripts/batchMint.js --network goerli`

## Approve and Deposit NFTs to Polygon Mumbai
Run the following commands to approve and deposit the minted NFTs from Ethereum to the Polygon Mumbai network using the FxPortal Bridge:

`npx hardhat run scripts/approveDeposit.js --network goerli`
## Authors
Vaishnav Arora

## LICENSE
This project is licensed under the [MIT License](LICENSE).

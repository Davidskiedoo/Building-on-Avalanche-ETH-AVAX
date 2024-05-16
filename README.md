# Building-on-Avalanche-ETH-AVAX
Overview

The DegenToken smart contract enables a game platform to manage a custom ERC20 token with functionalities for minting, transferring, redeeming, burning, and checking balances. It also includes a mechanism for players to redeem their tokens for in-game items with predefined prices. The contract is secured by restricting certain actions to the contract owner. And this contract is designed to be deployed on the Avalanche network, leveraging its compatibility with Ethereum smart contracts and low transaction fees. Ensure you have the necessary development environment set up to interact with the Avalanche network.

## Requirements
* Solidity version 0.8.20
* OpenZeppelin contracts for ERC20 and Ownable functionalities
* Avalanche-compatible development tools (e.g., Avalanche C-Chain, Remix, Truffle, Hardhat)
* MetaMask or other web3 wallets configured for the Avalanche network


## Usage
Minting New Tokens
* Only the owner of the contract can mint new tokens. This can be used to reward players within the game.

Transferring Tokens
Players can transfer their tokens to others using the transferDGN function.

Redeeming Tokens
Players can redeem their tokens for items in the in-game store. Each item has a predefined price.

Burning Tokens
Players can burn tokens they own that are no longer needed.

Checking Token Balance
Players can check their token balance at any time.

Viewing Shop Items
Players can view the items available for redemption in the shop.

## Deployment
* Configure your development environment for the Avalanche network.
* Compile the contract using your preferred tool (e.g., Remix, Hardhat).
* Deploy the contract to the Avalanche C-Chain.
* Verify the contract on a block explorer (e.g., SnowTrace).

## Authors
David Joshua B. Bucol

## License
This project is licensed under the MIT License - see the LICENSE.md file for details

# Building-on-Avalanche-ETH-AVAX
Overview

The DegenToken smart contract enables a game platform to manage a custom ERC20 token with functionalities for minting, transferring tokens and rewards, redeeming rewards, burning, and checking balances. It also includes a mechanism for players to redeem their tokens for in-game items with predefined prices. The contract is secured by restricting certain actions to the contract owner. And this contract is designed to be deployed on the Avalanche network, leveraging its compatibility with Ethereum smart contracts and low transaction fees. Ensure you have the necessary development environment set up to interact with the Avalanche network.

## Requirements
* Solidity version 0.8.25
* OpenZeppelin contracts for ERC20 and Ownable functionalities
* Avalanche-compatible development tools (e.g., Avalanche C-Chain, Remix, Truffle, Hardhat)
* MetaMask or other web3 wallets configured for the Avalanche network

## Features
- **ERC20 Compliance**: Implements the ERC20 standard for fungible tokens.
- **Minting**: Allows the owner to mint new tokens up to a specified limit.
- **Burning**: Allows token holders to burn their own tokens.
- **Transfer**: Facilitates the transfer of tokens between addresses.
- **Redeemable Items**: Supports the redemption of specific items using tokens.
- **Check Redeemed Items**: You are able to check your redeemed items.
- **Transfer Redeemed Items** You can send your redeemed items from another player.
- **Ownership Control**: Includes an `onlyOwner` modifier to restrict certain functions to the contract owner.

 ## Functions
- `constructor(string memory name, string memory symbol)`: Initializes the token with a name and symbol.
- `mint(address account, uint256 amount)`: Mints new tokens and assigns them to the specified account.
- `burnToken(address account, uint256 amount)`: Burns a specified amount of tokens from the given account.
- `transfer(address recipient, uint256 amount)`: Transfers tokens from the sender's account to the recipient's account.
- `transferRewards(address to, uint256 itemId)`: Transfers redeemed items to another address.
- `redeem(uint256 itemId)`: Allows users to redeem items using their tokens.
- `viewRedeemedItems(address account, uint256 itemId)`: Retrieves the number of redeemed items for a specific account and item.

## Deployment
* Configure your development environment for the Avalanche network.
* Compile the contract using your preferred tool (e.g., Remix, Hardhat).
* Deploy the contract to the Avalanche C-Chain.
* Verify the contract on a block explorer (e.g., SnowTrace).

## Authors
David Joshua B. Bucol

## License
This project is licensed under the MIT License - see the LICENSE.md file for details

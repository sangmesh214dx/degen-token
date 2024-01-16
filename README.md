# DegenToken 

## Overview

The DegenToken smart contract is an Ethereum-based ERC-20 token with additional functionalities for minting, burning, transferring, and redeeming tokens. It also incorporates a mechanism for managing rates and extents associated with different "bitcoins."

## Features

1. **ERC-20 Token**: DegenToken is an ERC-20 compliant token with the symbol "DGN" and the name "DEGEN."

2. **Ownable Contract**: The smart contract is owned by a single address, providing exclusive privileges to the owner for certain operations.

3. **Minting and Burning**: The owner can mint new tokens and burn existing ones. Minting is done through the `mint` function, and burning is achieved using the `burn` function.

4. **Transferring Tokens**: Token holders can transfer tokens to other addresses using the standard ERC-20 transfer mechanism implemented in the `transfer_` function.

5. **Bitcoin Management**: The contract allows the owner to set rates and extents for different "bitcoins." The rates represent the conversion rate of DegenToken to a specific bitcoin, and extents indicate the quantity available for redemption.

6. **Redeeming Bitcoins**: Token holders can redeem their DegenTokens for a specific bitcoin by providing the bitcoin's name and the desired extent. The redemption process is governed by the `redeemBitcoin` function.

7. **Update Bitcoin Rates**: The owner has the ability to update the conversion rates for different bitcoins through the `updateBitcoinRate` function.

8. **Event Logging**: The contract emits events such as `LogMessage` to provide transparency and keep track of important contract actions.

## Usage

### Deployment

Deploy the DegenToken contract on the Ethereum blockchain. The contract constructor sets the name to "DEGEN" and the symbol to "DGN."

### Owner Operations

The owner can perform the following operations:

- Mint new tokens: `mint(address recipient, uint256 totalTokens)`
- Burn existing tokens: `burn(uint256 totalTokens)`
- Update bitcoin conversion rates: `updateBitcoinRate(string memory bitcoinName, uint256 newRate)`
- Set bitcoin rates and extents: `setBitcoinRatesAndExtents(string memory bitcoinName, uint256 rate, uint256 extent)`

### User Operations

Token holders can:

- Transfer tokens: `transfer_(address recipient, uint256 totalTokens)`
- Redeem bitcoins: `redeemBitcoin(string memory bitcoinName, uint256 extent)`

## Requirements

- **Solidity Compiler**: The code is intended to be compiled using Solidity version 0.8.0.
- **OpenZeppelin Contracts**: The contract relies on the OpenZeppelin ERC-20, Ownable, and ERC-20 Burnable contracts. Ensure that the necessary dependencies are installed.

## Author 

Sangmeshm42@gmail.com

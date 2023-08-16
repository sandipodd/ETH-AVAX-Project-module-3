# Token System Contract

A basic Ethereum token system contract with minting, transferring, and burning functionality.

## Functionality

- Only the contract owner can mint tokens.
- Any user can transfer tokens.
- Any user can burn tokens.

## About

This Ethereum smart contract, written in Solidity, provides a simple token system where the owner can mint tokens, users can transfer tokens, and users can burn tokens.

## License

This project is licensed under the [MIT License](LICENSE).

## Installation and Usage

1. Install a compatible Ethereum development environment (e.g., Remix, Truffle, etc.).

2. Deploy the `TokenSystem.sol` contract to an Ethereum network.

3. Interact with the contract using the provided functions:
   - `createTokens(address _receiver, uint256 _amount)`: Mint tokens and assign them to the specified address (only contract owner).
   - `transferTokens(address _to, uint256 _amount)`: Transfer tokens from the sender's balance to a specified address.
   - `burnTokens(uint256 _amount)`: Burn a specified amount of tokens from the sender's balance.
   - `getTokenBalance(address _account)`: Retrieve the token balance of a specified account.

## Usage Example

```solidity
// Deploy the contract and get its address
TokenSystem tokenContract = TokenSystem(paste_contract_address_here);

// Mint tokens (only contract owner)
tokenContract.createTokens(userAddress, amount);

// Transfer tokens
tokenContract.transferTokens(receiverAddress, amount);

// Burn tokens
tokenContract.burnTokens(amount);

// Get token balance
uint256 balance = tokenContract.getTokenBalance(userAddress);



**Mod3** is a custom ERC20 token implemented using Solidity. This smart contract leverages OpenZeppelin's libraries to provide standard token functionalities along with additional features for controlled minting and burning of tokens.

## Features

- **ERC20 Standard Compliance:** Inherits from OpenZeppelin’s ERC20 contract.
- **Ownership Control:** Only the contract owner can mint new tokens.
- **Token Burning:** Users can burn their own tokens.


## Functions

### Constructor

```solidity
constructor(uint256 initialSupply, uint8 decimals, string memory name, string memory symbol)
```
- Initializes the token with a specified `initialSupply`, `decimals`, `name`, and `symbol`.
- Mints the initial supply to the contract creator’s address.

### Minting

```solidity
function minting(address to, uint256 amount) public onlyOwner
```
- Allows the contract owner to mint new tokens.
- Parameters:
  - `to`: The address to receive the minted tokens.
  - `amount`: The number of tokens to mint.

### Burning

```solidity
function burning(uint256 amount) public
```
- Allows any user to burn their tokens.
- Parameters:
  - `amount`: The number of tokens to burn.

### Transfer

```solidity
function transfer(address recipient, uint256 amount) public override returns (bool)
```
- Overrides the `transfer` function from the `ERC20` contract.
- Parameters:
  - `recipient`: The address to receive the tokens.
  - `amount`: The number of tokens to transfer.

## Getting Started

1. Open the contract in Remix IDE and deploy it to your preferred Ethereum network.

### Usage

1. **Minting Tokens**: Only the owner can call the `minting` function to create new tokens.
2. **Burning Tokens**: Any user can call the `burning` function to destroy their tokens.
3. **Transferring Tokens**: Use the `transfer` function to send tokens to another address.



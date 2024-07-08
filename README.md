# Token Management Smart Contract for Efficient Minting and Burning

## Description

This project involves developing an Ethereum smart contract that manages a token called "NewTokenName" with the symbol "NTN". Written in Solidity, this contract facilitates the easy minting and burning of tokens, providing a simple yet efficient way to manage token supply.

## Features

- **Token Management:** Mint and burn tokens with ease.
- **Public Variables:** Track token details and balances.
- **Efficient Supply Control:** Adjust the total supply dynamically through minting and burning operations.

## Public Variables

- `tokenName`: Stores the name of the token.
- `tokenSymbol`: Stores the abbreviation of the token, set to "NTN".
- `totalSupply`: Tracks the total number of tokens in circulation, initially set to 0.
- `balances`: A mapping that associates addresses with their respective token balances, using an address as the key and a `uint` as the value to store the balance.

## Functions

### Mint Function

The `mint` function is used to generate new tokens and assign them to a specified address. It accepts two parameters:

- `account`: The address to which the new tokens will be allocated.
- `amount`: The number of tokens to be created and added to the total supply.

**Example:** Initially, if you have 0 tokens in your account and want to add 100 tokens, this function will be called to increase the amount. It will also update the balance of the specified address.

```solidity
function mint(address account, uint amount) public {
    totalSupply += amount;
    balances[account] += amount;
}
```

### Burn Function

The `burn` function is used to destroy tokens from a specified address, decreasing both the total supply and the balance of the address. It accepts two parameters:

- `account`: The address from which the tokens will be burned.
- `amount`: The number of tokens to be burned.

**Example:** Initially, if you have 100 tokens in your account and want to burn 10 tokens, this function will be called to reduce the amount. It will also update the balance of the specified address.

```solidity
function burn(address account, uint amount) public {
    require(balances[account] >= amount, "Balance is not sufficient to burn the requested amount");
    totalSupply -= amount;
    balances[account] -= amount;
}
```

## Usage

To use this smart contract, deploy it on the Ethereum blockchain. Once deployed, you can call the `mint` and `burn` functions to manage the token supply.

### Minting Tokens

To mint new tokens, call the `mint` function with the address to which the tokens should be allocated and the number of tokens to be created.

```solidity
mint(0xYourAddress, 100);
```

### Burning Tokens

To burn tokens, call the `burn` function with the address from which the tokens should be burned and the number of tokens to be destroyed.

```solidity
burn(0xYourAddress, 10);
```

## Conclusion

This smart contract provides a simple and efficient way to manage token supply through minting and burning operations. With clearly defined public variables and straightforward functions, it offers an easy-to-use solution for token management on the Ethereum blockchain.

## Smart Contract Code

```solidity
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public tokenName = "NewTokenName"; 
    string public tokenSymbol = "NTN"; 
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address account, uint amount) public {
        totalSupply += amount;
        balances[account] += amount;
    }

    // burn function
    function burn(address account, uint amount) public {
        require(balances[account] >= amount, "Balance is not sufficient to burn the requested amount");
        totalSupply -= amount;
        balances[account] -= amount;
    }
}
```

This smart contract offers a robust foundation for managing a token with minting and burning functionalities, ensuring a dynamic and controllable token supply on the Ethereum blockchain.

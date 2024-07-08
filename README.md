# Metacrafter_Eth_project
**PROJECT TITLE:** Token Management Smart Contract for Efficient Minting and Burning

**DESCRIPTION:** This project entails developing an Ethereum smart contract that manages a token called "NewTokenName" with the symbol "NTK". Written in Solidity, this contract facilitates the easy minting and burning of tokens.

**PUBLIC VARIABLES:**

- `tokenName`: Stores the name of the token.
- `tokenSymbol`: Stores the abbreviation of the token, set to "NTK".
- `totalSupply`: Tracks the total number of tokens in circulation, initially set to 0.
- `balances`: A mapping that associates addresses with their respective token balances, using an address as the key and a `uint` as the value to store the balance.

**MINT FUNCTION:** The `mintToken` function is used to generate new tokens and assign them to a specified address. It accepts two parameters:

- `add`: The address to which the new tokens will be allocated.
- `value`: The number of tokens to be created and added to the total supply.

**Example:** Initially, if you have 0 tokens in your account and want to add 100 tokens, this function will be called to increase the amount. It will also update the balance of the specified address.

**BURN FUNCTION:** The `burnToken` function is used to destroy tokens from a specified address, decreasing both the total supply and the balance of the address. It also accepts two parameters:

- `add`: The address from which the tokens will be burned.
- `value`: The number of tokens to be burned.

**Example:** Initially, if you have 100 tokens in your account and want to burn 10 tokens, this function will be called to reduce the amount. It will also update the balance of the specified address.

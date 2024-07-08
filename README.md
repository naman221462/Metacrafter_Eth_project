# Metacrafter_Eth_project
PROJECT TITLE: Token Management Smart Contract for Efficient Minting and Burning

DESCRIPTION: This project involves the creation of an Ethereum smart contract that manages a token called "NewTokenName", consisting of the symbol "NTK". This smart contract, written in Solidity, makes it easy to mint and burn tokens.

PUBLIC VARIABLES:

tokenName: Stores the name of the token.
tokenSymbol: Stores the abbreviation of the token, set to "NTK".
totalSupply: Keeps track of the total number of tokens in circulation. Initially set to 0.
MAPPING balances: A mapping that links addresses to their respective token balances, using an address as the key and a uint as the value to store the balance.

MINT FUNCTION: The mintToken function is used to create new tokens and assign them to a specified address. It takes two parameters:

add: The address to which the new tokens will be assigned.
value: The number of tokens to be created and added to the total supply.
Example:Suppose intially you have 0 rupee in your account and you want to add 100 rupees then compiler call this mint function to add the amount. It also update the address of balance.

BURN FUNCTION: The burnToken function is used to destroy tokens from a specified address, reducing both the total supply and the balance of the address. It also takes two parameters:

add: The address from which the tokens will be burned.
value: The number of tokens to be burned.
Example:Suppose intially you have 100 rupee in your account and you want to burn 10 rupees then compiler call this burn function and substract from the amount. It also update the address of balance.

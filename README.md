# MercedesToken
Overview
MercedesToken is a simple Solidity smart contract that implements a basic ERC20-like token. The contract allows for minting and burning of tokens and keeps track of balances for each address. This project is intended to demonstrate the fundamentals of Solidity and smart contract development.
Contract Details
Token Name: Mercedes
Token Abbreviation: Merc
Total Supply: Dynamic, starting at 0 and changing with minting and burning actions.
Features
Public Variables:

tokenName: The name of the token.
tokenAbbrv: The abbreviation of the token.
totalSupply: The total supply of tokens.
Mapping:

balances: A mapping from addresses to their respective balances.
Mint Function:

Increases the total supply by a specified value.
Increases the balance of a specified address by the same value.
Burn Function:

Decreases the total supply by a specified value.
Decreases the balance of a specified address by the same value, provided the address has a sufficient balance.

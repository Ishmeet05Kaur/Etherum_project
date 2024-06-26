# MercedesToken
## Overview
MercedesToken is a simple Solidity smart contract that implements a basic ERC20-like token. The contract allows for minting and burning of tokens and keeps track of balances for each address. This project is intended to demonstrate the fundamentals of Solidity and smart contract development.
## Contract Details
1. Token Name: Mercedes
2. Token Abbreviation: Merc
3. Total Supply: Dynamic, starting at 0 and changing with minting and burning actions.
## Features
1. Public Variables:
   1. tokenName: The name of the token.
   2. tokenAbbrv: The abbreviation of the token.
   3. totalSupply: The total supply of tokens.
   
3. Mapping:
   1. balances: A mapping from addresses to their respective balances.
   
5. Mint Function:
   1. Increases the total supply by a specified value.
   2. Increases the balance of a specified address by the same value.
   
7. Burn Function:
   1. Decreases the total supply by a specified value.
   2. Decreases the balance of a specified address by the same value, provided the address has a sufficient balance.
## Functions
mint
```javascript
function mint(address m_address, uint m_value) public
```
Description:
Increases the total supply of tokens and the balance of the specified address.

Parameters:

m_address: The address to which the tokens will be minted.
m_value: The number of tokens to mint.
Usage:
```javascript
mint(0xYourAddressHere, 100);
```
burn
```javascript
function burn(address m_address, uint m_value) public
```
Description:
Decreases the total supply of tokens and the balance of the specified address, ensuring the address has a sufficient balance to burn.

Parameters:

m_address: The address from which the tokens will be burned.
m_value: The number of tokens to burn.
Usage:
```javascript
burn(0xYourAddressHere, 50);
```
## Usage Example
Here is a simple example of how to interact with the MercedesToken contract:
```javascript
// Deploy the contract
MercedesToken token = new MercedesToken();

// Mint 100 tokens to an address
token.mint(0xYourAddressHere, 100);

// Check the balance
uint balance = token.balances(0xYourAddressHere); // Should be 100

// Burn 50 tokens from the same address
token.burn(0xYourAddressHere, 50);

// Check the balance again
balance = token.balances(0xYourAddressHere); // Should be 50
```





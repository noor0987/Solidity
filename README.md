# NoorBegContract

## Overview

`NoorBegContract` is a simple ERC20-like token smart contract built on the Ethereum blockchain. This contract defines a token named "Kanwalnoor kaur" with the abbreviation "KK" and an initial total supply of 310 tokens. The contract allows minting and burning of tokens, enabling the total supply and individual balances to be dynamically managed.

## Features

- **Token Information**: The contract provides basic information about the token, including its name and abbreviation.
- **Minting**: Allows the creation of new tokens and increases the total supply.
- **Burning**: Allows the destruction of tokens, decreasing the total supply.

## Contract Details

### State Variables

- `tokenName`: The name of the token. (public)
- `tokenAbbr`: The abbreviation of the token. (public)
- `totalSupply`: The total supply of tokens. (public)
- `balances`: A mapping that tracks the token balance of each address. (public)

### Functions

#### mint

```solidity
function mint(address addr, uint amount) external
```

- **Description**: Mints new tokens and assigns them to the specified address, increasing the total supply.
- **Parameters**:
  - `addr`: The address to which the minted tokens will be assigned.
  - `amount`: The number of tokens to mint.
- **Visibility**: `external`

#### burn

```solidity
function burn(address addr, uint amount) external
```

- **Description**: Burns tokens from the specified address, decreasing the total supply.
- **Parameters**:
  - `addr`: The address from which the tokens will be burned.
  - `amount`: The number of tokens to burn.
- **Visibility**: `external`
- **Condition**: The function checks if the address has enough balance to burn and if the total supply is greater than the amount to be burned.

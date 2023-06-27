# MyToken

This is a basic implementation of a Solidity contract for an ERC-20 token. The contract enables the generation and removal of tokens while also providing a means to store relevant token information.

## Requirements

1. The contract includes publicly accessible variables that hold information regarding the coin's specifications:
   - `tokenName`: A string variable that represents the name of the token.
   - `abbrv`: A string variable that represents the abbreviation of the token.
   - `totalSupply`: An unsigned integer that represents the total supply of the token.

2. The contract has a mapping of addresses to balances:
   - `balances`: A mapping that associates addresses with their corresponding token balances.

3. Within the contract, there exists a 'mint' function that allows for the increment of the total supply and the balance associated with the "sender" address by a specified value.
   - Parameters:
     - `_address`: The address to which the tokens will be created.
     - `_value`: The amount of tokens to be created.
   - Actions:
     - Increase the `totalSupply` by `_value`.
     - Increase the balance of the `_address` by `_value`.

4. The contract has a `burn` function that decreases the total supply and the balance of the "sender" address by a given value:
   - Parameters:
     - `_address`: The address from which the tokens will be burned.
     - `_value`: The amount of tokens to be burned.
   - Actions:
     - Check if the balance of the `_address` is greater than or equal to `_value`.
     - If true, decrease the `totalSupply` by `_value`.
     - Decrease the balance of the `_address` by `_value`.

## Usage

1. Deploy the `MyToken` contract to a supported Ethereum network.

2. Once deployed, you can interact with the contract by calling the following functions:

   - `mint`: Creates new tokens and assigns them to a specified address.
     - Parameters:
       - `_address`: The address to which the tokens will be minted.
       - `_value`: The amount of tokens to be minted.

   - `burn`: Destroys existing tokens by reducing the total supply and the balance of a specified address.
     - Parameters:
       - `_address`: The address from which the tokens will be burned.
       - `_value`: The amount of tokens to be burned.

## License

This contract is licensed under the MIT License. SPDX-License-Identifier: MIT.

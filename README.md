Readme

MyToken Contract
This Solidity contract represents a basic implementation of a token called "LESTER" with the abbreviation "SYMON". It allows for the minting and burning of tokens, as well as tracking the token balances of addresses.

Contract Details

SPDX-License-Identifier: MIT

This line specifies the license under which the code is released. In this case, it is released under the MIT license.

pragma solidity 0.8.18

This line specifies the version of Solidity used for compiling the contract. In this case, it is version 0.8.18.

string public tokenName

This variable represents the public name of the token, which is set to "LESTER".
string public tokenAbbrv

This variable represents the public abbreviation of the token, which is set to "SYMON".
uint public totalSupply

This variable represents the total supply of tokens. It is initially set to 0 and will increase when new tokens are minted.

mapping(address => uint) public balances

This mapping represents the token balances of different addresses. It maps addresses to their respective token balances.

function mint(address _address, uint _value) public

This function allows for the minting of new tokens. It takes an address and a value as parameters and increases the total supply of tokens by the specified value. It also adds the minted tokens to the balance of the given address.

function burn(address _address, uint _value) public

This function allows for the burning of tokens. It takes an address and a value as parameters. If the balance of the given address is greater than or equal to the specified value, it decreases the total supply of tokens by the specified value and reduces the balance of the address accordingly.

Usage

Deploy the contract on the Ethereum blockchain using Solidity version 0.8.18.

Once deployed, you can interact with the contract using the following functions:

mint: Call this function to mint new tokens. Pass the recipient's address and the amount of tokens to be minted.

burn: Call this function to burn tokens. Pass the owner's address and the amount of tokens to be burned.

Note

This contract provides a basic implementation of a token and does not include functionalities such as token transfers or ownership management. It serves as a starting point for more complex token contracts

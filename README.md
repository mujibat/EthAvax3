# DOLTOKEN Smart Contract

## Overview

This Solidity smart contract, named DOLTOKEN, is designed to create a basic ERC-20 token with additional functionality. The primary features include:

- **Minting**: Only the contract owner has the authority to mint new tokens.
- **Transfers**: Any user can transfer tokens to other addresses.
- **Burning**: Any user can burn their own tokens, reducing the total supply.

## SPDX-License-Identifier

This code is licensed under the MIT License. Please refer to the SPDX-License-Identifier at the beginning of the code for more details.

## Prerequisites

- Solidity version 0.8.19 or higher

## Contract Details

### Token Properties

- **Name**: The name of the token is set during contract deployment and is accessible via the `name()` function.
- **Symbol**: The symbol for the token is also set during deployment and can be retrieved using the `symbol()` function.
- **Decimals**: The token has a fixed decimal value of 18.

### Ownership

- The contract includes a concept of ownership, with a designated owner who has special privileges.

### Events

- **Transfer**: Fired when tokens are transferred from one address to another.
- **Approval**: Fired when the owner approves another address to spend a certain amount of tokens.
- **Minted**: Fired when new tokens are minted and added to a specified address.

### Functions

1. **Constructor**
   - Initializes the contract with the token name, symbol, and sets the deployer as the owner.

2. **onlyOwner Modifier**
   - A custom modifier to restrict certain functions to the contract owner.

3. **mint**
   - Allows the owner to mint new tokens and assign them to a specified address.

4. **burn**
   - Enables any user to burn their own tokens, reducing the total supply.

5. **transfer**
   - Allows any user to transfer tokens to another address.

6. **name, symbol, decimals**
   - Getter functions to retrieve token information.

7. **totalSupply**
   - Returns the total supply of tokens.

8. **balanceOf**
   - Returns the balance of tokens for a specified address.

9. **approve**
   - Allows the owner to approve another address to spend a certain amount of tokens.

10. **allowance**
    - Returns the amount of tokens approved for a spender by the owner.

## Usage

1. Deploy the contract, specifying the token name and symbol.
2. The owner can then mint new tokens using the `mint` function.
3. Users can transfer tokens using the `transfer` function.
4. Users can burn their own tokens using the `burn` function.
5. The `approve` function can be used by the owner to grant spending approval to another address.
6. Token information can be queried using the various getter functions.

## Important Notes

- Ensure that the contract owner's private key is securely stored, as it has the authority to mint new tokens.
- Be cautious with the `approve` function, as it involves granting spending permission to another address.

## License

This code is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

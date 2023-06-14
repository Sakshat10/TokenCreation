# Token Contract

This is a simple token contract implemented in Solidity. The contract allows for the minting and burning of tokens, while keeping track of the total supply and individual balances.

## Requirements

1. The contract has public variables that store the details about the coin:
   - `tokenName`: The name of the token (e.g., "DOGECOIN").
   - `tokenAbbrv`: The abbreviation or symbol of the token (e.g., "DOGE").
   - `TotalSupply`: The total supply of the token.

2. The contract has a mapping of addresses to balances:
   - `balances`: A mapping that associates addresses with their respective token balances.

3. The contract has a `mint` function:
   - Parameters: `address _address`, the address to receive the minted tokens, and `uint256 _value`, the amount of tokens to mint.
   - Behavior: Increases the total supply by `_value` and increases the balance of the `_address` by the minted amount.

4. The contract has a `burn` function:
   - Parameters: `address _address`, the address to burn tokens from, and `uint256 _value`, the amount of tokens to burn.
   - Behavior: Decreases the total supply by `_value` and decreases the balance of the `_address` by the burned amount.
   - Conditional: The function checks if the balance of `_address` is greater than or equal to the `_value` before performing the burn operation.

## Usage

To use this contract, you can follow these steps:

1. Deploy the contract on an Ethereum-compatible blockchain network.
2. Interact with the contract using a smart contract wallet or through a web interface.
3. Call the `mint` function to create new tokens by specifying the recipient address and the desired token amount.
4. Call the `burn` function to destroy tokens by specifying the address to burn tokens from and the amount to be burned.
5. Make sure to check the balances and total supply variables to keep track of the token distribution.

Please note that this contract does not include additional functionalities like token transfers or allowances, as it focuses on the minting and burning operations.

## License

This contract is released under the MIT License. You can find the license text in the [LICENSE](LICENSE) file.


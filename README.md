# Token Contract

This is a simple token contract implemented in Solidity. The contract allows for the minting and burning of tokens, while keeping track of the total supply and individual balances.

## Requirements

1. **Token Details**: The contract has public variables that store the details about the token:
   - `tokenName`: A string representing the name of the token (e.g., "DOGECOIN").
   - `tokenAbbrv`: A string representing the abbreviation or symbol of the token (e.g., "DOGE").
   - `TotalSupply`: An unsigned integer representing the total supply of the token.

2. **Balance Mapping**: The contract has a mapping of addresses to balances:
   - `balances`: A mapping that associates addresses with their respective token balances. It allows querying the balance of a specific address.

3. **Mint Function**: The contract has a `mint` function:
   - Parameters: `address _address`, the address to receive the minted tokens, and `uint256 _value`, the amount of tokens to mint.
   - Behavior: Increases the total supply by `_value` and increases the balance of the `_address` by the minted amount.

4. **Burn Function**: The contract has a `burn` function:
   - Parameters: `address _address`, the address to burn tokens from, and `uint256 _value`, the amount of tokens to burn.
   - Behavior: Decreases the total supply by `_value` and decreases the balance of the `_address` by the burned amount.
   - Conditional: The function checks if the balance of `_address` is greater than or equal to the `_value` before performing the burn operation. If the condition is not met, the burn operation is not executed.

## Usage

To use this contract, you can follow these steps:

1. **Deployment**: Deploy the contract on an Ethereum-compatible blockchain network using a compatible development environment or deployment tool.

2. **Interaction**: Interact with the contract using a smart contract wallet, a command-line interface, or a web interface. You can use tools like Remix, Truffle, or Hardhat to interact with the contract.

3. **Minting Tokens**: Call the `mint` function to create new tokens. Provide the recipient address (`_address`) and the desired token amount (`_value`) as parameters to the function. This will increase the total supply and add the minted tokens to the balance of the recipient address.

4. **Burning Tokens**: Call the `burn` function to destroy tokens. Specify the address from which the tokens will be burned (`_address`) and the amount of tokens to be burned (`_value`) as parameters. This will decrease the total supply and deduct the burned tokens from the balance of the specified address.
   - Note: Before executing the burn operation, the function checks if the balance of the specified address is greater than or equal to the amount to be burned. If the condition is not met, the burn operation will not be executed.

5. **Monitoring Balances and Total Supply**: Keep track of the token balances and the total supply by accessing the public variables:
   - `balances[_address]`: Use this mapping to query the balance of a specific address.
   - `TotalSupply`: This variable holds the total supply of the token.

Please note that this contract provides a basic implementation of token minting and burning operations. It does not include additional functionalities like token transfers, allowances, or access control mechanisms. You can extend this contract or integrate it into a more comprehensive token ecosystem based on your specific requirements.

## License

This contract is released under the MIT License. You can find the license text in the [LICENSE](LICENSE) file.


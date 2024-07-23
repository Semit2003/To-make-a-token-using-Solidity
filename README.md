# **To-make-a-token-using-Solidity**

## **Overview**
The `UniqueToken` contract is a simple ERC-like token contract written in Solidity. It allows for the creation (minting) and destruction (burning) of tokens while keeping track of token details and individual account balances.

## **Contract Details**

### **Public Variables**
- **`tokenName`**: The name of the token, set to `"UniqueToken"`.
- **`tokenSymbol`**: The symbol of the token, set to `"UTK"`.
- **`totalTokenSupply`**: The total number of tokens in circulation.

### **Mapping**
- **`accountBalances`**: A mapping from addresses to their token balances.

## **Functions**

### **`mintTokens`**
- **Parameters**:
  - `address _address`: The address to receive the newly minted tokens.
  - `uint256 amount`: The number of tokens to mint.
- **Description**: Increases the total token supply and adds the specified amount of tokens to the balance of the given recipient address.

### **`burnTokens`**
- **Parameters**:
  - `address _address`: The address from which tokens will be burned.
  - `uint256 amount`: The number of tokens to burn.
- **Description**: Checks if the specified account has a sufficient balance to burn the specified amount of tokens. If true, it decreases the total token supply and reduces the balance of the specified account.

## **Usage**
- **Minting Tokens**: Call the `mintTokens` function with the recipient address and amount to mint new tokens.
- **Burning Tokens**: Call the `burnTokens` function with the account address and amount to burn tokens from that account, ensuring the account has enough tokens.

## **License**
This contract is licensed under the MIT License.

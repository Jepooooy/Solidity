# Solidity

This Solidity program is a straightforward "Creating a Token" example that illustrates the basic syntax and functionality of the Solidity programming language. The aim of this program is to provide a starting point for newcomers to Solidity, helping them understand how to create a simple token and get a feel for the process of developing smart contracts on the Ethereum blockchain.

## Description

This Solidity program is a basic example titled "Creating a Token" that demonstrates the essential syntax and functionality of the Solidity programming language. The primary purpose of this program is to serve as an introductory guide for those who are new to Solidity, providing them with a practical example of how to create a simple token on the Ethereum blockchain.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at 
https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the '+' icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Token.sol). Copy and paste the following code into the file:

```javascript
pragma solidity 0.8.18;
contract MyToken {

    
    string public tokenName = "META";
    string public tokenAbbrv = "MTA";
    uint public totalSupply = 0;

    
    mapping(address => uint) public balances;

    
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    
    function burn (address _address, uint _value) public {
        if (balances[_address] >= _value)
        totalSupply -= _value;
        balances[_address] -= _value;
    }

}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Ensure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile Token.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

After the contract is deployed, you can interact with it by calling its functions. Click on the "MyToken" contract in the left-hand sidebar to expand its functions. You can call the "mint" function to create new tokens, specifying the recipient's address and the amount of tokens to mint. Similarly, you can call the "burn" function to destroy tokens from a specific address. Additionally, you can check the "totalSupply" to see the total amount of tokens in circulation or use "balances" to check the token balance of any address.

## Authors

Metacrafter Chris  
[@metacraftersio](https://twitter.com/metacraftersio)


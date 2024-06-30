# Simple Contract

This program is a simple contract that tries to mint and burn supplies

## Description

This program is a simple contract that contains `mint` and `burn` functionalities for supplies

## Getting Started

### Executing program

To run the program, you can use Remix, an online Solidity IDE to get started. Here's the step-by-step instruction on how to make this work:

1. Open Remix (https://remix.etherum.org)
2. Copy the code below:
```sl
contract MyToken {

   // public variables here
   string public tokenName = "TempName";
   string public tokenAbbrv = "TN";
   uint public totalSupply = 0;

   // mapping variable here
   mapping (address => uint) public balances;

   // mint function
   function mint (address _address, uint _value) public {
      totalSupply += _value;
      balances[_address] += _value;

   }

   // burn function
   function burn (address _address, uint _value) public {
       if (balances[_address] >= _value) {
           totalSupply -= _value;
           balances[_address] -= _value;
       }
   }
}
```

the `mint` and `burn` function services as the methods that we'll be using for doing test in our program
3. Compile the code with compiler set to 0.8.9+
4. Deploy and Run The Code

### Testing the Code

After deploying the code, you should be able to `Deploy & Run Transactions` using the contract. Click the `Deploy` button and you'll see under `Deployed/Unpin Contract` your deployed contract. You can then proceed to test the code there using the UI they provide for testing how it works.

### Changing the code.

If you want to change how minting works in the code, you can do so by changing the `mint` function you can see in the `main.sol`

### Interacting with the code

To test your program, you can just go to the `Deploy & Run Transactions` section at the left navigation.

## Authors

Renz Angelo Aguirre


## License

This project is licensed under the MIT License - see the LICENSE.md file for details

# myTokens - SOLIDITY FINAL ASSESSTMENT
Solidity is the final project to show off code that creates a primary token contract. 
Solidity briefly introduces beginners to the procedures used to create tokens, burn them, and check the balances. 

# DESCRIPTION
Solidity is the programming language designed for developing smart contracts that run on the Ethereum Virtual Machine. 
This project requires making a contract that can be used to create tokens with two variables and public variables that store details about coins and mapping variables to map addresses to balances. 
Then there are two functions: the mint function, which increases the total supply by that number and increases the balance of the address by 
that amount, and the burn function, which works the opposite of the mint function as it will destroy tokens. 

# GETTING STARTED

# Executing program
To run this program, we can use Remix, for an online Solidity IDE. And to get started, go to the Remix website at https://remix.ethereum.org/.

Once you open the website, create a new file by clicking on the "+" icon in the left-hand sidebar And Save the file with a .sol extension (e.g., Yumang.sol). 
Copy and paste the following code into the file:


pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public name ="DHONALYN";
    string public abbrv ="LYN";
    uint public supply =0;

    // mapping variable here
    mapping(address=> uint) public blnc;

    // mint function
    function mint(address add, uint val) public{
        supply += val;
        blnc[add] += val;
    }

    // burn function
    function burn(address add, uint val) public{
        if(blnc[add]>=val){
            supply-=val;
            blnc[add]-=val;
        }
    }

}

To compile the code, click the "Solidity Compiler" tab in the left-hand sidebar. Next, click the "yumang.sol" button, then click compile code and wait for the green check to appear in the "Solidity Compiler" logo. After that, you can deploy the contract using the "Deploy & Run Transactions" tab in the left-hand sidebar after the code has been compiled. Choose the "salinas.sol" contract from the drop-down menu, then press the "Deploy" button. When it is ready, you can interact with the agreement by expanding the Deployed Contracts area below the address. Simply clicking the arrow button on the left side of your deployed contract will develop it. You can now interact with the agreement you generated. To set up the changes, enter the necessary information, such as the address (just copy the account address), the token's value, and the number of tokens you wish to mint, burn, and transact. Just select "balances" to check it.

# AUTHORS
Yumang, Dhonalyn L.

# LICENSE
This project is licensed under the MIT License - see the LICENSE.md file for details

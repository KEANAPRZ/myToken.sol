# myToken.sol
Final assesment for Netacrafters ETH PROOF: Beginner EVM Course
# DESCRIPTION
This program is a contract witten using Solidity that represents a custom token on the blockchain. It allows for the minting and burning of tokens. 
The token has a name "KEANA" and an abbreviation "KNA".The contract keeps track of the total supply of tokens and maintains a mapping of addresses to token balances.
#GETTING STARTED
# EXECUTING PROGRAM
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., myToken.sol). 
Copy and paste the following code into the file:
contract MyToken {

    // public variables here
    string public tokenName = "KEANA";
    string public tokenAbbrb = "KNA";
    uint public totalSupply = 0;
    // mapping variable here
    mapping(address => uint) public balances;
    // mint function
    function mint (address _address,uint _value) public  {
        totalSupply += _value;
        balances[_address] += _value;
    }
    // burn function
    function burn (address _address,uint _value) public  {
        if (balances[_address]>= _value){
        totalSupply -= _value;
        balances[_address] -= _value;
    }
}
}

To compile the code, click on the "Sol\idity Compiler" tab in the left-hand sidebar. 
Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile myToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. 
Select the "myToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by using the "Deployed Contracts". Copy and paste your "Acount" to the "Address" seen in the "Mint" you can add the value of tokens you want to mint by clicking on the "transact" button to execute.
Same goes to burning tokens just  Copy and paste your "Acount" to the "Address" seen in the "Burn" you can add the value of tokens you want to burn by clicking on the "transact" button to execute.
If you want to see the "Balances" just Copy and paste your "Acount" to the "Address" seen in the "Balances" and click on the "Call" button to see your balances. 
Finally, if you want to see the "totalSupply" just click on the "totalSupply" button.

# AUTHORS
Keana Aliza C. Perez

Student of National Trachers College - BSIT 2.2

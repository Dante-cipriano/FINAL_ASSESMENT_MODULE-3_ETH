# Final_Assessment_Module3_ETH

This is the Solidity Program, commonly known as the minting and burning program. This software will show you how to mint and burn the token, as well as the total quantity of the token.

# Description

For MetaCrafters' final assessment, I created an ethereum token that will mint, burn, and know the overall supply of the token.

# Getting Started

# Executing program

Search remix.etheruem.org first, then once there, find the create a new file and name it like this (name).sol then enter the code then add your name on token name and token abbreviation. When you're finished with the code, run the solidity compiler and compile your file. If you have finished compiling the code, you can now deploy and run transactions, then copy the account and use it the address of the burning,minting, and balances once you finish putting the account of the address then input a value then transact first transact the minting to store the token, then click the transact button on the burning to burn the token. And if you manufacture three tokens and then burn four, nothing will happen because you have exceeded the mint's store value. You sent an email to remix.etheruem.org.

//SPDX-License-Identifier: MIT
pragma solidity ^0.8.18;

contract ModuleThree {

    // public variables here
    string public tokenName = "DotaToken";
    string public tokenAbbrv = "DToken";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances [_address] += _value;
    }

    // burn function
    function burn (address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}

# Help

just check the code if there's missing like this symbol {, }, (, ), [] and ;. Please always check if there's an error per line, If there's an errror your file name will turn red or the red symbol will pop up on the left side of the number it means theres an error.

# authors

Dante R. Cipriano Jr.

8214040@ntc.edu.ph

# License

This project is licensed under the [MIT] License - see the LICENSE.md in the files details


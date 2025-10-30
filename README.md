# MyToken - ERC20 Token Example

This is a simple implementation of an ERC20 token built using Solidity. 

## Example Code

Here is the Solidity code for the ERC20 token:

pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

contract MyToken is ERC20, Ownable {
    constructor(uint256 initialSupply) ERC20("MyToken", "MTK") {
        _mint(msg.sender, initialSupply);
    }

    function mint(address to, uint256 amount) public onlyOwner {
        _mint(to, amount);
    }

    function burn(uint256 amount) public {
        _burn(msg.sender, amount);
    }
}# MyToken.sol
MyToken is a simple implementation of an ERC20 token built using Solidity. This contract demonstrates basic functionalities of an ERC20 token, including minting and burning tokens

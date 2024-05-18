// SPDX-License-Identifier: MIT
pragma solidity 0.8.25;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

contract DegenToken is ERC20 {
    address private owner;
    mapping(uint256 => uint256) public leagueTokens;
    mapping(address => mapping(uint256 => uint256)) public redeemedItems;

    constructor(string memory name, string memory symbol) ERC20(name, symbol) {
        owner = msg.sender;
        leagueTokens[1] = 10000;
        leagueTokens[2] = 8000;
        leagueTokens[3] = 7000;
        leagueTokens[4] = 5000;
        leagueTokens[5] = 3000;
        leagueTokens[6] = 1000;
    }

    modifier onlyOwner() {
        require(msg.sender == owner, "Only owner can call this function");
        _;
    }

    function mint(address account, uint256 amount) public onlyOwner {
        require(amount <= 10000, "Minting amount exceeds 10,000 tokens limit");
        _mint(account, amount);
    }

    function burnToken(address account, uint256 _amount) public {
    require(balanceOf(account) >= _amount, "Burn Failed: Insufficient Tokens.");
    _burn(account, _amount);
    }


    function transfer(address recipient, uint256 amount) public override returns (bool) {
        require(recipient != address(0), "ERC20: transfer to the zero address");
        _transfer(msg.sender, recipient, amount);
        return true;
    }

    function transferRewards(address to, uint256 itemId) public {
        uint256 redeemedItemCount = redeemedItems[msg.sender][itemId];
        require(redeemedItemCount > 0, "Insufficient redeemed items to transfer");
        redeemedItems[msg.sender][itemId]--;
        redeemedItems[to][itemId]++;
}

    function redeem(uint256 itemId) public {
        uint256 itemPrice = leagueTokens[itemId];
        require(itemPrice > 0, "Item does not exist");
        require(balanceOf(msg.sender) >= itemPrice, "Insufficient balance to redeem item");
        _burn(msg.sender, itemPrice);
        redeemedItems[msg.sender][itemId]++;
    }
    
    function viewRedeemedItems(address account, uint256 itemId) public view returns (uint256) {
        return redeemedItems[account][itemId];
    }
  
}

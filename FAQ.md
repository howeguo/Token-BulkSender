# Language:
[English](https://github.com/howeguo/Token-BulkSender/blob/master/FAQ.md)  | [中文](https://github.com/howeguo/Token-BulkSender/blob/master/FAQ_%E4%B8%AD%E6%96%87.md)

# Token BulkSender FAQ

Here, I am very grateful to you for your interest in our DAPP. Here are some common questions that I hope will help you:

# FAQ's

## Why do I need to do the approval option?
Because it's a safe way, you don't need to transfer tokens to our smart contract directly, and the approval option just grant permission for smart contract to spend up some amount, it's only available when you actually send a token transfer by our contract, so you don't worry about it, just do it.
[About ERC20 Token Standard#Approve](https://theethereum.wiki/w/index.php/ERC20_Token_Standard#Approve_And_TransferFrom_Token_Balance)

## Do I need to do the approval option every time?
No, you don't have to, in my suggestion, you can approve a large amount to smart contract in one time, that you can save some time and tx fees.

## Why is my transaction out of gas?
This is caused by the Ethereum's gas limit. Due to the special nature of your token contract, you can change the send address number per tx to 150, and you will succeed.

## Why was the approval option failed?
Please check if your token smart contract has the following similar code, if so, Just click Reset Aproval Amount, and then, approve again.

if ((_value != 0) && (allowed[msg.sender][_spender] != 0)) throw
```
 function approve(address _spender, uint _value) {
    // To change the approve amount you first have to reduce the addresses`
    //  allowance to zero by calling `approve(_spender, 0)` if it is not
    //  already 0 to mitigate the race condition described here:
    //  https://github.com/ethereum/EIPs/issues/20#issuecomment-263524729
    if ((_value != 0) && (allowed[msg.sender][_spender] != 0)) throw;
    allowed[msg.sender][_spender] = _value;
    Approval(msg.sender, _spender, _value);
  }
```

## Why is my token list not showing?
You must make sure you have install MetaMask(https://metamask.io) and unlock the right account.

## What's the max address number of one transaction?
The default number is 175, the max number is 200. This depends on the gas limit of Ethereum. If it is too large, the transaction may fail. 175 is the number we have tested with a high success rate. If you still often fail, try to reduce this number.

## What's the tx fee of one transaction?
The default tx fee is 0.01ETH, But we have VIP membership, you just need to pay 1 ETH to be a VIP, the tx fee will be zero forever for your account.

## Is your smart contract open source?
Sure, you can check them by the following link.

Mainnet: https://etherscan.io/address/0x2f6321db2461f68676f42f396330a4dc4a8f49df#code  
Ropsten: https://ropsten.etherscan.io/address/0xfe25a97b5e3257e6e7164ede813c3d4fbb1c2e3b#code










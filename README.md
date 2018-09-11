# Language:
[English](https://github.com/howeguo/Token-multisender/blob/master/README.md)  | [中文](https://github.com/howeguo/Token-multisender/blob/master/README_%E4%B8%AD%E6%96%87.md)

# Token MultiSender
This DAPP was used to send token or ETH to many addresses in one transaction, and that can help user to save tx fee

# Demo
![Demo](demo_en.gif)

# Problem:
Previously in Ethereum Network, additional tools were required in order to transfer many ERC20 tokens at once.
Many people still do this manually, one transaction at a time. This process is time consuming and prone to an error.

# Solution:
This Dapp allows a user to send thousands of token transfers in a very effecient way by batching them in groups of 0 - 245 token transfers per Ethereum transaction. This automation saves time by automatically generating transactions to MetaMask. Finally, this tool allows a user to maintain security of their account by delegating the trust of their private keys to a secure MetaMask wallet.

# How to use:
1. Install [Metamask](https://metamask.io).
2. Make sure you have an account in MetaMask which has a token balance.
3. Make sure your MetaMask is pointed to the network that you would like to use.
4. Make sure your MetaMask account is unlocked.
5. Go to http://multisender.phizhub.com
6. Wait for the full page to load.
7. Select a token from the dropdown that you would like to send.
8. Provide either EXCEL or CSV or TXT file with addresses and values.
9. Click next.
10. You need to approve a enough amount to our contract.
11. Once the approve transaction is complete, click Next, go to the Send List, click Send, MetaMask will automatically generate a transaction for your token (200 addresses per transaction).
12. Done!

You can test this tool on Ropsten test network, if you want to make sure that
everything will work as expected.

```
Proof of work:
![https://etherscan.io/tx/0x16aabf8e76f67e912eccb64c5a9d7de044109486f687236dae558c6139b2aa1d
](https://etherscan.io/tx/0x16aabf8e76f67e912eccb64c5a9d7de044109486f687236dae558c6139b2aa1d)
```

# Contract deployed and Source Code
Contracts deployed:  
Mainnet, ropsten  
Mainnet: 0x2f6321db2461f68676f42f396330a4dc4a8f49df  
Ropsten: 0xfe25a97b5e3257e6e7164ede813c3d4fbb1c2e3b  

Source Code:  
Mainnet: https://etherscan.io/address/0x2f6321db2461f68676f42f396330a4dc4a8f49df#code  
Ropsten: https://ropsten.etherscan.io/address/0xfe25a97b5e3257e6e7164ede813c3d4fbb1c2e3b#code 


# Disclaimer
I am not responsible for any loss from transactions derived by MultiSender.  Some of the underlying JavaScript libraries and Ethereum tools that were used are under active development. The website and smart contract has been thoroughly tested, there is always the possibility something unexpected happens resulting in losses of Ethereum and/or tokens.

Any ERC20 tokens you transfer to the Multisender will be sent out to the addresses that you provided.

I encourage you to assess its security before using the Mutlisender Dapp.

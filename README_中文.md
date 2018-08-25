# 语言:
[English](https://github.com/howeguo/Token-multisender/edit/master/README.md)  | [中文](https://github.com/howeguo/Token-multisender/blob/master/README_%E4%B8%AD%E6%96%87.md)

# Token Multisender
这个应用可用来批量发送以太币和ERC20的代币，通过批量交易，可以节省很多交易费。

# 问题:
以前在以太坊网络中，需要额外的工具才能同时发送许多ERC20代币。
很多人仍然通过手工的方式一个一个的发送，这个过程既耗时，也很容易出错。

# 解决方案:
这个应用允许用户几分钟内用很少的交易即可完成对上千个地址的代币发送，每次发送的数量为1到200个，默认是130。当你点击确认时，会自动生成交易到MetaMask。该工具允许用户通过将其私钥的信任委派给MetaMask钱包来维护其帐户的安全性。
.

# 如何使用:
1. 安装 [Metamask](https://metamask.io).
2. 确保你有MetaMask账户并且有代币或ETH余额.
3. 确保MetaMask连接到你想连接的测试环境.
4. 确保MetaMask账户账户是解锁状态.
5. 前往 http://multisender.phizhub.com
6. 等待页面全部加载完成.
7. 从下拉框中选择一个你想发送的代币.
8. 上传包含地址和数量的EXCEL或CSV或TXT文件.
9. 点击下一步.
10. 如果一些都没问题的话.
11. 需要您授信一定的额度给我们的合约.
12. 一旦授信交易完成, 点击下一步，进入到发送列表，点击发送，MetaMask将会自动为你的代币生成一笔交易 (每笔交易130个地址).
13. 完成!

你可以先通过ropsten网络来测试是不是跟你预想的一致.

```
Proof of work:
https://ropsten.etherscan.io/tx/0x1c7ba7e088dc3670cc24b100df9e67284f5d978560c3c6d5cd1fb0953d391f71
```

# 合约部署和源码
合约部署:  
Mainnet, ropsten  
Mainnet: 0xaab60b6cb2b0d9f0c7f0bfb7ffb727d2583f5e57  
Ropsten: 0x209ad7c282294e50bc51f499cc85c1c90386aa0f  

源码:  
Mainnet: https://etherscan.io/address/0xaab60b6cb2b0d9f0c7f0bfb7ffb727d2583f5e57#code  
Ropsten: https://ropsten.etherscan.io/address/0x209ad7c282294e50bc51f499cc85c1c90386aa0f#code 


# 声明
我不能保证任何交易的丢失
对于MultiSender产生的交易造成的任何损失，我概不负责. 该网站和智能合约已经过全面测试，总有可能发生意外情况，导致以太坊和/或令牌丢失。

您转移到Multisender的任何ERC20代币都将发送到您提供的地址。

我鼓励您在使用Mutlisender Dapp之前评估其安全性。

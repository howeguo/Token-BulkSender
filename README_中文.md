# 语言:
[English](https://github.com/howeguo/Token-BulkSender/blob/master/README.md)  | [中文](https://github.com/howeguo/Token-BulkSender/blob/master/README_%E4%B8%AD%E6%96%87.md)

# Token BulkSender
这个应用可用来批量发送以太币和ERC20的代币，通过在一个交易中实现批量发送，可以节省很多不必要的交易费。

# Demo
![Demo](demo_en.gif)

# 问题:
以前在以太坊网络中，需要额外的工具才能同时发送许多ERC20代币。
很多人仍然通过手工的方式一个一个的发送，这个过程既耗时，也很容易出错。

# 解决方案:
这个应用允许用户几分钟内用很少的交易即可完成对上千个地址的代币发送，每次发送的数量1到200个，默认是200。当你点击确认时，会自动生成交易到MetaMask。该工具允许用户通过将其私钥的信任委派给MetaMask钱包来维护其帐户的安全性。
.

# 如何使用:
1. 安装 [MetaMask](https://metamask.io).
2. 确保你有MetaMask账户并且有代币或ETH余额.
3. 确保MetaMask连接到你想连接的测试环境.
4. 确保MetaMask账户账户是解锁状态.
5. 前往 https://bulksender.app?locate=zh
6. 等待页面全部加载完成.
7. 从下拉框中选择一个你想发送的代币.
8. 上传包含地址和数量的EXCEL或CSV或TXT文件.
9. 点击下一步.
10. 如果一些都没问题的话.
11. 需要您授信一定的额度给我们的合约.
12. 一旦授信交易完成, 点击下一步，进入到发送列表，点击发送，MetaMask将会自动为你的代币生成一笔交易 (默认每笔交易200个地址，如果您在首页有修改该数量，则实际为您修改后的数值，最多245个地址).
13. 完成!

你可以先通过ropsten网络来测试是不是跟你预想的一致.

例子文件 EXCEL / CSV:

| Address   |Amount |
|----------|-------------|
|0x7edbaa86b8d2757322342157d3a44ed0f583514e |12|
|0x2f6321db2461f68676f42f396330a4dc4a8f49df |1123.126|
|0x001dbj28905DEA1a67940093fFeaCeee58cA91nc |1.03|

例子文件 TXT:
```
0x7edbaa86b8d2757322342157d3a44ed0f583514e,12
0x2f6321db2461f68676f42f396330a4dc4a8f49df,1123.126
0x001dbj28905DEA1a67940093fFeaCeee58cA91nc,1.03
```


```
Proof of work:
https://ropsten.etherscan.io/tx/0xd79502721c914f32d42c83d326c62ce635d2df3f012cd6bc667659505e3a4de2
```

# 合约部署和源码
合约部署:  
Mainnet, ropsten  
Mainnet: 0x2f6321db2461f68676f42f396330a4dc4a8f49df  
Ropsten: 0xfe25a97b5e3257e6e7164ede813c3d4fbb1c2e3b  

源码:  
Mainnet: https://etherscan.io/address/0x2f6321db2461f68676f42f396330a4dc4a8f49df#code  
Ropsten: https://ropsten.etherscan.io/address/0xfe25a97b5e3257e6e7164ede813c3d4fbb1c2e3b#code 


# 声明
我不能保证任何交易的丢失
对于BulkSender产生的交易造成的任何损失，我概不负责. 该网站和智能合约已经过全面测试，总有可能发生意外情况，导致以太坊和/或令牌丢失。

您转移到BulkSender的任何ERC20代币都将发送到您提供的地址。

我鼓励您在使用BulkSender应用之前评估其安全性。

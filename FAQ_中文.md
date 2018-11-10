 # 语言:
[English](https://github.com/howeguo/Token-BulkSender/blob/master/FAQ.md)  | [中文](https://github.com/howeguo/Token-BulkSender/blob/master/FAQ_%E4%B8%AD%E6%96%87.md)

# Token BulkSender 问题列表

首先非常感激您对我们的产品兴趣，这里我们列了一些常见问题，希望对你们有帮助:

# 问题列表

## 为什么需要授信?
因为这是一种安全的方式，这样你不需要直接给我们的合约转币，而且授信也只是授权我们的合约在真正的交易过程中一定数量的代币使用权，所以您不用担心我们会有任何不法的行为，在使用之前也建议您在测试网络上先测试使用。[关于ERC20代币授信官方说明](https://theethereum.wiki/w/index.php/ERC20_Token_Standard#Approve_And_TransferFrom_Token_Balance)

## 需要我每次都做授信吗?
其实是不需要的，如果您已经了解授信的含义, 我们的建议是您可以一次性给一个数量比较大的授信额度，这样您可以在以后的交易中不需要重复授信，可以省去不少的时间和手续费。

## 为什么授信会失败?
请检查您的代币合约代码是否包含如下代码, 如果是，请重置授信额度，然后重新授信新的数量即可.

if ((_value != 0) && (allowed[msg.sender][_spender] != 0)) throw
```
Proof of work:
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

## 为什么交易失败并且显示错误是"Out of gas"?
这是以太坊每个块的gas限制导致的，由于您的代币合约的特殊性（或者转账方法设计的过于复杂），您可以将单笔发送数量改成150，那样您就会成功了。

## 为什么我的代币列表不显示?
您必须确保您已经安装好MetaMask(https://metamask.io) ,然后确保在MetaMask中解锁了正确的账户。

## 单笔交易的地址数量限制是多少?
默认是175, 最大是200，这个也取决于以太坊每个块的gas limit上限，如果每次发送的地址数量过大, 交易可能会失败， 175是我们经过测试，成功率比较高、速度比较快的一个数量, 如有失败，可尝试将该数值调小。

## 单笔交易的手续费是多少?
默认手续费是0.01ETH, 但是，我们有VIP会员模式, 您只需要支付1个ETH，从我们DAPP中发起的所有交易将永久免手续。

## 智能合约是开源的吗?
当然, 你可以从以下链接中找到我们的源码。

Mainnet: https://etherscan.io/address/0x2f6321db2461f68676f42f396330a4dc4a8f49df#code  
Ropsten: https://ropsten.etherscan.io/address/0xfe25a97b5e3257e6e7164ede813c3d4fbb1c2e3b#code











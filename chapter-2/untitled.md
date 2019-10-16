# 2.2 签名与多重签名

### 签名

使用私钥对消息（数据）进行签署即会得到签名（Signature）。这一过程通常是将消息（数据）先通过哈希算法（Hash）生成哈希值，然后使用私钥对此哈希值进行签名。由签名（Signature）与消息的哈希值，便可以推出一个公钥，验证此公钥，便可知道此签名是否由公钥对应的私钥签名。

_Sig = FuncSig\(FuncHash\(m\), dA\)_

* _dA_ 是签名私钥
* _m_ 是交易（或其部分）
* _FuncHash_ 是散列函数
* _FuncSig_ 是签名算法
* _Sig_ 是结果签名

函数_FuncSig_ 产生由两个值组成的签名_Sig_，通常称为_R_和_S_：

Sig = \(R, S\)

通常，每个比特币签名会有三个长度：73、72、71，符合校验的概率为25%、50%、25%。所以每次签署后，需要找出符合校验的签名长度，再提供给验证方。

比特币的一个私钥，可以通过签名完成一个地址里的比特币的转账——这种情况可称之为“单签名交易”，因为转账只需要一个签名。

以太坊EIP-155“简单重放攻击保护”标准在交易数据结构中添加了v字段，即链标识符。它能确保为一个区块链（例如以太坊主网络）创建的交易在另一个区块链（例如以太坊Classic或Ropsten测试网络）上无效。因此，在一个网络上广播的交易不能在另一个网络上重播。

v签名前缀字段初始化为链标识符，其值为：

| **链** | **Chain ID** |
| :--- | :--- |
| 以太坊主网 | 1 |
| Morden \(obsolete\), Expanse | 2 |
| Ropsten | 3 |
| Rinkeby | 4 |
| Rootstock主网 | 30 |
| Rootstock测试网络 | 31 |
| Kovan | 42 |
| 以太坊经典主网 | 61 |
| 以太坊经典测试网络 | 62 |
| Geth私有网络 | 1337 |

数字签名在以太坊中有三个用途。首先，签名证明私钥的所有者（其暗示是以太坊账户的所有者）已授权币的支出或合约的执行。其次，授权证明是不可否认的（不可否认性）。第三，签名证明交易数据在交易签署后没有也不能被任何人修改。

### 多重签名

比特币的多重签名（Multi Signature，又被称为M-N多签名）指的是需要总共N个私钥中的M个（M≤N）共同签署一笔比特币转账（它实际收集的是这些私钥对应的公钥，签名时仍然是验证这些公钥），这笔交易才可能发生。多重签名的实质是一个地址里的数字加密货币的交易需要多个私钥通过规定好的合约授权。它通常被多个人或机构或程序脚本或人工智能用来协同管理数字资产。

多重签名的典型应用模式是：一个多重签名地址，可以有多个相关联的私钥进行管理，如果要转账，则需要按照合约规定，使用所有或部分相关联的私钥签署交易。譬如，你可以事先设置成N个私钥一起签名才能完成转账，你也可以设置为五个私钥中，有任意三个私钥进行签名即可转账。

以太坊的多重签名虽然机制和比特币的多重签名相近，但它充分发挥出其技术核心智能合约的特色，通过部署一个智能合约，并把N把公钥设为智能合约地址的资产的拥有人。以太坊的这么一点改变，让多重签名的应用发生了很大的提升！

### 比特币多重签名钱包和以太坊多重签名对比

以下将进行比特币核心钱包和以太币钱包在进行多重签名操作时的对比。

**共同点：**

都可进行多重签名，实现多方共同管理资产。

**不同点：**

1. 比特币：完全通过私钥管理，每一笔交易都需要人工进行多重签名。应用场景非常有限。

以太坊：基于智能合约管理，是否需要人工或者什么情况下需要人工进行多重签名，完全由智能合约细节决定。应用场景非常宽泛也非常灵活。譬如，可通过智能合约设置每日提款限额，超过每日提款限额时才需要人工进行多重签名。又譬如，以太坊多重签名可应用于所有采用ERC-20通证标准的数字资产的管理。再譬如，即使一方中所有掌握私钥的人都挂掉了，资金也不一定就“胎死腹中”，智能合约还能按照预设的条款执行（譬如30天这一方没有做出决策，则全部资金自动转给对方）。

1. 比特币：一般没有钱包余额限制

以太坊：有限制，譬如Mist钱包要求余额应不低于1.02 ETH，具体原因可参考：

[http://ethdocs.org/en/latest/account-management.html\#creating-a-multi-signature-wallet-in-mist](http://ethdocs.org/en/latest/account-management.html#creating-a-multi-signature-wallet-in-mist)

1. 比特币：一次性，而且如果转出金额小于钱包上的金额，需要填入找零地址。

![](../.gitbook/assets/0%20%287%29.png)以太坊：同一个合约地址可以反复使用。

这个对比应该让我们能够明白，以太坊在区块链领域的专业地位已经超越比特币的维度！



---
description: Smart Contract
---

# 4.3 智能合约

智能合约（Smart Contract）是用程序代码定义合约参与方的承诺，并能够完全抗干预地根据承诺自动执行包括转账数字加密货币在内的约定条款的协议。

智能合约允许在不同的匿名方之间进行可信交易和协议，而无需中央机构，法律系统或外部强制执行的机制。它们使得交易、状态和数据可追溯，透明且不可逆转。

智能合约的部署过程，可理解为发送一个包括可执行代码的特殊交易，将合约代码存储在区块链中（是在合约账户的accountstate中的codehash指向的一块存储区域中），交易只记录合约代码的哈希值（作为存证），当需要调用这个智能合约的方法时只需要向这个智能合约的地址发送一笔交易即可。

如果您懂一点点编程语言，或者您有丰富的微信使用经验，那智能合约是非常好理解的。

智能合约可以简单理解为可执行的公开透明的程序，被开发者部署到以太坊区块链上，与外界完全隔离并运行于以太坊虚拟机（Ethereum Virtual Machine，简称EVM）中，这样它就脱离了人为的干预。而完全只按照代码设定的规则运行。

智能合约为所谓的去信任提供了基础架构，它允许我们信任系统的输出，而不需要信任它里面的任何参与者。

我们今天所使用的任何技术，都是很多前人花费了几十几百年的摸索才得以实现的！ 智能合约也不例外。早在1994年，密码学家尼克萨博（Nick Szabo）就提出了智能合约的概念，并于1998年进行了尝试（Bit Gold），但没有成功，其中一个重要的原因是缺乏能够支持可编程合约的科技水平。而我们已经知道，比特币的发行（挖矿奖励）和转账等等，都是由程序根据协议（即合约）直接实施的，比特币为包含转账货币在内的可编程合约带来了巨大的技术突破。

区块链技术的出现不仅解决了该概念里最重要的合约对货币的百分之百的控制权，并且可编程的优势又让它秒杀了一切传统合约——而区块链的去中心化、不可篡改、过程透明可追踪等优点，更是令智能合约如虎添翼，一飞冲天！

智能合约是纯正且原生的区块链技术。它符合我们对于区块链价值观的所有期望。

智能合约的特色：

* 去中心化——智能合约是严格按照甲乙双方已写入代码的约定，封闭式自动执行的。勿需也不允许第三方的介入（思考：现在的预言机、Amberdata等等是否有问题？）。
* 勿需信用中介——勿需第三方的信用背书，智能合约本身以及区块链即可以提供可靠的保障。
* 不可篡改——通过区块链加密技术，它可以防范人为作弊等干扰，从而具体抗审查的能力。
* 透明可追踪——任何人都可以在链上查阅智能合约代码，从而彻彻底底了解它的所有细节。
* 匿名——智能合约是自主运行的，它不需要有人去启动或终止。也不需要知道你是谁。
* 精准——智能合约是用代码写出来的，它不存在任何语言上的歧义的可能。

请注意：除了区块链，其它任何技术都无法部署智能合约，如此则可以说，智能合约是区块链的独门秘技。

智能合约已经广泛应用到区块链ICO、游戏等领域，而比特币到目前为止在应用领域还只是一个货币，无法承载智能合约千变万化的应用。这样，我们再次看到了比特币极大的局限。而且智能合约在应用中爆发出来的威力，让我们几乎可以肯定：以太坊虽然任重道远，但百步已经走完九十九步，可以说为这个世界带来”智能合约“这一区块链技术的它已经非常接近成功。

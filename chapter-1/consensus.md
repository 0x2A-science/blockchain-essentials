---
description: 共识、共识算法、共识规则、共识机制、PoW、PoS、分叉、挖矿、挖矿难度与算力。区块链很忙的！
---

# 1.3 区块链的共识与共识机制

## 共识

共识是指在议题无法被搁置而必须得到解决的情况下，分歧各方搁置争议，达成能够被各方所共同接受的方案（即使对某些人有时只是勉强接受）的解决之道。

举个例子，工农红军在第五次反围剿失败后，又在“湘江战役”中遭受极大损失，部队下降到3万人。如果此时未通过著名的“遵义会议”调整领导层，使整支部队在正确的战略目标上达成共识，那么一味逃跑的工农红军就无法摆脱被围歼的命运。

还有个活生生的区块链领域的例子：比特币因为确认时间太长、每个区块可容纳的交易数量太少，而从2016年起，就完全不能适应市场的需求。但因为无法有效达成共识，造成它无法顺利地更新技术以及基础协议，发展陷入停顿，将智能合约市场拱手相让给以太坊，失去了技术领域的霸主地位。

## 共识算法、共识规则、共识机制

区块链的共识机制通常包含了两个方面：

* 达成共识的计算机算法，即共识算法（Consensus Algorithm）
* 达成共识的规则，即共识规则（Consensus Rule）

我们经常说的“共识机制”，多数情况下同时包含了共识算法和共识规则，少数情况下单指其中一方。这是导致我们的讨论经常发生穿越的原因之一。

百度云：_由于点对点网络下存在较高的网络延迟，各个节点所观察到的事务先后顺序不可能完全一致。因此区块链系统需要设计一种机制对在差不多时间内发生的事务的先后顺序进行共识。这种对一个时间窗口内的事务的先后顺序达成共识的算法被称为“共识机制”。_

这里解释的其实只是共识算法，也就是节点依照共识规则达成共识的计算机算法。

而共识规则（Consensus Rule）则是指每个区块链里面都有自己精心设计好的规则性协议，这些协议通过共识算法来保证它们可靠地得以执行。譬如我们通常所说的比特币的挖矿，就是比特币记账的共识规则，其专业术语为PoW（Proof of Work），即工作量证明。

比特币的工作量证明共识规则是通过SHA（Secure Hash Algorithm）系列安全散列算法之一的SHA256来可靠地得到执行的。

区块链账本或者数据的记录和维护是去中心化的，也就是往往有很多个记账节点。比特币或是以太坊这样的公有区块链，已有成千上万个记账节点。这些记账节点必须对所有区块有效性的验证都能达成共识。缺乏良好的共识机制，交易的验证就陷入混乱，对应的区块链也就会沦为投机者的温床，甚至是骗子和黑客的狂欢盛宴。因此共识机制对于区块链来说至关重要！

区块链有很多的共识机制，根本原因在于只要让人来做决策，就可能发生恶意的破坏行为，因此我们认为区块链最终的共识机制可能得依托于算法和开源代码。

## 最常用的两种共识规则

**Proof of Work（工作量证明，PoW）**

PoW的全称为Proof of Work，翻译过来就是“工作证明”或者“工作量证明”。

工作量证明是一种对应服务与资源滥用、或是阻断服务攻击的经济对策。一般是要求用户进行一些耗时适当的复杂运算，并且答案能被服务方快速验算，以此耗用的时间、设备与能源做为担保成本，以确保服务与资源是被真正的需求所使用。我们把用户为获利而付出劳动的行为称为“挖矿”。

此概念最早由Cynthia Dwork和Moni Naor于1993年的学术论文提出，而工作量证明一词则是在1999年由Markus Jakobsson与Ari Juels.所发表。现时此一技术成为了加密货币的主流共识机制之一。

比特币、狗狗币和莱特币等都是基于POW模式的数字加密货币。挖矿获得多少货币奖励，取决于挖矿贡献的有效工作，也就是说，矿机的性能越好、挖矿时间越长，所获得的货币奖励就越多。工作量证明的重要意义在于：它迫使货币的产生，需要付出一定的工作量和成本，这就赋予了货币一定的商品属性，使得自由市场这只无形的手能够通过“价格机制”自发地调节货币供应，保证了货币具有稳定的价值，从而使得货币能够获得人们的信任。

从共识层面讲，PoW的数学算法简单透明，并且完全去中心化；从理论上讲，任何人都可以加入到网络中并产生区块。

**PoS与DPoS**

PoS即权益证明，全称为Proof of Stake。它是以共识算法的方式，通过使用伪随机数或其它规则指定质押代币的人为矿工（记账员）或交易的验证者，并获得奖励或（及）交易手续费。

2012年8月点点币（PPCoin）的创世，首次实现了PoS（它采用PoW + PoS 的混合共识机制）。它是一个根据所持有货币的量和时间，给持有者发利息的一个模式。在PoS模式下有一个核心名词——币龄：每个币每天产生1币龄。比如你持有100个币，总共持有了30天（一个月），那么，此时你的币龄就为3000。这个时候，如果你发现了一个PoS区块，你的币龄就会被清空为0。你每被清空某个固定的币龄，就会从区块中获得一定的奖励（利息）——持币有利息。比如，首创PoS模式的点点币就是1%年利率。

PoS最大的问题是“富者更富”，在PoS体系下，受益的能力受持有代币的绝对限制。有人认为它是一种不公平的模式。另外质押代币会降低代币的流通量。

DPoS即授权权益证明，全称为Delegated Proof-of-Stake。

DPoS一般为股东投票产生代表。得票最高的代表（一般筛选出101个）有权将交易打包成区块，并获得系统的奖励和交易手续费。同时，他们还可能被赋予投票表决项目基金支配与否的项目各种开发的决策权。

DPoS的优势在于更快的区块确认和可扩展到VISA级别的每秒10000次支付或转账频率。但有些人担心它有违区块链“去中心化”的初衷。因此像达世币和早期以太坊就采用PoW+PoS的混合共识机制，来规避这样的风险。

2014年黑币（Blackcoin）对PoS进行了改进，Vitalick Buterin随后也多次专文对PoS进行了探讨。进阶阅读：

[https://blockgeeks.com/guides/proof-of-work-vs-proof-of-stake/](https://blockgeeks.com/guides/proof-of-work-vs-proof-of-stake/)

[https://en.wikipedia.org/wiki/Proof\_of\_stake](https://en.wikipedia.org/wiki/Proof_of_stake)



区块链已经在实践的共识机制还有好几十种，如Proof of Importance（重要性证明）、Proof of Assets（资产证明）、Proof of Burn（烧毁证明）、Proof-of-Purchase（购买证明）、Proof-of-Time（时间证明）、Proof-of-Identity（身份证明）和Combining Proofs（混合证明）等。

## 厘清共识的歧义

由于普遍缺乏正确的理解，我们发现区块链业界的讨论，经常在一条偏离的轨道上做无用功，因此有必要让大家重新认识下到底什么是“共识”：

* 1. **共识不是多数选举制**

共识需要全部投票通过。只有51%的人同意而达成的方案，不叫共识，75%通过也不叫共识，95%通过也不叫共识！

当然，学过数理统计的都知道，“全部投票通过”并非一定要达到100%。通过数理统计的方法，在实际没有达到100%，但通过计算，尚且处于系统误差范围之内的情况下，我们可以视为已经达成共识。

还有值得注意的一点是：投票应该科学设置。譬如只有“同意”与“不同意”二选一这样的投票表决机制的最大隐患是，它可能会扼杀真正有价值的新的解决方案。并且这样投票有的时候会阻碍我们进行充分的讨论，所以在共识沟通中，要允许有“保留意见”这样的投票，或者多种提案。

特朗普当选美国总统就是一个非常典型的案例！他是在有截止时间的情况下，仅限2选1，以多数制（Majority rule）而非共识机制选举出的美国总统！有很多美国公民持之以恒地反对他执政，也就有情可原了！

* 1. **共识最重要的核心是指反对派能够搁置不同意见，拥护一个所有人可接受的社区解决方案**

中国政府常说的“搁置争议，共同开发” （仅限这八个字），就是典型的共识。

* 1. **共识不是“全体一致同意“**

对于一个大社区，比如我们这个泱泱大国，在全体公民投票的情况下，相当多的提案，都不会得到“一致同意“。如果坚持必须“一致同意“，那么就会被个别人利用这一规则，阻挠区块链的重要决策。

共识只是让大家必须做出选择或者决策。一架飞机燃油耗尽，左边是大海，右边是森林，中间是乱石堆，迫降哪边如果您非要“一致同意”，不会游泳的人怎会同意迫降大海，害怕大树刺穿机体的怎会同意迫降森林？非要“一致同意”，那只有一种结果：撞上乱石堆！

比特币目前的转账处理速度是7笔/秒，已经难以满足市场需要，因此它迫切需要整个社区在多种解决方案中，达成一个共识。但此事讨论了两年多了，一直无果。问题的核心是：共识机制POW的决策者本来只有矿工，吃瓜群众根本不沾边。而此时比特币矿业已经中心化，并且其发展因此受阻，吃瓜群众介入进来，自然就步入了混乱状态。

* 1. **共识不是要全部完美解决**

共识只是要在关键时间点上，推动整个议题向前发展。

一个议题里面，常常有大家容易接受的部分，也有不容易接受的部分，要想它的方方面面都完全被所有人接受，那是不切实际甚至完全有毒的。把议题向前推进，在必要的时候再解决掉其中的缺陷或者分歧比较大的部分，这才是真正的共识。

比特币社区里的一些人，就非常害怕对比特币的修改不够完美，比特币社区现在的状态有时候甚至是“搁置共识，互相攻击”。

* 1. **共识不是一劳永逸**

共识在必要的时候，是可以更改的。以刚才飞机着陆为例，即使乘客已经达成水面降落的共识，如果机长的专业判断不同，加上时间也足够，他可以通过他的专业解释，影响乘客改变共识。无论是领袖还是群众，都可能犯错误，因此，坚持区块链数据不可篡改、坚持code is law是正确的，但坚持错误code带来的不良后果和被黑客污染的区块链数据不可通过共识修改，那就从根本上扭曲了共识的含义！

* 1. **共识不是竞赛或对抗**

一些地方常常把共识当竞赛或对抗来对待，这非常危险！它非常容易让社区变得不再友好！不友好的社区全球很多，它们有一个共同的名称：贫民窟！

以上讨论，主要参考了维基百科的共识定义，也是几十年开源软件协作的经验总结。

大家都已经知道，区块链往往是开源项目。特别是公有链，理论上它已经不是完全专属于某个公司或者某个团队。在这种情况下，维护社区的安全和健康发展，就特别需要以协议形式开放的而非建立在公司或者团队的权力基础上的，偏平而有效的管理体系。而这个体系里，除了达成共识的机制，还一定不能少了具有执行能力、能促成共识达成、可防止共识被破坏的奖惩工具。

脑筋灵活的马上会想到代币：共识规则的一个重要的核心，就是一套对区块链维护者们的代币奖惩制度！但目前区块链还没有很成熟地运用这种奖惩制度。

共识机制的根本作用是构建出一个既安全又符合其社区需求及社区发展的生态系统。毫不过分地说：共识机制就是构建其区块链生态的决定性机制。鉴于共识机制如此重要，我们往往还会把区块链的重要决策权也放到共识机制里解决——特别是后面要介绍的去中心化自治组织。

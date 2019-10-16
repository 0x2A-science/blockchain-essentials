# 1.7 区块链的定义与分类分歧

## 区块链的定义

区块链是一门尚处于萌芽期的崭新的学科——迄今还没有一个严格而完全统一的定义。我们认为综合性的定义大致如下：

**区块链（Blockchain）源于比特币的底层技术，是一种按时间顺序记录交易，智能合约的代码、运行状态及数据的分布式时态数据库，也是提供智能合约执行环境（亦即可以承载众多去中心化应用）的去中心化超级计算机。区块链是通过其共识规则、共识算法和智能合约等起到的安保、确权、监管、经济自治等作用，做到集去中心化运作、数据抗审查、去公信力等本质特征于一体的新兴互联网技术。区块链的终极目标是要完成从Internet of Information到Internet of Value的飞跃。**

换一个角度，我们可以看到区块链是通过去中心化的数据记录、点对点的数据分发、时间戳（timestamp）对每个数据块的计时、用密码学方法将每个区块与其前后区块唯一关联等等技术手段，来保证数据及其追溯性的安全可靠；但其核心创新，还是智能合约，和通过特定的共识机制保障其数据安全可靠以及数据具备抗审查（Anti-censorship）的特性。

区块链虽起源于比特币的底层技术，但是通过太坊智能合约等方面的拓展，它已经得到很大的提升。可以说经过比特币对共识机制的贡献和以太坊对于智能合约的贡献，区块链才开始显山露水，并且“大鹏一日同风起，扶摇直上九万里”。

区块链技术将会被应用到人类社会的方方面面，区块链也是迄今为止唯一能够帮助人类突破所有障碍，彻底消除政治、经济、文化等领域的差异，从而真正实现地球村的技术。

如果我们说比特币是第一个成功的区块链应用，以太坊是第二个杀手级应用。你是不是能够恍然大悟了呢？

## 区块链的分类及其分歧

区块链常被分为三类，普遍采用的是天才级的以太坊创始人[Vitalik Buterin的分类解释](https://blog.ethereum.org/2015/08/07/on-public-and-private-blockchains)（[中文版](https://www.8btc.com/article/65053)）：

1. 公共区块链（Public Blockchain，简称公有链）  
   公共区块链是指全世界任何人都可读取的、任何人都能发送交易且交易能获得有效确认的、任何人都能参与其共识过程的区块链——共识过程决定哪个区块可被添加到区块链中并能被明确其当前状态。作为中心化或者准中心化信任的替代物，公共区块链的安全由“加密数字经济”维护——“加密数字经济”采取工作量证明机制（proof of work）或权益证明机制（proof of stake）等公平公正、公开透明的方式，将经济奖励和密码学验证结合了起来，并遵循着一个原则：某个人从中可获得的经济奖励，与对共识过程作出的贡献成正比。这种类型的区块链通常被认为是“完全去中心化”的。

   公共区块链在区块链行业已经得到了爆发性的应用，譬如我们所熟知的比特币，以太坊及其竞争者Lisk、Waves，都是公共区块链。  


   公共区块链的优点可以归结为两点：

   * 保护用户免受开发者的影响

   在公共区块链中程序开发者无权干涉用户，譬如开发者是不可能冻结用户帐号的，所以公共区块链可以有效保护用户。

   * 轻松实现跨链交易

   私有链因为本来就不愿意透露其资产或数据，是不易实现跨链交易的。公共区块链，包括采用零知识证明的公共区块链，可以轻松实现跨链交易或数据分享。  

2. 联盟区块链（Consortium Blockchain，简称联盟链）  
   联盟区块链是指其共识过程受到预选节点控制的区块链；例如，不妨想象一个有15个金融机构组成的共同体，每个机构都运行着一个节点，而且为了使每个区块生效需要获得其中10个机构的确认（2/3确认）。区块链或许允许每个人都可读取，或者只受限于某些人可读取，或走混合型路线，例如区块的根哈希及其API（应用程序接口）对外公开，API可允许外界用来作有限次数的查询和获取区块链某些部分状态的密码学证明。这种类型的区块链可视为“部分去中心化”。  


   2017年5月下旬，区块链行业最知名的R3（[www.r3.com](www.r3.com)）领导下的全球银行业区块链联盟宣布已经完成其A轮投资的第二阶段，募资1.07亿美元，这是迄今为止区块链领域涉及金额最大的一轮投资。但R3 CEO大卫•鲁特（David Rutter）却说“我们正在蜕变为面向金融服务的新型操作系统”，并且早在三个月前，R3副主管兼前瑞士信贷区块链架构师克莱门斯•万（Clemens Wan）就已经公开说“我们意识到，我们不需要一个区块链系统，我们只希望在区块链技术中得到启发”\[2\]。R3区块链联盟已聚集100多家全球顶尖金融机构，其中包括来自中国的中国平安集团、招商银行、中国外汇交易中心、民生银行等。但从2016年底起，高盛（Goldman Sachs）、桑坦德（Santander）、摩根士丹利（Morgan Stanley）、摩根大通（JP Morgan）等多家巨头已经先后退出。其原因无非是一个平台无法完全照顾到所有金融企业的利益，并且各家金融机构的软硬件建设都已经相当完备，想要以无缝接管的方式置换其核心，工作量和成本都是巨大的。由此可见联盟区块链的实践有多艰难！  


   摩根大通（JP Morgan）后以以太坊为基础，通过改变共识规则、共识算法，增加权限管理，衍生出联盟链[Quorum](https://www.goquorum.com)，并于2016年11月22日发布 Quorum 1.0，但对于联盟链的实践并未带来多大的变化。  

3. 私有区块链（Private Blockchain，简称私有链）  
   私有区块链是指其写入权限掌握在一个中心化的组织手里。读取权限或者对外开放，或者被任意程度地进行了限制。相关的应用囊括数据库管理、审计等等都由一家公司内定，尽管在有些情况下希望它能有公共的可审计性，但在很多情形下，公共的可读性并非是必须的。  
  
   在零知识证明在区块链行业得到爆发性的应用之前，Vitalik已经思考过零知识证明在很多应用场景下，让私有链失去了存在的必要性。而比特股（Bitshares）和区块链社交平台Steem的创始人Daniel Larimer推出的EOS（www.eos.io），由于可以直接满足企业的管理需求，进一步挤压了私有区块链的生存空间。  


   Multichain、Corda和Hyperledger Fabric都是打造私有区块链的利器，但迄今尚未看到令人拍案的项目。  


   私有区块链的优点可以归结为以下几点：

   * 可以任性

   像改变游戏规则、还原交易、修改余额这种事，是绝不可能发生在公有链里的，但私有链可以任性，可以看心情——因此这个优点也可能是致命的缺点！  


   * 公开了交易审核者的身份

   只有私有链的主人才有交易的审核权，并且私有链的主人百分之百拥有交易的审核权。那么像PoW（工作量证明）里面大家担心的因为矿工串通而导致的51%攻击的危险，在私有链里根本就不存在——因为这方面的风险要么是零，要么是百分之百！这个优点显然也可能是其致命的缺点！  


   * 交易成本真的很低廉

   交易只需被几个受信的高算力节点验证就可以了，而不是需要数十万台矿机的协同，因此交易成本会便宜很多。事实上我们知道，公有链的代表比特币和以太坊，其交易手续费都不便宜。作者本人的比特币转账手续费的最高记录是单笔150元！  
   既然是私有链，交易手续费到底收多少，主人说了算，他要不想便宜大家那就真不便宜。并且，随着有向无环图（Directed Acyclic Graph, DAG）在区块链领域的应用，公有链交易手续费的问题应该能够得到大大的改善。  


   * 交易效率更高

   节点少，验证简单，因此私有链交易并发的承载能力也就优于公有链。

   但既然故障可以迅速通过人工干预来修复，万一人工出错，事情就难办了！  


   * 更好的隐私保护

   读取权限受到限制，即可提供更好的隐私保护。但公有链通过采用零知识证明，甚至可以达到更高水平的隐私保护能力。

Vitalik Buterin天才地预见了私有链的窘境，他分析说：

考虑到私有链的特色，似乎私有链无疑是机构的一个好的选择。然而，即使是在机构的环境下，公共区块链仍有很多价值，而且事实上，其价值在很大程度上体现在提倡公共区块链的哲学美德上，其中包括自由、中立和开放。公共区块链的优势一般分为两大类:

公共区块链提供了一种方法，可以保护应用程序的用户不受开发人员的影响，亦即有些事情即使是应用程序的开发人员也无权去做。经验不够的人很难理解为什么一个应用程序开发人员会想要自愿放弃权力和束缚自己。然而，更高级的经济分析提供了两个原因，用托马斯·谢林（Thomas Schelling）的话说：软弱是一种力量。首先，如果很显然你让自己做某些事情变得更加困难或不可能独自完成，那么其他人就更有可能信任你并与你进行互动，因为他们相信这些事情不太可能发生在他们身上。第二，如果你个人受到另一个实体的强迫或施压，然后说“即使我想我也没有权力这么做”，它就会变成一个重要的讨价还价的筹码，因为它会阻止那个实体强迫你去做的企图。应用程序开发人员面临的一个主要的压力或强制要求是政府，所以“审查反抗”与这种观点紧密相关。

公共区块链是开放的，因此很可能被许多实体使用并获得一些网络效应。要给出一个特定的例子，请考虑域名托管的情况。目前，如果A想要把域名卖给B，就需要解决标准的对手方风险问题:如果A先发，B可能不付钱，如果B先付款，那么A可能不发域名管理资料。为了解决这个问题，我们有中心化的托管中介，但收取的中介费是3%到6%。然而，如果我们有一个区块链域名系统，然后有一种货币也在同一个区块链上，然后我们可以通过智能合约（Smart Contract）削减成本接近于零：A可以发送域项目到一个程序（管理的合约地址），程序立即转发给B，并将B事先托管给程序的钱转给A，并且程序是可信的，因为它运行于一个公有链。请注意，为了有效地工作，来自完全不同行业的两个完全异构的资产类别必须位于同一个数据库中——这种情况显然是不容易发生在私有链上。另一个类似的例子是土地注册和产权保险，尽管重要的是要注意到互操作性的另一个途径是有一个公有链可以验证的私有链，类似BTC Relay采用的方法，并执行跨链交易。

注：ConsenSys公司和以太坊开发的BTC Relay是一个以太坊智能合约，允许以太坊用户使用比特币支付。作为以太坊和比特币之间的一座桥梁，BTC Relay为那些想要使用以太坊和智能合约应用来验证比特币交易的开发者提供了一个工具。

[![Gitter](https://badges.gitter.im/naturaldao/区块链概论.svg)](https://gitter.im/naturaldao/区块链概论?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

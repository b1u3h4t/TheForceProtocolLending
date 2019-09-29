# 币币贷产品说明

## 币币贷简介

币币贷由注册在塞舌尔的 *Bibidai Distributed Network Technology Service Group Ltd.* 运营管理。币币贷依托原力协议开源框架，搭建全球借贷网络，根据社会各阶层和群体的不同借贷需求制定专属方案，提供适当、有效的金融服务，关注欠发达国家或地区的弱势群体，践行人类普惠金融事业。

币币贷的去中心化借贷服务，是基于以太坊、EOS等主流公链开发的借贷dApp，支持点对点质押借贷和汇集流动性借贷，质押资产由智能合约保管。币币贷业务旨在改善全球各区域金融服务的不平衡，实现全球借贷资源共享。

### 产品要素和规则

币币贷将提供两种类型的借贷服务：点对点借贷和集中借贷。

#### 点对点借贷

表1 基于以太坊的去中心化点对点借贷产品

<center>

| <b>要素</b> | <b>规则</b> |
| ------ | ------ |
| <b>借币币种</b> | USDT(ERC-20)、DAI、QIAN（原力协议稳定币，即将推出） 
| <b>质押币种</b> | ETH、BNB、FOR、WBTC、BAT、HT、MKR、LRC等 
| <b>质押率</b> | 180%（=质押币市值/借币市值）
| <b>补仓线</b> | 150% |
| <b>平仓线</b> | 120% |
| <b>日利率</b> | 万1到万8，借币用户自主设置 
| <b>借款期限</b> | 7、14、30、60、90天，借币用户自主选择 
| <b>最低借款数量</b> | 等值 10 USD 起
| <b>手续费</b> | 见备注
| <b>订单有限期</b> | 若订单在5个自然日内未成交，订单将被系统取消。

</center>

<b>备注：</b>

日手续费率万0.5（以页面提示为准），向借币用户和出借用户双向收费。借币者还款时支付手续费，出借者出借时支付手续费。质押率到达120%时将被平仓，其中5%质押币将转给借币订单来源渠道，5%作为币币贷平仓费用，110%转给出借人。

<br>

#### 集中借贷

点对点借贷让借贷双方能够自由的确定借贷的条款，但是也带来了很多不便：参与点对点借贷，用户需要自主发布、管理贷款订单，在抵押借贷的情况下，借贷双方需要随时关注抵押物的价格变化，同时，一笔点对点借贷订单从发布到最终成交，往往需要经过漫长的等待……这些不足之处，限制了点对点借贷业务的规模和增速。

传统银行业通过将资金集中，大大提高了借款的效率，通过银行业，借贷业务能够真正的推动实体经济的增长。然而，传统银行业的借贷业务申请流程复杂，借款人被银行拒绝贷款的概率高，传统银行业借贷的种种不便因素，为新型的借贷工具提供了发展的机会。

通过将不同资金来源但是符合相同借贷条件的资金集中起来，就可以创造出聚焦于特定借贷条件的资金池，向资金需求方快速提供资金。借助智能合约技术，人们能够首次实现不通过传统银行业汇集出资人的资金：通过部署在主流区块链系统上的自动程序（智能合约），出资方可以无摩擦的快速获得资金收益，有资金需求的借款方在提供合适的抵押物之后就可以快速便捷的获得财务支持，此类业务模式已经在以太坊的Compound借贷协议得到了市场认可。

币币贷在项目创立初期就设立了点对点借贷、集中借贷两种业务模式的技术架构。在实际发展中，我们先落地并完善了点对点借贷协议，在开发集中借贷功能的过程中，我们参考了Compound借贷协议的理念，精简了我们原有的基于不同借款周期的资金池模型，对每种特定的借贷资产只采用一种集中借贷模式。

我们改进了Compound协议在利率模型、cToken设计等方面的不足，提出了币币贷原创的集中借贷产品架构。

**资金归集**

币币贷的用户可以通过dApp的“存币生息”功能，将稳定币资产转给智能合约托管获取利息收入，由币币贷的智能合约汇总每个用户的供给。在智能合约内的剩余资产足够时，用户可以随时将其稳定币资产从智能合约转出，不需要等待贷款到期。在上线初期，币币贷dApp将提供DAI和USDT两种稳定币的资金池，随着系统的持续运行，将考虑纳入USDC、PAX等更多种类的稳定币。

**借入资产**

币币贷dApp支持用户直接将其ERC-20资产用于借贷抵押，快速便捷的通过集中借贷功能获取稳定币资金，无需挑选借贷条款，借款期限等因素，随着借款时间延长，所付出的利息成本也可供预测，保持了透明。随着稳定币资金池内剩余可出借资产的变化，借款利率将根据算法自动调节。

- 抵押品类型

在币币贷dApp上线初期，智能合约接受ETH、FOR、BNB、HT、MKR、LRC、ZRX、BAT为抵押物。由于不同的抵押物资产在流动性、使用人群等方面存在区别，对于不同的抵押品，能够获得的借贷比例也会有所不同，具体借贷比例数值将会随着各抵押物品种的发展，由社区治理进行定期调整。

**风险与清算**

当借款人的未偿还借款超过其抵押物限定比例时，系统会要求借款人及时补仓，若借款人未在规定时间内完成补仓，则其抵押物将被智能合约扣押，进入清算流程。此时，允许套利者调用清算合约，按照一定的折价比例用稳定币置换扣押资产，任何持有足够稳定币资产的以太坊地址都可以调用清算合约。清算程序内置于合约中，无需依赖外部系统的支持，因此清算过程将保持高效和快捷。

**利率模型**

币币贷dApp采用一套算法控制的利率模型，基于供求关系的变化，利率自动调节，从而有效的影响借贷总规模、资金供应量等因素。

对于借贷资金的调控，币币贷遵循以下原则：当借贷资金池内的资金借出量较低时，借贷利率上涨的速度较低，以促进借款人从资金池借款；当借贷资金池内的资金借出量较高，甚至接近饱和时，借贷利率上涨的速度较快，带动存款利率增加，以促进存款人向资金池内存入更多稳定币。通过算法调节，确保整个借贷资金池的发展和增长处于健康的范围。

对资金借出量进行量化，我们引入参数x，代表资金借出的比例，其公式为：

x = a稳定币的借出总额 / (a稳定币剩余可借总额 + a稳定币的借出总额)

设借款利率为y，y和x的关系可以用分段函数表示如下：

<div align = center>

![GitHub](https://raw.githubusercontent.com/theforceprotocolgroup/TheForceProtocolLending/Dev/Images/interest.rate.equation01.latex.gif "Pool lending interest rate equation")

</div>

与Compound这样采取简单利率变化机制的模型不同，币币贷dApp将利率的变化分为了三个阶段，在第一阶段，为了刺激初始的借贷量上涨，利率增长模型近似指数曲线，这也符合自然增长规律；在第二阶段，通过积累一定量的借款额，利率的增长速度进入了稳定期，其图形符合一定斜率的直线；在第三阶段，由于借出的资金量已经较多，借贷利率的增加速率会加快，以适当的控制资金借出速度，促进存款量增加，利率增加的速度会逐渐逼近一个极值，这一阶段的利率变化接近于修正指数曲线。

**利率计算**

从第一笔借款开始，每次交易发生都会引起资金借出率x的变化，从而导致利率y发生变化，对于稳定币资产的借款利率，假设y为前一交易发生时的利率，y'为后一交易发生时的新利率，y和y'之间的利息额采取逐块计算，公式为：

y'时的利息额 = y时的利息额 + a稳定币的总借出额 × y × （ n个间隔区块 / 年总区块数 ）

对于存款利率的计算，采用下列公式：

a稳定币的存款利率 = a稳定币借款利率 × 资金利用率x × 调整比例

其中，调整比例由社区治理确定，( 1 - 调整比例 ) 可以视为合约的息差收入，这部分收入将用于维持智能合约正常运转的应急储备金，其计算公式为：

a稳定币的储备金（ y 和 y' 之间） = y'时的利息额 × ( 1 - 调整比例 )

**喂价机制**

系统需要实时获取外部价格以监控质押率的变化，以便及时清算，控制风险。在没有成熟的去中心化预言机解决方案时，系统将维护一个喂价地址白名单，该白名单由社区治理投票新增或去除。每个喂价都包含价格信息和价格有效期，系统从所有有效喂价中计算出中位值作为最终价格。在有了行业普遍认可的预言机方案之后，系统将会切换到对应的去中心化预言机，以保证喂价机制的公平、公正、公开、透明。

**治理机制**

币币贷dApp的治理采取社区治理和管理团队相结合的形式，涉及增加新的稳定币资金池，更新全局利率模型，更新oracle地址，修改利息调整比例，管理团队改选等重大事项时，将经过社区的充分讨论和投票；币贷团队成员组成的管理团队则负责日常的dApp开发运营维护工作。

<br>

### 共享订单簿

借币用户向智能合约质押数字货币，自主设定借款利率和借款期限即可创建借款订单。每笔借款订单将进入币币贷共享订单薄，该共享订单簿向所有币币贷合作伙伴开放，来自任何合作伙伴的出借用户可以选择其中任意一笔借款订单进行出借。

<div align = center>

![GitHub](https://raw.githubusercontent.com/theforceprotocolgroup/TheForceProtocolLending/Dev/Images/SharedOrderBookCN.jpg "Shared Order Book")

图1 共享订单薄</div>

<br>

### 全球借贷网络

币币贷通过合作节点搭建全球借贷网络，实现全球借贷资源共享。所有合作节点可以享受手续费分润。

- 平台合作节点：数字货币钱包、数字货币交易所及其他流量平台等；
- 区域合作节点：区域性金融机构和个人（需符合当地法律法规）。

<div align = center>

![GitHub](https://raw.githubusercontent.com/theforceprotocolgroup/TheForceProtocolLending/Dev/Images/GlobalLendingNetworkCN.jpg "Global Lending Network")

图2 全球借贷网络</div>

<br>

### 合作模式

币币贷提供多种接入方式，方便各合作方快速接入。

<b>表3 币币贷合作模式</b>

| 接入方式 | 账户模式 | 是否需要开发 | 适合对象 |
| ------------- | ------------- | ------------- | ------------- |
| H5 | 托管账户 | 无需开发 | 流量平台 |
| dApp | 钱包 | 少量开发 | 钱包平台 |
| API | 自定义 | 自主开发 | 专业借贷平台 |

<br>

### 技术支持

币币贷依托原力协议开源框架开发，是原力协议支持的首个落地DeFi项目。

由原力协议提供的技术解决方案包括：

- 托管账户
- 预言机
- 借贷合约套件：质押、借款、出借、还款、补充、平仓等

<br>

### 币币贷借贷公益基金

为践行人类普惠金融事业，币币贷成立借贷公益基金，向全球欠发达国家和地区用户提供低息借款服务。对欠发达国家和地区的区域性合作节点，币币贷将分配更多服务费，并提供全方位的技术和资金支持。

<br>

### 我们的优势

- 真正落地的DeFi产品
- 致力于完全去中心化
- 智能合约保管资产，合约代码开源
- 息费自动清结算
- 共享全球借贷网络

<br>

### 去中心化借贷产品研发路径

币币贷以实用和落地为准绳开发，致力于推动完全去中心化全球借贷网络搭建。

<b>表4 去中心化借贷产品研发计划</b>

| 时间计划 | 内容 | 详情 |
| ------------- | ------------- | ------------- |
| 已上线 | 基于iOS的中心化借贷产品 | MVP验证性产品 |
| 已上线 | 基于EOS的去中心化借贷产品 | MVP验证性产品 |
| 2019年8月 | 基于ETH的去中心化借贷产品 | 形成借贷网络，支持dApp、H5模式 |
| 2019年10月 | 基于ETH的去中心化借贷产品 | 用户体验优化、支持API模式 |
| 2019年12月 | 基于ETH的去中心化借贷产品 | 完善去中心治理架构 |
| 预计2020年底 | 基于原力协议金融公链的去中心化借贷产品 | 支持所有主流加密资产 |

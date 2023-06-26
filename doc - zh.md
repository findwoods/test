# ZH

# 面向全球的量子DNA分析项目

2023年6月12日

回应Wellcome Leap关于量子生物学（Q4Bio）的征集要求

总资金申请：$\$1,355,324$ 总计划工作时间：2.5年。

业务联系：

部门：

组织：

电话：

电子邮件：Lien Pham

加州大学洛杉矶分校合同与拨款管理办公室

$424-259-5934$

lien.pham@research.ucla.edu

Jens Palsberg是加州大学洛杉矶分校的计算机科学教授。他是ACM量子计算交易的副编辑，并且在2023年因他关于量子计算的课程而获得了UCLA颁发的Eon仪器杰出教学奖。

Sriram Sankararaman是加州大学洛杉矶分校的人类遗传学、计算医学和计算机科学教授。他是《计算生物学杂志》的编委，并在2020年获得了NSF职业奖。

## 项目的执行摘要

### 目标和演示

对大规模人群的DNA分析已经取得了引人注目的发现，引起了全球的轰动。其中一些进展为我们提供了关于我们起源的理解，包括我们的祖先居住在哪里以及如何找到未知的亲属。其他进展则为我们的健康提供了洞察，包括我们是否遗传了疾病的风险因素以及我们是否对某种药物反应不佳。随着越来越多的人进行DNA测序，这些发现变得越来越有用。

DNA测序的增长速度非常快。在2001年进行了第一次DNA测序，2010年对数百人进行了基因变异的测量，2015年增加到了数千人，而2018年的数据集则整合了大约50万人的遗传和表型信息。如今，已有超过3000万人进行了DNA测序，并且这个数字还在增长，部分原因是每人的价格标签为

每人$\$400$，而且价格还在下降。不断增长的数据集为DNA分析提供了在进化和医学领域提供新见解的巨大机会。

处理数十亿人的DNA数据的主要障碍是计算能力。原因是当前的算法在即使是最快的经典计算机上也无法进行扩展。事实上，处理高达100万人的DNA分析的当前算法可能需要几天的计算时间。对于潜在的80亿人口规模的数据集，这是一个数量级的增加，对于经典计算机来说是不可达到的。我们将利用量子计算来革新DNA分析的速度，从而克服这个问题。

我们的起点是我们最近开发的三个经典DNA分析算法。这些算法可以发现自然选择、遗传疾病的可遗传性和疾病发展风险。对于每个算法，我们将用指数级更快的量子计算方法替换最耗时的经典子程序。得到的算法将是经典和量子的混合算法。一旦我们插入指数级更快的量子子程序，我们期望我们的算法能够在即将到来的量子计算机上适用于全球范围内的应用。

我们将使用现有的量子电路模拟器来模拟我们的算法。我们将在现有的DNA数据集的子集上运行模拟，该数据集包含488,363个个体的数据。我们将专注于适应于30个量子比特和电路深度为20,000的子集。我们将比较我们的算法与我们最先进的经典算法的性能。我们将通过在一系列更大的子数据集上运行来研究扩展性。在实践中，我们预计模拟可以扩展到30个量子比特。

最终，我们将在量子计算机上运行我们的算法。我们将在包含488,363个个体的完整数据集上运行，我们估计我们需要50个量子比特和电路深度为50,000。我们计划与谷歌合作，谷歌过去曾向我们提供53个量子比特的Sycamore量子计算机的使用权限，这对于我们的项目来说是足够的。

对于未来的80亿人的DNA数据集，我们估计我们需要70个量子比特和电路深度为100,000。因此，我们的项目将实现面向全球范围的DNA分析。

### 研究重点和活动

#### 算法

我们选择了一个我们的三个经典算法已经处理过的DNA数据集。这些运行的结果将作为我们即将推出的算法的基准。我们的下一步是设计我们算法的经典和量子混合版本，并准备一个表示数据集的量子状态。

##### 数据集。我们的数据集是英国生物库（UK Biobank）数据集[4]，其中包含488,363个个体的DNA数据。对于每个个体，我们将关注约500,000个基因变异的信息。对于每个基因变异，该信息表示这个突变是从个体的母亲和父亲那里遗传而来的数量。数据集包含这些突变的计数，每个突变的值为$0,1,2$之一。

只有经过申请和批准的过程后才能访问英国生物库数据集。我们在这方面有多年的积极经验，并已经在这个数据集上运行了我们的三个经典算法。

##### 自然选择。我们提出了一个经典算法[3]，可以识别出近期正选择的多个全基因组信号，这些信号是基因组中进化异常迅速且高度可能具有功能重要性的区域。我们的算法处理UK Biobank数据集需要30分钟的时间。

我们算法的主要步骤是找到主成分，即对应于最大特征值的特征向量。我们可以用已知的量子主成分分析算法[17, [T]]替换这一步骤。量子主成分分析的主要步骤是相位估计，该算法使用了两次。对于可以用$n$个量子比特表示的数据，该算法需要$O(n)$个辅助量子比特和深度为$O(n^{2})$的电路。

##### 遗传疾病的可遗传性。我们提出了一个经典算法[2T]，可以识别出哮喘、湿疹、甲状腺和自身免疫疾病中FANTOM5增强子的遗传性富集，遗传信号的一个度量。我们的算法处理UK Biobank数据集需要3小时的时间。

我们算法的主要步骤是估计一个矩阵的迹，即对角元素的和。我们可以用已知的量子迹估计算法[18, 引理31]替换这一步骤。量子迹估计的主要步骤是幅度估计，主要依赖于相位估计。然而，论文[18]中的算法解释使用了QRAM，这在项目期间可能不可用。因此，我们需要重新设计算法，使用一种已知的表示方法。我们计划使用与量子主成分分析相同的表示方法。对于可以用$n$个量子比特表示的数据，新算法的表述不需要辅助量子比特，电路深度为$O(n^{2})$。

##### 疾病发展风险。我们提出了一个经典算法[6]，可以推断人群结构，了解个体基因组的复杂祖先起源，从而提高我们对根据遗传祖先而变化的疾病风险的理解。我们的算法处理UK Biobank数据集需要51小时的时间。

我们算法的主要步骤是找到一个非负矩阵分解，即使用只有非负元素的矩阵进行分解。我们可以用已知的量子非负矩阵分解算法[8]替换这一步骤。量子非负矩阵分解的主要步骤是哈密顿模拟和相位估计。对于可以用$n$个量子比特表示的数据，该算法执行$n$次哈密顿模拟，然后进行一步相位估计。我们计划通过Trotter方法进行哈密顿模拟，这引发了一个问题，即我们需要多少个时间步骤才能得到一个好的分解。我们的假设是，使用电路深度为$O(n^{2})$的足够多的时间步骤。该算法需要$O(n)$个辅助量子比特。

##### 数据加载。在对UK Biobank数据集上运行量子子程序的初始步骤是进行数据加载。这一步骤将数据集的经典表示映射到数据集的量子表示[10]。量子表示可以是一个幺正矩阵或者一个量子态，供量子子程序使用。

UK Biobank数据集有488,363个$\times$ 500,000个数据点，每个数据点的值为0,1,2之一。这个数据集的经典表示需要近1万亿位（1TB），我们可以用40个量子比特来表示，因为$2^{40}$大于一万亿。我们将以一种适应相位估计和哈密顿模拟的方式进行数据加载，这是我们量子子程序的关键组成部分，如上所述。

### 模拟

我们在量子电路模拟器方面有多年的经验，既是实施者也是用户。从这些经验中，一个显著的观点是，模拟器在可扩展性、噪声模型和易用性方面存在巨大差异。对于处理英国生物库数据集的算法模拟，可扩展性至关重要。因此，根据目前可用的资源，我们计划使用Google的qsim模拟器。qsim模拟器可以在一个成本为10000美元的90核Xeon台式机上进行无噪声模拟，使用40个量子比特。它还可以在同一类型的计算机上使用30个量子比特进行有噪声模拟。然而，这些观察结果是针对特定应用的。我们估计对于我们的算法来说，30个量子比特的模拟已经是qsim可以达到的极限。因此，我们将在英国生物库数据集的一个子集上运行，该数据集的数据和算法适合30个量子比特。

我们的模拟的基准是我们在英国生物库数据集上运行经典算法的论文中提供的真实结果。与基准结果的比较将帮助我们调试量子算法并寻找改进的方向。

除了模拟，我们还将使用我们自己的验证方法[24]来增加对量子子程序的信心。

### 实验

在我们对量子计算机和整个英国生物库数据集运行我们的算法的实验中，我们需要50个量子比特。我们有在Google、IBM和Rigetti的量子计算机上运行的经验。我们预计能够获得53个量子比特的Google Sycamore的访问权限，就像我们过去一样。虽然我们以前可以免费使用Google Sycamore，但我们已经为访问成本做了预算。

我们希望获得尽可能高的可靠性。我们预计量子计算机的可靠性在项目期间会得到改善，我们将密切关注这一点。我们注意到，在项目期间添加纠错编码来修正量子电路的错误是不太可能的：这需要太多的量子比特。我们将优化我们的量子电路，减少其门数和深度，从而增加其在近期量子计算机上成功运行的可能性，而不是添加纠错编码。我们将同时依赖现成的优化器和我们自己的优化器[23]。我们将以高级方式使用Cirq [12]编写我们的算法，以便能够轻松将其编译成不同的门集和不同的量子比特连接方式。

### 研究方向、平衡和整合

图[3]展示了我们的项目。我们的起点是我们最近的三个用于DNA分析的经典算法。在第一阶段，我们将关键子程序替换为指数级更快的量子子程序。在第二阶段，我们将在英国生物库数据集的一个子集上模拟量子经典混合算法。这将涉及30个量子比特和20,000个深度的量子电路。在第三阶段，我们将在量子计算机上使用混合算法对整个英国生物库数据集进行实验。

### 关键中期项目评估和里程碑

**第一阶段结束时：我们拥有了三个可以处理DNA数据的混合量子-经典算法。**

**第二阶段结束时：我们已经在英国生物库数据集的一个子集上使用qsim模拟器演示了所有三个算法，使用了30个量子比特。**

第三阶段结束时：我们已经在量子计算机上对整个英国生物库数据集进行了运行，使用了50个量子比特。

### 风险缓解和备选策略

我们认为项目存在三个主要风险，并采取以下缓解策略。

风险1：量子子程序效果不佳。我们将使用我们认为能够正常工作和按照广告宣传的量子子程序。然而，其中一个或多个子程序可能效果不佳或需要比预期更多的资源。通过使用三种不同的使用不同量子子程序的算法，我们多样化了风险。因此，即使其中一个子程序令人失望，其他子程序可能表现良好。

风险2：量子计算机不可靠。Google Sycamore的可靠性约为每个操作99%，这可能对50个量子比特的良好结果来说仍不可靠。我们预计，在项目期间，量子计算机的可靠性将提高，我们可能会获得更好的机器。然而，如果情况不如预期，我们对30个量子比特的模拟结果本身就是有价值的进展。

风险3：关键学生离开项目。我们的项目组有两位教授和两位博士研究生。其中两人是DNA分析的专家，另外两人是量子计算的专家。如果其中一位博士研究生离开项目，这在UCLA很少见，我们将要求其他学生加入并为项目做出贡献。在这种情况下，一位学生可以帮助另一位学生迅速适应。

## 资金和活动总结

### 提案项目的总

成本和持续时间

预算主要用于负责人总共5个月的时间成本，联合负责人总共5个月的时间成本，两位博士研究生2.5年的时间成本，以及一位博士后2年的时间成本。这包括直接成本和相关费用。预算还包括旅行费用和使用量子计算机的费用。我们将在计算后单独添加UCLA的一些间接费用。

总薪金、工资和福利费用为714,790美元。旅行费用为36,000美元，用于整个项目期间。使用量子计算机的费用为175,000美元，用于第三阶段。一旦我们加上用品和费用、计算机服务和相关费用的费用，我们得到总直接费用为973,705美元。对于UCLA的间接费用为381,619美元。总费用为1,355,324美元。

### 按活动划分的预算和时间表

在下表中，所有金额均以1,000美元为单位。为了简化，我们将每个阶段的成本平均分配到各个季度。

|              | 第一阶段 |    |    |    |    | 第二阶段 |    |    | 第三阶段 |    |    |    |    |     总计     |
| :----------: | :------: | :-: | :-: | :-: | :-: | :------: | :-: | :-: | :------: | :-: | :-: | :-: | :-: | :-----------: |
|              |    Q1    | Q2 | Q3 | Q4 | P1 |    Q1    | Q2 | P2 |    Q1    | Q2 | Q3 | Q4 | P3 |              |
| 算法模拟实验 |   118   | 118 | 119 | 119 | 474 |   138   | 138 | 276 |   151   | 151 | 151 | 152 | 605 | 474, 276, 605 |
|     总计     |   118   | 118 | 119 | 119 | 474 |   138   | 138 | 276 |   151   | 151 | 151 | 152 | 605 |     1,355     |

## 提案主体

### 动机

人类常见疾病的大多数已久已知受多种遗传和环境因素的调节。理解这些复杂人类疾病遗传信号的性质——遗传变异对疾病状态的预测能力（遗传性如何）、以及这种遗传性在基因、调控元件和生物途径之间的分布——是人类遗传学长期以来的目标。

除了直接与理解基本疾病病因学相关，了解遗传信号或遗传性对人

类健康的一些问题至关重要。第一个问题是药物发现。药物发现和开发的一个挑战是无法准确预测药物在人体中的疗效（大约90%的候选药物在临床试验中失败）。这种无法预测药物在人体中的疗效的情况导致人们寻找其他证据来决定潜在药物靶点的选择。多项研究已经表明，使用基因信号作为药物靶点的药物获得批准的可能性要大得多（[15]估计这种可能性增加一倍）。一个引人注目的例子是基于对具有自然突变使得该基因失活的个体的人类基因研究开发降低低密度脂蛋白胆固醇水平的PCSK9抑制剂[7]。第二个问题涉及个体化医学，重点是根据个体的遗传信息准确预测其疾病或健康结果。目前正在为多种疾病结果开发这种预测模型，其准确性各不相同。例如，最近的研究表明，这种预测模型在预测冠状动脉疾病风险方面具有临床相关性[14]，而最近的一项工作表明这些预测模型在决定哪些人需要接受前列腺特异性抗原筛查的方面有价值[13]。

寻找疾病遗传信号的工作已经得到了测量数千个个体的数百万个位点的基因变异的能力的革命性改变。基因数据与疾病信息的分析已经发现了数千个与常见疾病相关的遗传变异。这一努力的关键发现之一是大样本量对获得可靠和可重复的遗传关联的重要性。

尽管取得了令人瞩目的进展，发现的遗传关联的预测能力低于理论预期。这种“缺失的遗传性”现象导致遗传学界需要（i）研究更大样本的个体；（ii）利用能够捕获先前无法获取的遗传变异的新技术；（iii）测量多样化的表型集合。这些努力的结果是收集的数据的规模和复杂性（以个体数量、遗传变异和测量的表型数量衡量）显著增加。

例如，英国生物库项目涉及收集来自约50万英国个体的全基因组基因型数据以及成千上万种不同的表型，而其他类似的项目也正在进行中（中国卡多里生物库、日本生物库、芬兰基因组计划、UCLA ATLAS生物库、Vanderbilt大学BioVU生物库、Mount Sinai的BioMe生物库以及美国国立卫生研究院的AllofUs计划）。此外，正在进行额外的工作，以实现在这些多样数据集之间共享数据，充分发挥大规模数据的威力。准确了解人群间的关系（种群结构）对于共享努力至关重要。这是因为由于种群结构引起的基因差异可能会干扰有关疾病遗传性的学习，如果没有准确推断，可能会导致错误的发现。在开发可以推断种群结构并估计遗传性的算法方面，面临着挑战。

虽然我们和其他人已经为这些关键任务开发了许多经典算法，但这些数据集的增长预计会超过这些算法的能力。

### 目标和意义

问题：将DNA分析扩展到未来的数据集。通过比较英国生物库数据集的大小和可能的未来数据集的大小，我们可以对问题的规模有所了解。英国生物库数据集有**488,363 x 500,000个数据点**。该数据集的经典表示几乎为1万亿比特，即1TB。可能的未来数据集可能覆盖整个世界，并包含1150万个单核苷酸多态性（SNP）。因此，该数据集将具有80亿x 1150万个数据点，其经典表示将达到10万TB。我们还可以比较在这些数据集上进行经典计算所需的时间。我们的自然选择算法、疾病的遗传性和疾病发展风险的处理时间分别为30分钟、3小时和51小时，用于处理英国生物库数据集。这些算法的计算时间与数据大小呈线性关系，这意味着对于可能的未来数据集，它们的计算时间将增加100,000倍。因此，我们估计在使用经典计算时，处理规模更大的数据集将需要非常长的时间。如果经典计算是我们能做的最好的，那么我们将错过人类健康应用的洞察力。

我们相信量子计算将为我们处理整个世界的DNA数据集提供所需的可扩展性。此外，我们估计DNA处理所需的逻辑

比特数和电路深度与其他一些应用相比较为适中。具体而言，我们估计量子计算机可以处理具有50个比特和50,000个电路深度的英国生物库数据集。与一些其他应用相比，这是一个较小的量子体积（量子比特数和电路深度的乘积），这将使量子计算机具有优势。特别是，Shor算法、Grover算法和DNA测序所需的量子体积要高得多，如果它们要带来量子优势。如果我们以处理英国生物库数据集的50个比特为基准，通过添加log2 100,000 = 17个比特以及一些辅助比特，我们可以处理一个大约比现有数据集大100,000倍的数据集。

扩展DNA分析的问题中有一个重要的子问题：验证。对于英国生物库数据集来说，量子体积已经足够大，无法通过模拟来进行验证。相反，我们将不得不对数据子集进行量子算法的模拟。然而，其他验证量子电路的方法正在出现，一个问题是这些方法是否可以帮助验证整个数据集的量子算法的某些方面。

目标：我们将用量子算法替换当前的经典算法，如图【2所示。我们的实验数据集仍然是英国生物库数据集，并且我们将得出对健康有用的相同类型的结论。我们将将数据集表示为量子状态，使得量子算法能够处理数据。

图【凤比我们的意图更简单：在每个经典算法中，我们将关键子程序替换为更快的量子子程序。因此，得到的算法将是经典和量子的混合。

图[凤的设计的一个好处是我们可以轻松地比较现有经典算法和新的混合算法的输出。这将有助于我们验证我们的混合算法的正确性。

我们将通过在英国生物库数据集的越来越大的子集上运行经典算法和混合算法来展示可扩展性。我们将记录执行时间，并将其作为输入数据集大小的函数绘制成图表。如果成功，结果将显示混合算法的执行时间增长较慢。这意味着对于更大的数据集，经典计算将变得不可行，而混合计算将成功。

意义：我们对可扩展性的演示将是朝着从未来更大数据集中得出新结论的关键一步。这些结论将对健康领域有用。

量子计算领域正在寻找能够让量子计算机优于经典

计算机的有用应用。迄今为止，这些应用需要大量的量子比特，这些比特在遥远的未来才能获得。我们估计DNA分析是一个例子，它可以在较小数量的量子比特下获得量子优势。事实上，一些现在的量子计算机已经提供了我们进行DNA分析所需的50-70个量子比特。如果我们还想添加纠错来获得50,070个完美的量子比特，我们只需要少于50,000-70,000个量子比特，而这可能会在本十年内实现。总之，我们认为DNA分析是一个应用领域，其中量子算法将革命性地提高我们可以处理的数据集的规模。

图【3显示了我们于2023年5月31日在UCLA的研究团队。

### 我们的团队和初步调查

我们的研究团队由8人组成，如图[3所示]：

- Abdulrahman Sahmoud（亚马逊AWS量子计算中心高级软件工程师，位于最左侧），
- Sriram Sankararaman（共同负责人，最左边第二位），
- Jens Palsberg（负责人，最左边第三位），
- Payal Kaushik（物理学研究生，最左边第四位），
- Shane Woods（物理学研究生，最右边第四位），
- Ali Pazoki（计算医学研究生，最右边第三位），
- Jeffrey Ma（计算机科学研究生，最右边第二位），
- Yin Huang（物理学研究生，最右边）。

Yin Huang、Payal Kaushik、Jeffrey Ma和Shane Woods都参加过Jens Palsberg关于量子编程和量子算法的课程。作为课程的一部分，他们学习了许多量子算法并在量子硬件上运行了这些算法，他们每个人都构建了一个量子电路模拟器，并学习了量子计算的基础知识。Ali Pazoki是DNA分析的经典算法专家。

今年春天，我们的重点是对现有经典算法进行共同理解，了解如何将数据集映射到单位矩阵和量子状态，并掌握我们所需的量子算法。特别是，我们进行了数据加载的实验，主要是通过手动设计适当的电路。我们还通过在微基准测试上运行量子算法进行了实验，以确保它们按预期工作。

我们的初步调查为我们提出的研究提供了信息，我们将在下文中解释。

### 提出的研究：算法

数据集。我们从一个虚构的包含四个个体和四个SNP的数据开始。目标是展示我们如何组织数据并解释数据的含义。稍后，我们还将使用这些数据来展示我们将如何进行数据加载。下面的矩阵$A$包含了数据：

```
A = 
2 0 1 2
1 0 2 2
1 2 2 1
2 2 2 2

这行包含了SNP 1的数据
这行包含了SNP 2的数据
这行包含了SNP 3的数据
这行包含了SNP 4的数据

每个个体占据一列
```

在上面的矩阵$A$中，每个SNP对应一行，每个个体对应一列。$A$的每个元素都是0、1或2中的一个。请

注意，在第一行的第三列中，元素是0。这意味着对于表示在第三列的个体，对于SNP 1，与父母相比没有发生变异。相反，对于表示在第一列的个体，对于SNP 1，元素是2，因此与父母都发生了变异。然而，对于表示在第二列的个体，对于SNP 1，元素是1，所以与父母之一相比只发生了单一变异，而不是两者都有。

让我们更详细地看一下UK Biobank数据集，具体来说是针对291,273个个体（列）基因分型的454,207个SNP（行）。我们统计了SNP和个体中0、1、2的数量。以下是摘要统计信息：

|              | 每行包含 |          |          | 每列包含 |          |          |
| :----------- | -------: | -------: | -------: | -------: | -------: | -------: |
|              | $\# 0$ | $\# 1$ | $\# 2$ |       协 | $\# 1$ | $\# 2$ |
| 最小值       |        7 |    5,634 |   72,296 |   12,766 |   71,872 |  355,850 |
| 第一四分位数 |      189 |   14,497 |  196,420 |   14,089 |   80,345 |  359,081 |
| 中位数       |      912 |   30,785 |  259,571 |   14,219 |   80,645 |  359,342 |
| 均值         |    9,121 |   51,708 |  230,444 |   14,223 |   80,632 |  359,351 |
| 第三四分位数 |    9,294 |   85,557 |  276,586 |   14,351 |   80,947 |  359,599 |
| 最大值       |   73,262 |  147,164 |  285,612 |   16,511 |   84,164 |  368,963 |

请注意，我们的示例矩阵$A$中的0、1和2的频率与上面的表一致：较少的0、更多的1和较多的2。

不失一般性，我们可以选择一种表示方式，使0的数量最大化。对于这个数据集，我们将0和2互换，以获得更多的0。（在该领域的行话中，这种变化可以描述为将主等位基因与次等位基因互换。）

一旦我们进行了互换，UK Biobank数据的矩阵中将包含79％的零。然而，虽然列中的零的数量变化不大，但行中的零的数量差异很大。特别地，其中一行只包含72,296个零。因此，该矩阵是稀疏的，并且列是稀疏的，但是一些行远非稀疏。这个观察结果将在我们估计量子算法所需的量子比特数和电路深度时起关键作用，见下文。数据加载。主要负责人：Payal Kaushik。

让我们再次考虑上面的$4 \times 4$矩阵$A$，并将0与2互换，如上所述。结果是以下矩阵$B$：

```
B = 
0 2 1 0
1 2 0 0
1 0 0 1
0 0 0 0
```

为了进行量子处理，我们需要以两种不同的方式表示矩阵$B$：作为一个单位矩阵和一个量子态。这是因为其中一个量子算法需要将数据表示为单位矩阵，而另外两个算法则使用量子态。我们接下来描述我们实现这一目标的方法。

让我们首先考虑如何将$B$表示为一个单位矩阵。我们可以看到$B$不是单位矩阵，至少有两个原因。首先，行和列不是单位向量，因此$B$不是单位矩阵。其次，$B$的一行是0，这意味着$B$不可逆，因此$B$不是单位矩阵。然而，我们可以对$B$进行块编码，将$B$作为一个较大的单位矩阵的一个块放置其中。这使得量子算法可以在较大矩阵上工作，并在此过程中对$B$做正确的处理。

进行块编码的第一步是缩放$B$，使得较大矩阵的行和列成为单位向量。如果我们将$B$缩放为$\frac{1}{4}$，我们就可以达到这个目标。让我们将缩放后的矩阵称为$C=\frac{1}{4} B$。

第二步是将$C$作为一个单位矩阵$U$的一个块放置：

```
U = 
C *
* *
```

Gilyen、Su、Low和Wiebe [9，Lemma 48]展示了如何对稀疏矩阵$C$进行良好近似的$U$。Camps等人的最近论文[5，I]进一步研究了如何有效地对某些稀疏矩阵进行块编码。构建矩阵$C$的块编码的电路结构如下所示：

（这里有一个电路图，在图中无法显示，请参考原文）

在上面的电路图中，$m$满足$s=2^m$，其中$s$是任何行或列中非零元素的最大数量，$|j\rangle$编码列编号，$V$和$W$编码对$C$中数据的访问。主要挑战是生成具有小深度的电路$V$和$W$。我们将使用[22]论文中的技术来实现这一点，该论文展示了如何对类似我们的矩阵（仅包含0、1和2等三个不同值）进行高效的块编码。具体而言，对于一个大小为$2^n$的数据集，[22]中的方法需要$2n+2$个量子比特和深度为$O(n^2)$的电路。

对于UK Biobank数据集，我们上面看到经过0和2互换的转换矩阵是稀疏的，尽管一些行有很多非零元素。为了简单起见，我们需要使矩阵是方阵。为了进一步简化，我们需要行数为2的幂。鉴于UK Biobank数据集包含了关于488,363个个体的数据，我们将关注$2^{18}$行，因为$2^{18}=262,144$。因此，我们将选择$2^{18}$个个体和$2^{18}$个SNP，并形成一个大小为$\left(2^{18} \times 2^{18}\right)$的数据矩阵。对于我们的$\left(2^{18} \times 2^{18}\right)$矩阵的块编码，我们将需要$(2 \times 18)+2=38$个量子比特和估计深度为6,000的电路。

现在让我们将矩阵$B$表示为一个量子态。基本方法是使用**幅度编码**，将矩阵的元素表示为量子态的振幅。然而，生成这样的编码可能需要**指数深度**的电路。我们将使用最近的改进方法，称为**近似幅度编码**[II]。其思想是训练一个参数化的量子电路$U(\theta)$，其中$\theta$是参数列表，使得$U(\theta)|0^n\rangle$产生数据的近似幅度编码。论文[19]展示了这种方法可以在$O(n^2)$的电路深度下取得成功。

训练阶段需要进行多次测量，其中一次测量是量子电路的单次运行。我们将尝试几种技术来变化和优化参数。

### 自然选择。主要负责人：Jeffrey Ma。

对于计算主成分，我们使用**标准化后的矩阵$A$**。我们了解到两篇关于量子主成分分析的论文[I7，I]。

目标是编写一个以量子比特数量为参数的实现，对具有不同量子比特数量的实例进行模拟，并撰写一份关于研究结果的报34告。这种方法的可扩展性如何？一个关键目标是识别问题和障碍，然后解决和克服它们，或者提出为什么需要更多的工作的论据。如果我们发现了与算法问题相关或有帮助的其他论文，请引用并分享。我特别想知道在输入大小为$n$的情况下，所需的**量子比特数**是否是$O(\log n)$，而所需的**电路深度**是否是$O((\log n)^2)$或类似的。让我们拭目以待！疾病的遗传性。

### 主要负责人：Yin Huang。

我们正在计算从给定矩阵**派生的矩阵**的迹，具体步骤如下：

$$
\begin{array}{rlrl}
\text { 步骤 1: } & A & =\text { 给定的 } 0,1,2 \text { 矩阵 } \\
\text { 步骤 2: } & X & =\text { 矩阵 } A \text { 的标准化版本 } \\
\text { 步骤 3: } & K & =(1 / \# \mathrm{SNP}) X \times X^{T} \\
\text { 步骤 4: } & S & =K \times K \\
\text { 步骤 5: 结果 } & =\operatorname{trace}(S)
\end{array}
$$

步骤3的复杂度为$O(N^2M)$，其中$N$是个体的数量，$M$是SNP的数量；计算迹的复杂度为$O(N^2)$。当前数据集的$N$为$10^5-10^6$，$M$为$10^6-10^7$，而未来的数据集将具有$N=10^9$和$M=10^8-10^9$。

我们了解到一篇关于量子迹估计的论文[18，Lemma 31]。主要问题是我们是否可以使用[18，Lemma 31]中的技术来估计迹，或者我们需要一种算法的变体。目标是在使用合理的资源量的情况下得到迹的估计值。还请阅读上述自然选择部分（红色和蓝色文字）。

### 发展疾病的风险。主要负责人：Shane Woods。

对于计算非负矩阵分解，我们使用矩阵$A$本身。我们了解到一篇关于量子非负矩阵分解的论文$[8]$。

还请阅读上述自然选择部分（红色和蓝色文字）。

其目标是编写一个以量子位数参数化的实现，对不同数量量子位的实例进行模拟，并编写一份关于发现的报告。这种方法的规模很好吗？一个关键的目标是识别问题和障碍，然后解决和克服它们，或者争论为什么需要做更多的工作。如果我们发现了更多与算法问题相关的论文或其他有用的论文，请引用它们并分享它们。我特别感兴趣的是，经典和量子之间的来回是否是实现的重要组成部分。

目标是编写一个以量子比特数量为参数的实现，对具有不同量子比特数量的实例进行模拟，并撰写一份关于研究结果的报34告。这种方法的可扩展性如何？一个关键目标是识别问题和障碍，然后解决和克服它们，或者提出为什么需要更多的工作的论据。如果我们发现了与算法问题相关或有帮助的其他论文，请引用并分享。

我希望有一个清晰的说明，即要求的**量子位的数量**和要求的**电路深度**，两者都用输入的大小来表示。我的希望是，对于大小为n的输入，所需的量子位数是是$O(\log n)$，而所需的电路深度是$O((\log n)^2)$，或类似的东西。我们会看到的！

##### 疾病发展风险。我们提出了一个经典算法[6]，可以推断人群结构，了解个体基因组的复杂祖先起源，从而提高我们对根据遗传祖先而变化的疾病风险的理解。我们的算法处理UK Biobank数据集需要51小时的时间。

我们算法的主要步骤是找到一个**非负矩阵分解**，即使用只有非负元素的矩阵进行分解。我们可以用已知的量子非负矩阵分解算法[8]替换这一步骤。量子非负矩阵分解的主要步骤是**哈密顿模拟**和**相位估计**。对于可以用$n$个量子比特表示的数据，该算法执行$n$次哈密顿模拟，然后进行一步相位估计。我们计划通过**Trotter方法**进行**哈密顿模拟**，这引发了一个问题，即我们需要多少个时间步骤才能得到一个好的分解。我们的假设是，使用电路深度为$O(n^{2})$的足够多的时间步骤。该算法需要$O(n)$个辅助量子比特。

##### Trotterization


Trotterization是一个在量子计算中常用的方法，它可以将连续时间演化的哈密顿量（Hamiltonian）转化为可以在量子电路中实现的离散门序列。这种方法的名称来自于物理学家Hugh F. Trotter，他在1959年的一篇论文中首次提出了这种方法。

Trotter公式（或称为Trotter分解）是物理学中的一个重要概念，它表明，如果你有两个不对易的算符A和B（也就是说，它们的对易子AB-BA不为零），那么你无法直接计算指数形式的这两个算符之和，例如$e^{t(A+B)}$，但是你可以通过Trotter公式将它近似为如下形式：

$$
e^{t(A + B)} = \lim_{n\to\infty} (e^{tA/n} e^{tB/n})^n
$$

在量子计算中，Trotterization方法被广泛用于将连续时间演化的哈密顿量转化为离散门序列。例如，如果你有一个哈密顿量$H = H_1 + H_2$，并且你想要执行时间t的演化$e^{-itH}$，那么Trotterization方法可以让你用离散的量子门（例如，$e^{-itH_1/n}$ 和 $e^{-itH_2/n}$）来近似这个连续时间演化。

Trotterization方法的一个重要应用是在量子相位估计（Quantum Phase Estimation，QPE）和量子化学模拟中，这两种应用都需要处理时间演化的哈密顿量。


### 提议的研究：模拟

通过Amazon Braket进行模拟。我们希望能够从电路模拟无缝转向使用量子计算机。我们将通过Amazon Braket实现这一目标。我们首先注意到，对于少于18个量子比特的电路模拟，我们可以在笔记本电脑上运行。对于18-34个量子比特的电路模拟，我们可以使用SV1模拟器。电路深度没有限制，但运行时间有限制：6小时。Braket网站报告称，一个$34 \times 34$的电路需要1-2小时才能执行，这给出了电路深度的实际限制。对于34-50个量子比特的电路模拟，我们可以使用TN1模拟器。这个模拟器的电路深度限制为1,000，它的性能可能好也可能差，这有待观察。

与真实结果的比较。图⿴囗口说明了为什么我们可以将模拟结果与真实结果进行比较。真实结果可以在我们的论文中找到，是通过在UK Biobank数据集上运行我们的经典算法获得的，这是图中的上路径。我们对UK Biobank数据集进行量子算法的模拟是图中的下路径。我们可以比较这两种方法找到的特征向量、迹和非负矩阵分解，并确定它们之间的相似性。此外，我们还可以比较对健康保健有用的总体结论，并确定它们之间的相似性。我们将定义相似性度量并自动化比较过程。

我们预计，模拟和与真实结果的比较将揭示出一些错误。这些错误可能存在于我们加载数据和实现量子算法的过程中。我们认为项目的第二阶段是一个至关重要的阶段，在这个阶段我们将修复和调优我们的实现，使其具有高质量。在第二阶段结束时，我们将获得具有30个量子比特的电路的模拟结果，这些结果与经典算法产生的结果相匹配。这将使我们相信这些算法在更多量子比特情况下的工作效果仍然良好。

调试。如果我们模拟量子算法并得到一个意外的结果，我们将详细说明我们将采取的步骤。问题是：我们如何知道出了什么问题？我们可以让模拟器打印中间状态，但前提是我们知道期望的结果。为了解决这个问题，我们将我们的期望以关于某些状态的断言的形式写下来。现在，我们可以检查这些状态是否满

足断言，随着模拟的进行。如果模拟达到一个断言失败的状态，我们就知道问题出现在之前。事实上，问题很可能出现在最后一个成功的断言和第一个失败的断言之间。

我们计划进一步推动使用断言进行调试的思想。这个想法是限制我们可以编写的断言的类型，并且作为回报，获得超出模拟的调试支持。具体来说，我们使用投影作为我们的断言，这使我们能够使用Li等人[16]和Yu和Palsberg [24]的两种最新技术。Li等人[16]的技术支持在量子计算机上运行时的断言检查。相比之下，Yu和Palsberg [24]的技术支持在没有模拟和没有使用量子计算机的情况下进行断言检查。在这两种情况下，断言检查的规模远远超过我们可以模拟的电路大小。

### 提议的研究：实验

通过Amazon Braket进行访问。我们为通过Amazon Braket访问量子计算机预算了175,000美元。目前，Amazon Braket提供的最佳选择是名为Aspen-M-3的Rigetti量子计算机，拥有79个量子比特。对于这台量子计算机，175,000美元的预算将给我们提供5亿次测量。

在为期一年的第三阶段中，我们希望将这5亿次测量均匀分布在50个工作周内，每周1000万次测量。Aspen-M-3的相干时间为20微秒[2]。因此，理论上每次耗时20微秒的1000万次测量可以在200秒内执行完毕。然而，开始新测量的时间远远超过测量本身的执行时间。我们从Amazon的同事那里听说，在2023年夏季推出的一种版本中，可以在17分钟内执行1000万次测量。

这使我们设计了第三阶段每周的以下工作周期：

1. 准备新的实验（一周的大部分时间），
2. 进行实验（少于一个小时），最后
3. 从实验中学习（剩余时间）。

这将最大限度地发挥我们对量子计算机的访问价值。

优化。我们估计，一台量子计算机可以处理具有50个量子比特和50,000个电路深度的UK Biobank数据集。然而，Aspen-M-3只能处理最多500个电路深度的电路。虽然我们希望能够访问比Aspen-M-3更好的量子计算机，但我们也将优化我们的量子电路以减少其深度

。我们意识到无法预测第三阶段将有哪些量子计算机可用或它们将具备哪些门集。因此，我们将使用我们自己的量子电路超级优化工具Quartz [2:3]。Quartz可以自动生成和验证适用于任意量子门集的电路转换。对于给定的门集，Quartz通过系统地探索小电路来生成候选电路转换，并使用自动定理证明器验证发现的转换。为了优化量子电路，Quartz使用基于成本的回溯搜索将经过验证的转换应用于电路。我们的实验证明，Quartz能够优化各种门集的广泛范围的电路，性能优于或与手动调优的电路优化器相匹配。对于Rigetti门集，Quartz平均减少了49％的门数。我们将设计和实现Quartz的更激进版本，以进一步减少门数。

可扩展性。我们将设计一系列越来越大的UK Biobank数据集的子集。为简单起见，在每个子集中，个体数量将等于SNP数量。因此，每个子集可以用一个大小为$2^{i} \times 2^{i}$的矩阵表示，其中$2 \leq i \leq 18$。因此，第$(i+1)$个数据集比第$i$个数据集大4倍。这将使我们能够在对数尺度的x轴上绘制数据大小的结果，并在线性尺度的y轴上绘制执行时间。目标是获得形成直线的数据点，这将表明当我们将数据大小翻倍时，执行时间呈线性增长。

## 关键人员简介、设施/资源

Jens Palsberg。研究领域：编程语言、软件工程、量子计算。项目：NJR：Java资源的规范化；关于Java内存模型的推理；量子程序的验证和优化。

教育背景。

MBA，加州大学洛杉矶分校安德森管理学院，2017年

博士，计算机科学，丹麦奥胡斯大学，1992年

硕士，计算机科学和数学，丹麦奥胡斯大学，1988年

工作经历。

2003年至今，加州大学洛杉矶分校教授。

2010年至2015年，加州大学洛杉矶分校计算机科学系主任。

2005年至2007年，加州大学洛杉矶分校计算机科学系研究生副主任。

2002年至2003年，普渡大学教授

兼副系主任。

1996年至2002年，普渡大学副教授。

1995年至1996年，麻省理工学院访问科学家。

1993年至1994年，东北大学访问助理教授。

近五年的发表论文。

a. Mingkuan Xu, Zikun Li, Oded Padon, Sina Lin, Jessica Pointing, Auguste Hirth, Henry Ma, Jens Palsberg, Alex Aiken, Umut A. Acar, Zhihao Jia. Quartz: superoptimization of Quantum circuits. PLDI 2022, 国际程序设计语言设计与实现会议, 2022年。

b. Akshay Utture, Shuyang Liu, Christian Gram Kalhauge, Jens Palsberg. Striking a Balance: Pruning False-Positives from Static Call Graphs. In ICSE'22, 国际软件工程会议, 2022年。

c. Akshay Utture, Jens Palsberg. Fast and Precise Application Code Analysis using a Partial Library. In ICSE 2022, 国际软件工程会议, 2022年。

d. Nengkun Yu, Jens Palsberg. Quantum abstract interpretation. In PLDI'21, ACM程序设计语言设计与实现会议, 2021年。

e. Christian Gram Kalhauge, Jens Palsberg. Logical bytecode reduction. In PLDI'21, ACM程序设计语言设计与实现会议, 2021年。

五项协同活动。

a. 加州大学洛杉矶分校-亚马逊人工智能与人类科学中心主任，2021年至今。

b. 担任22个国家科学基金会（NSF）审查小组的成员。

c. 作为ACM执行委员会的成员，2020年至今，成功推动特别兴趣小组在2022财年对ACM的一项附加费用减免，考虑到疫情的影响。

d. 作为普渡大学计算机科学博士教育的一部分，以平稳和低成本的方式将形式审查的原则和实践纳入课程。

e. 创建了一个供普渡大学本科编译器课程使用的项目，并基于此合著了Andrew Appel的《现代编译器实现（Java版）》教材的修订版。

Sriram Sankararaman。我是一名计算生物学家，广泛研究开发统计和机器学习模型，以理解基因组和生物医学数据之间的联系。我的实验室开发新颖的统计和计算工具，并将这些工具应用于分析大规模基因组数据集，以探索进化、基因和性状之间的关系。

教育背景。

2010年至2015年，哈佛

医学院遗传学系博士后研究员。

2004年至2010年，加州大学伯克利分校计算机科学博士。

2000年至2004年，印度理工学院马德拉斯分校计算机科学与工程学士。

工作经历。

2021年至今，加州大学洛杉矶分校副教授；计算机科学、计算医学、人类遗传学系。

2015年至2021年，加州大学洛杉矶分校助理教授。

2011年至2015年，哈佛医学院遗传学系博士后研究员。

荣誉。

2022年中国-美国工程前沿研讨会邀请参与者，美国国家工程院。

2021年阿拉伯-美国前沿研讨会邀请参与者，美国国家科学院。

2020年微软研究员奖。

2020年国家科学基金会职业奖。

2019年加州大学洛杉矶分校优秀教学奖。

2017年加州大学洛杉矶分校Hellman Fellow。

2017年阿尔弗雷德·P·斯隆学者。

2017年Okawa基金会奖。

2015年美国人类遗传学协会学员研究奖的半决赛选手。

2014年NIH K99/R00独立之路奖。

2014年伯克利理论计算研究所学者。

2012年哈佛人类过去科学倡议学者。

近五年的发表论文。

a. Chiu等人。在生物库规模的基因组数据中推断人群结构，美国人类遗传学杂志（2022）。

b. Wu等人。对生物库规模数据进行快速遗传相关性估计，美国人类遗传学杂志（2021）。

c. Agrawal、Chiu等人。用于大规模遗传变异数据的可扩展概率主成分分析，PLoS遗传学杂志（2020）。

d. Pazokitoroudi等人。跨百万基因组的高效变体成分分析，自然通讯（2020）。

e. Durvasula和Sankararaman。在非洲人群中恢复幽灵古老内插的信号，科学进展（2020）。

设施/资源。我们在加州大学洛杉矶分校拥有足够的设施来进行项目。我们的学生和博士后的实验室位于Palsberg和Sankararaman的实验

室。

我们将通过Amazon Braket访问量子电路模拟器和量子计算机。```

## 商业化/合作伙伴策略

我们的研究团队由UCLA和亚马逊AWS量子计算中心的成员组成。我们的目标是充分利用AWS提供的经典计算资源和Amazon Braket提供的量子计算资源。这有以下三个主要优势：

- AWS是一个强大且经济实惠的资源，可用于运行量子电路模拟器。
- Amazon Braket提供了访问许多量子计算机的机会，我们预计在第3阶段开始时，还会有其他可访问的量子计算机。
- AWS提供了从量子电路模拟到在量子计算机上运行电路的无缝路径。这对于我们的大规模实验来说是一个重要的优势。

以下是Amazon Braket已经提供访问的一些量子计算机的示例。

| 设备                           | 量子比特数 | 每次运行的价格 |
| :----------------------------- | ---------: | :------------- |
| Rigetti - Aspen-M-3            |         80 | $\$ 0.00035$ |
| IonQ - Aria 1                  |         25 | $\$ 0.01$    |
| IonQ - Harmony                 |         11 | $\$ 0.03$    |
| Oxford Quantum Circuits - Lucy |          8 | $\$ 0.00035$ |

上表显示，Amazon Braket已经提供了访问量子计算机的机会，其量子比特数足够满足我们的需求。Aspen-M-3的一个主要关注点是其相干时间：我们希望在第3阶段时，Amazon Braket能提供一个量子计算机，既具有50个以上的量子比特，又具有更长的相干时间。

负责人Palsberg教授在另一个方面与Amazon AWS有良好的联系。具体来说，他是UCLA-亚马逊人类和人工智能科学中心的主任。该科学中心的使命是通过跨学术和工业研究的相互交流，利用人工智能的力量解决人类紧迫的挑战。科学中心已经在UCLA的研究人员和亚马逊的研究人员之间建立了许多联系。同样地，我们在量子分析人类DNA的项目，正如本提案中所描述的，是UCLA和亚马逊之间的联系。随着项目的推进，我们希望能有更多的亚马逊人员参与进来。

目前我们还没有商业化策略。负责人Palsberg教授既有强大的发表记录，也有专利记录，发表了180多篇论文和获得了3项美国专利。我们目前的计

划是发表我们的发现并将我们的软件以开源方式提供。然而，我们也愿意与商业实体进行对话，并保留根据我们的发现成立初创公司的可能性。

## 详细项目活动、进度和预算

### 项目活动和进度

第1阶段：算法（1年）。第2阶段：模拟（0.5年）。第3阶段：实验（1年）。

### 预算和预算说明

我们在下表中列出了预算。

UCLA的财政年度为7月1日至6月30日。教师和其他高级人员的日历工作量也在这个期间内进行。对于在学术岗位上的教师，承诺的工作量可能包括学年期间（10月1日至6月30日）和/或暑期（7月1日至9月30日）的工作量。工资按照每年3%的涨幅进行调整。

负责人：Jens Palsberg教授。负责人提议以下工作量：第1阶段2个月，第2阶段1个月，第3阶段2个月。负责人将领导研究并监督整个项目。负责人还将为研究生研究员和博士后研究员提供指导。Palsberg教授每个夏季月份的工资是$\$26,511.11$。

副负责人：Sririm Sankararaman教授。副负责人提议以下工作量：第1阶段2个月，第2阶段1个月，第3阶段2个月。副负责人将领导研究的子任务，并为研究生研究员提供指导。Sankararaman教授每个夏季月份的工资是$\$25,344.45$。

研究生研究员。该项目拟聘请两名研究生研究员。工作量安排如下：第1年和第3年：9个学术月份50%，3个暑期月份50%；第2年：4个学术月份50%，2个暑期月份50%。研究生研究员将与负责人和副负责人密切合作，进行拟议研究方向的工作。研究生研究员的薪水按照每月$\$6,861$的100%薪酬比例支付。

博士后研究员。该项目拟聘请一名博士后研究员。工作量安排如下：第1阶段7个月（从202

4年1月1日开始），第2阶段6个月，第3阶段12个月。博士后的薪水计算如下：第1年：$\$5,000/\mathrm{月}$；第2年：$\$5,185/\mathrm{月}$；第3年：$\$5,376.83/\mathrm{月}$，根据FY $2023/2024$的核准薪酬率。

博士后研究员将与负责人、副负责人和研究生研究员密切合作，完成拟议研究的里程碑。博士后研究员将在第1阶段的后半部分整合量子算法，扩展模拟（第2阶段），并领导实验工作（第3阶段）。总工资、薪金和福利。对于负责人、副负责人、研究生研究员和博士后研究员，总工资和薪金为$\$567,460$。加上员工福利后，该预算项目的总费用为$\$714,790$。

差旅费。整个项目周期为$\$36,000$。差旅经费用于支付负责人或研究生参加该项目的国内同行评审会议和国内专业会议的费用。

访问量子计算机。第3阶段为$\$175,000$。我们将通过Amazon Braket访问量子计算机。目前，Amazon Braket提供的最佳选择是一台名为Aspen-M-3的Rigetti量子计算机，拥有79个量子比特。在Aspen-M-3上运行的价格由以下公式给出：

$$
\text{总价格} = \text{运行次数} \times \text{每次运行的价格}
$$

我们估计需要运行5亿次。在Aspen-M-3上每次运行的价格为$\$0.00035$。因此，我们得到的总价格为

$$
\text{总价格} = 5 \times 10^8 \times \$0.00035 = \$175,000
$$

因此，我们预算了$\$175,000$用于通过Amazon Braket访问量子计算机。

材料和费用。整个项目周期为$\$24,000$。请求购买与项目相关的软件/硬件（笔记本电脑/台式机）和其他项目特定的杂项物品。

计算机服务。整个项目周期为$\$12,796$。计算机（ADPE）服务是提供与计算机科学系共享网络服务的计算机网络服务。ADPE服务将维护全功能计算环境，以支持研究和机构。网络服务费用为每人每月$\$124$。

技术基

础设施费用。整个项目周期为$\$2,948$。

一般和雇佣责任费用（GAEL）。整个项目周期为$\$8,172$。

总直接成本。将之前的所有预算项目相加，得出总直接成本为$\$973,705$。

间接费用（设施和行政费用）。整个项目周期为$\$381,619$。间接费用基于一个截至日期为2018年10月12日的联邦协商协议。校园内研究的费率目前为FY $23/24$为57%，FY $24/25$为57.5%。新的间接费用率协议日期为2023年3月28日。

![预算表格](https://cdn.mathpix.com/cropped/2023_06_10_dafc0691c19d9a8bb6a6g-23.jpg?height=2128&width=1619&top_left_y=264&top_left_x=253)

## 参考文献

[1] FABLE: Fast Approximate Quantum Circuits for Block-Encodings. In 2022 IEEE International Conference on Quantum Computing and Engineering (QCE), 2022.

[2] Aspen-M-3 Quantum Processor. Accessed on Jun 3, 2023.

[3] Aman Agrawal, Alec M. Chiu, Minh Le, Eran Halperin, and Sriram Sankararaman. Scalable Probabilistic PCA for Large-Scale Genetic Variation Data. PLOS Genetics, May 2020.

[4] C. Bycroft, C. Freeman, D. Petkova, G. Band, L.T. Elliott, K. Sharp, A. Motyer, D. Vukcevic, O. Delaneau, J. O'Connell, and Et Al. The UK Biobank Resource with Deep Phenotyping and Genomic Data. Nature, (562):203-209, 2018.

[5] Daan Camps, Lin Lin, Roel Van Beeumen, and Chao Yang. Explicit Quantum Circuits for Block Encodings of Certain Sparse Matrices. 2022.

[6] Alec M. Chiu, Erin K. Molloy, Zilong Tan, Ameet Talwalkar, and Sriram Sankararaman. Inferring Population Structure in Biobank-Scale Genomic Data. American Journal of Human Genetics, 109(4):727-737, 2022.

[7] Jonathan Cohen, Alexander Pertsemlidis, Ingrid K Kotowski, Randall Graham, Christine Kim Garcia, and Helen H Hobbs. Low LDL cholesterol in individuals of African descent resulting from frequent nonsense mutations in PCSK9. Nature Genetics, $37(2): 161-165,2005$.

[8] Yuxuan Du, Tongliang Liu, Yinan Li, Runyao Duan, and Dacheng Tao. Quantum Divide-and-Conquer Anchoring for Separable Non-Negative Matrix Factorization. In Proceedings of the 27 th International Joint Conference on Artificial Intelligence, pages 2093-2099. AAAI Press, 2018.

[9] Andras Gilyen, Yuan Su, Guang Hao Low, and Nathan Wiebe. Quantum Singular Value Transformation and Beyond: Exponential Improvements for Quantum Matrix Arithmetics. In Proceedings of the 51st Annual ACM SIGACT Symposium on Theory

 of Computing (STOC 2019), pages 193-204, 2019.

[10] Max Hunter Gordon, M. Cerezo, Lukasz Cincio, and Patrick J. Coles. Covariance Matrix Preparation for Quantum Principal Component Analysis. PRX Quantum, (3), 2022.

[11] Chen He, Jiazhen Li, Weiqi Liu, and Jane Wang. A Low Complexity Quantum Principal Component Analysis Algorithm. IEEE Transactions on Quantum Engineering, 2021.

[12] Alan Ho and Dave Bacon. Announcing Cirq: An open source framework for NISQ algorithms. Google AI Blog; Google AI Quantum Team; https://ai.googleblog. com/2018/07/announcing-cirq-open-source-framework.html, June 2018.

[13] Linda Kachuri, Thomas J Hoffmann, Yu Jiang, Sonja I Berndt, John P Shelley, Kerry Schaffer, Mitchell J Machiela, Neal D Freedman, and Wen-Yi Huang et al. Genetically adjusted psa levels for prostate cancer screening. Nature Medicine, 2023. [14] Amit V Khera, Mark Chaffin, Krishna G Aragam, Mary E Haas, Carolina Roselli, Seung Hoan Choi, Pradeep Natarajan, Eric S Lander, Steven A Lubitz, Patrick T Ellinor, and et al. Genome-wide polygenic scores for common diseases identify individuals with risk equivalent to monogenic mutations. Nature Genetics, 50(9):1219-1224, 2018.

[15] Emily A King, J Wade Davis, and Jacob F Degner. Are drug targets with genetic support twice as likely to be approved? revised estimates of the impact of genetic support for drug mechanisms on the probability of drug approval. PLoS Genetics, $15(12), 2019$.

[16] Gushu Li, Li Zhou, Nengkun Yu, Yufei Ding, Mingsheng Ying, and Yuan Xie. Projection-based runtime assertions for testing and debugging quantum programs. Proc. ACM Program. Lang., 4(OOPSLA), November 2020.

[17] Seth Lloyd, Masoud Mohseni, and Patrick Rebentrost. Quantum Principal Component Analysis. Nature Physics, 10:631-633, 2014.

[18] Alessandro Luongo and Changpeng Shao. Quantum Algorithms for Spectral Sums. 2020.

[19] Kouhei Nakaji, Shumpei Uno, Yohichi Suzuki, Rudy Raymond, Tamiya Onodera, Tomoki Tanaka, Hiroyuki Tezuka, Naoki Mitsuda, and Naoki Yamamoto. Approximate amplitude encoding in shallow parameterized quantum circuits and its application to financial market indicators. Phys. Rev. Res., 4, May 2022.

[20] Matthew R Nelson, Hannah Tipney, Jeffery L Painter, Judong Shen, Paola Nicoletti, Yufeng Shen, Aris Floratos, Pak Chung Sham, Mulin Jun Li, Junwen Wang, and et al. The support of human genetic evidence for approved drug indications. Nature Genetics, $47(8): 856-860,2015$.

[21] Ali Pazokitoroudi, Yue Wu, Kathryn S. Burch, Kangcheng Hou, Aaron Zhou, Bogdan Pasaniuc, and Sriram Sankararaman. Efficient Variance Components Analysis Across Millions of Genomes. Nature Communications, 11, 2020.

[22] Christoph Sünderhauf, Earl Campbell, and Joan Camps. Block-encoding Structured Mat

rices for Data Input in Quantum Computing. 2023.

[23] Mingkuan Xu, Zikun Li, Oded Padon, Sina Lin, Jessica Pointing, Auguste Hirth, Henry Ma, Jens Palsberg, Alex Aiken, Umut A. Acar, and Zhihao Jia. Quartz: Superoptimization of Quantum Circuits. In Proceedings of PLDI'22, ACM SIGPLAN Conference on Programming Language Design and Implementation, pages 625-640, June 2022.

[24] Nengkun Yu and Jens Palsberg. Quantum Abstract Interpretation. In Proceedings of PLDI'21, ACM SIGPLAN Conference on Programming Language Design and Implementation, June 2021.

# Quantum Analysis of Human DNA that Scales to the Entire World

June 12,2023

Response to the Wellcome Leap Solicitation for Quantum for Bio (Q4Bio) by

Principal Investigator:

Organization:

Telephone:

Email:

with:

Co-Principal Investigator:

Organization:

Telephone:

Email:

Jens Palsberg `<br>`University of California, Los Angeles (UCLA)`<br>`$310-938-8050$`<br>`palsberg@ucla.edu

## Sriram Sankararaman

University of California, Los Angeles (UCLA)

$510-813-9888$

sriram.sankararaman@gmail.com

Total Funds Proposed: $\$ 1,355,324$ Total Duration of Proposed Work: 2.5 years.

Business Contact:

Department:

Organization:

Telephone:

Email: Lien Pham

Office of Contract and Grant Administration University of California, Los Angeles (UCLA) $424-259-5934$

lien.pham@research.ucla.edu

Jens Palsberg is a Professor of Computer Science at UCLA. He is an associate editor of ACM Transactions on Quantum Computing and in 2023 he received the Eon Instrumentation Excellence in Teaching Award at UCLA for his courses on quantum computing.

Sriram Sankararaman is a Professor of Human Genetics, Computational Medicine, and Computer Science at UCLA. He is on the editorial board of Journal of Computational Biology and in 2020 he received an NSF Career award.

## Executive Summary of the Project

### Target objectives and demonstration

DNA analysis for large populations has led to riveting discoveries that have taken the World by storm. Some of those advances provide understanding of our origins, including about where our ancestors lived and how to find unknown family members. Other advances provide insights about our health, including whether we have inherited risk factors for diseases and whether we will respond poorly to a drug. As more and more people get their DNA sequenced, those discoveries get increasingly useful.

The growth of DNA sequencing has been rapid. In 2001 the first one was done, in 2010 genetic variation was measured across hundreds of individuals, in 2015 it increased to thousands, and in 2018 a dataset about half a million individuals integrated genetic and phenotypic information. Today more than 30 million people have had their DNA sequenced and the number is growing, in part because the price tag is $\$ 400$ per person and falling. The growing datasets are a huge opportunity for DNA analysis to provide new insights into evolution and medicine.

The main roadblock to processing DNA for billions of people is computational power. The reason is that current algorithms won't scale on even the fastest classical computers. Indeed, current algorithms for DNA analysis of up to 1 million people can take several days of computation time. The leap to potentially 8 billion people is an increase of 4 orders of magnitude, which is out of reach for classical computers. We will overcome this by using quantum computing to revolutionize the speed of DNA analysis.

Our starting point is three of our recent classical algorithms for DNA analysis. Those algorithms can discover natural selection, heritability of disorders, and risk of developing a disease. For each algorithm, we will replace the most time-consuming classical subroutine with an exponentially faster quantum counterpart. The resulting algorithms will be hybrids of classical and quantum. Once we plug in the exponentially faster quantum subroutines, we expect our algorithms to scale to the entire World on near-term quantum computers.

We will simulate our algorithms with an existing quantum-circuit simulator. We will run the simulation on a subset of an existing DNA dataset for 488,363 individuals. We will focus on a subset for which the data and the algorithms fit within 30 qubits and a circuit depth of 20,000. We will compare the performance of our algorithms with that of our state-of-the-art classical algorithms. We will investigate scaling by running on a succession of larger and larger subsets of the full dataset. In practice, we expect simulation to scale to 30 qubits.

Ultimately, we will run our algorithms on a quantum computer. We will run on the entire dataset for 488,363 individuals, for which we estimate that we need 50 qubits and a circuit of depth 50,000. We plan to partner with Google who in the past has given us access to a Sycamore quantum computer with 53 qubits, which will be sufficient for our project.

For a future DNA dataset for 8 billion people, we estimate that we need 70 qubits and a circuit of depth 100,000. Thus, our project will enable a DNA analysis that scales to the entire World.

### Constituent research thrusts and activities

#### Algorithms

We have chosen a DNA dataset that our three classical algorithms have processed already. The results from those runs are the baseline against which we will compare our upcoming algorithms. Our next steps are to design quantum-classical hybrid versions of our algorithms and to prepare a quantum state that represents the dataset.

Dataset. Our dataset is the UK Biobank dataset [4], which consists of DNA data for 488,363 individuals. For each individual, we will focus on information about 500,000 genetic variants. For each genetic variant, this information expresses whether a mutation was inherited from the mother and the father of the individual. The dataset contains the count of such mutations, each of which is one of the numbers $0,1,2$.

The UK Biobank dataset can be accessed only after a process of application and approval. We have years of positive experience with this and have run all our three classical algorithms on this dataset.

Natural selection. We have presented a classical algorithm [3] that can identify several genome-wide signals of recent positive selection, which are regions of the genome that are evolving unusually rapidly and are highly likely to be functionally important. Our algorithm takes 30 minutes to process the UK Biobank dataset.

The main step of our algorithm is to find the principal components, which are those eigenvectors that correspond to the largest eigenvalues. We can replace this step with a known quantum algorithm for principal component analysis [17, [T]. The main step of quantum principal component analysis is phase estimation, which the algorithm uses twice. For data that can be represented with $n$ qubits, this algorithm requires $O(n)$ helper qubits and a circuit of depth $O\left(n^{2}\right)$.

Heritability of disorders. We have presented a classical algorithm [2T] that can identify enrichment of heritability - a measure of genetic signal - in FANTOM5 enhancers in asthma, eczema, thyroid, and autoimmune disorders. Our algorithm takes 3 hours to process the UK Biobank dataset.

The main step of our algorithm is to estimate the trace of a matrix, which is the sum of the diagonal elements. We can replace this step with a known quantum algorithm for trace estimation [18, Lemma 31]. The main step of quantum trace estimation is amplitude estimation, which principly relies on phase estimation. However, the paper [18] explains the algorithm in terms of QRAM, which likely won't be available in the project period. Thus, we need to rephrase the algorithm to use a known kind of representation. We plan to use the same representation as for quantum principal component analysis. For data that can be represented with $n$ qubits, the new formulation of the algorithm requires no helper qubits and a circuit of depth $O\left(n^{2}\right)$.

Risk of developing a disease. We have presented a classical algorithm [6] that can infer population structure - understanding the complex ancestral origins of the genome of an individual - and thereby improve our understanding of the risk of developing diseases that are known to vary according to genetic ancestry. Our algorithm takes 51 hours to process the UK Biobank dataset.

The main step of our algorithm is to find a nonnegative matrix factorization, which is a factorization that uses matrices that have only nonnegative entries. We can replace this step with a known quantum algorithm for nonnegative matrix factorization [8]. The main steps of quantum nonnegative matrix factorization are Hamiltonian simulation and phase estimation. For data that can be represented with $n$ qubits, the algorithm executes $n$ Hamiltonian simulations followed by a single step of phase estimation. We plan to do Hamiltonian simulation by Trotterization, which raises the question of how many time steps we need to get a good factorization. Our hypothesis is that a sufficient number of time steps can be done with a circuit of depth $O\left(n^{2}\right)$. The algorithm requires $O(n)$ helper qubits.

Data loading. The initial step in running a quantum subroutine on the UK Biobank dataset is to do data loading. This step maps a classical representation of the dataset to a quantum representation of the dataset [10]. The quantum representation is either a unitary matrix or a quantum state that a quantum subroutine can use.

The UK Biobank dataset has 488,363 $\times 500,000$ data points that each is one of 0,1,2. The classical representation of this dataset is nearly a trillion bits (a terabyte), which we can represent with 40 qubits because $2^{40}$ is greater than one trillion. We will do this in a way that fits phase estimation and Hamiltonian simulation, which are the key components of our quantum subroutines, as discussed above.

#### Simulation

We have years of experience with simulators of quantum circuits, both as implementers and as users. One point that stands out from that experience is that simulators differ wildly in their scalability, their models of noise, and their ease of use. For simulation of algorithms that process the UK Biobank dataset, scalability is of paramount importance. So, based on what is available today, we plan to use the qsim simulator from Google. The qsim simulator scales to noiseless simulation with 40 qubits on a 90-core Xeon desktop that costs $\$ 10,000$. It can also do noisy simulation with 30 qubits on the same kind of computer. However, those observations are for particular applications. We estimate that for our algorithms, simulation with 30 qubits is as much as qsim can do. So, we will run on a subset of the UK Biobank dataset for which the data and the algorithms fit within 30 qubits.

The ground truth for our simulations is available in our papers that report on running our classical algorithms on the UK Biobank dataset. The comparison with ground truth will enable us to both debug our quantum algorithms and to look for improvements.

In addition to simulation, we will use our own verification approach [24] to gain confidence in our quantum subroutines.

#### Experiments

For our experiments with running our algorithms on a quantum computer and the entire UK Biobank dataset, we need 50 qubits. We have experience with running on quantum Phase 1

3 classical Algorithms

algorithms Phase 2

Simulation

3 hybrid algorithms Phase 3

Experiments

results for 50 qubits

Figure 1: Our project.

computers from Google, IBM, and Rigetti. We expect to get access to a Google Sycamore with 53 qubits, as we have had in the past. While we earlier had this access to a Google Sycamore for free, we have budgeted for a cost to access.

We want the highest reliability we can get. We expect the reliability of quantum computers to improve during the project period and we will keep a keen eye on this. We note that adding error correction to our quantum circuits is unlikely to work within the project period: it requires too many qubits. Instead of adding error correction, we will optimize our quantum circuits to decrease their gate count and depth and thereby make them more likely to succeed on a near-term quantum computer. We will rely both on off-the-shelf optimizers and our own optimizer [23]. We will write our algorithms in Cirq [12] in a high-level manner such that we can easily compile them to different gate sets and different qubit connectivities.

### Thrust dependencies, balance and integration

Figure Ш illustrates our project. Our starting point is three of our recent classical algorithms for DNA analysis. In Phase 1 we replace key subroutines with exponentially faster quantum subroutines. In Phase 2 we simulate the quantum-classical hybrid algorithms on a subset of the UK Biobank dataset. This will involve a quantum circuit with 30 qubits and a depth of 20,000. In Phase 3 we experiment with the hybrid algorithms on a quantum computer and the entire UK Biobank dataset.

### Key intermediate program assessments and milestones

At the end of Phase 1: we have three hybrid quantum-classical algorithms that can process DNA data.

At the end of Phase 2: we have demonstrated simulations with the qsim simulator of all three algorithms on a subset of the UK Biobank dataset, with 30 qubits.

At the end of Phase 3: we have demonstrated runs with a quantum computer on the entire UK Biobank dataset, with 50 qubits.

### Risk mitigation and alternatives development strategies

We see three main risks to our project and we have the following mitigation strategies. Risk 1: the quantum subroutines work poorly. We will use quantum subroutines that we believe will work and scale as advertised. Still, one or more of them may work poorly or require many more resources than anticipated. We diversify the risk by working with three different algorithms that use different quantum subroutines. So, even if one of the subroutines disappoints, the others may work well.

Risk 2: the quantum computer is unreliable. The reliability of the Google Sycamore is around 99 percent per operation, which may well be too unreliable to get good results for 50 qubits. We do anticipate that quantum computers will get more reliable during the project period and that we may get access to a better one. However, if this doesn't work out, our simulation result for 30 qubits will in itself be valuable progress.

Risk 3: a key student leaves the project. Our project group has two professors and two Ph.D. students. Two of those people are experts on DNA analysis while the other two are experts on quantum computing. If one of the Ph.D. students leaves the project, which is a rare event at UCLA, we will ask one of our other students to step in and contribute to the project. In this case, one student can help the other with getting up to speed.

## Funding and Activities Summary

### Total cost and duration of proposed project

The budget is mainly for the cost of a total of 5 months of the Principal Investigator's time, the cost of a total of 5 months of the Co-Principal Investigator's time, the cost of two Ph.D. students for 2.5 years, and the cost of a postdoc for 2 years. This includes direct cost and relevant fees. The budget is also for the cost of travel and for the cost of access to a quantum computer. We will add overhead to UCLA separately at the end of the following calculation.

The total salaries, wages, and benefits is $\$ 714,790$. The cost of travel is $\$ 36,000$ for the entire period. The cost of access to a quantum computer is $\$ 175,000$ for Phase 3 . Once we add the cost for supplies and expenses, computer services, and relevant fees, we get a total direct cost of $\$ 973,705$. The overhead to UCLA is $\$ 381,619$. The grand total $\$ 1,355,324$.

### Breakdown and timeline of budget by activities

In the following table, all amounts are in $\$ 1,000$ s. For simplity, we divide the cost of each phase evenly on the quarters.

|                                                                                                      | Phase 1 |    |    |    |    | Phase 2 |    |    | Phase 3 |    |    |    |    |                      Total                      |
| :--------------------------------------------------------------------------------------------------: | :-----: | :-: | :-: | :-: | :-: | :-----: | :-: | :-: | :-----: | :-: | :-: | :-: | :-: | :----------------------------------------------: |
|                                                                                                      |   Q1   | Q2 | Q3 | Q4 | P1 |   Q1   | Q2 | P2 |   Q1   | Q2 | Q3 | Q4 | P3 |                                                  |
| $\begin{array}{l}\text { Algorithms } \\ \text { Simulation } \\ \text { Experiments }\end{array}$ |   118   | 118 | 119 | 119 | 474 |   138   | 138 | 276 |   151   | 151 | 151 | 152 | 605 | $\begin{array}{l}474 \\ 276 \\ 605\end{array}$ |
|                                                Total                                                |   118   | 118 | 119 | 119 | 474 |   138   | 138 | 276 |   151   | 151 | 151 | 152 | 605 |                       1,35                       |

## Proposal Body

### Motivation

It has long been known that most common human diseases are modulated by multiple genetic and environmental factors. Understanding the nature of genetic signal underlying these complex human diseases - how predictive of disease state is genetic variation (how heritability is the disease) and how is this heritability distributed across genes, regulatory elements, and biological pathways?) is a long-standing goal of human genetics.

Beyond its direct relevance to understanding basic disease etiology, understanding genetic signal or heritability has proven critical to a number of problems in human health. The first is in drug discovery. A challenge in drug discovery and development is that a large fraction (about 90This inability to predict the efficacy of drugs in humans has led to a search for alternate sources of evidence to inform decisions about potential drug targets. Multiple studies [20, 15] have shown that drugs with targets that are informed by genetic signal are substantially more likely to be approved (with [15] estimating this to double the success rate). One striking example of a genetically-informed approach to drug discovery has been the development of PCSK9 inhibitors to lower LDL-cholesterol levels based on human genetic studies of individuals with naturally occuring mutations that knocked out this gene [7]. The second problem is in the realm of personalized or precision medcine and centers around the task of accurately predicting and individuals disease or health outcome from their genetic information. Such predictors are now being developed for several disease outcomes with varying degrees of accuracy. For example, such predictors have recently been shown to be clinically relevant for predicting risk of coronary artery disease [I4] while a recent work has shown the value of these predictors in determining individuals that need to be screened for prostate-specific antigen for prostate cancer [1:3].

The search for genetic signal underlying diseases has been revolutionized by our ability to measure genetic variation across thousands of individuals at millions of locations along their genomes. Analyses of genetic data paired with disease information has led to the discovery of thousands of genetic variants associated with common diseases. One of the key findings from the success of this effort is the importance of large sample sizes in obtaining robust and replicable genetic associations.

Despite this impressive advance, the discovered genetic associations have lower predictive power than expected from theoretical expectations. This "missing heritability" has led the genetics community to (i) study larger samples of individuals; (ii) leverage new technologies that capture previously inaccessible genetic variants and (iii) measure diverse collections of phenotypes. The net result of these efforts is that the scale and complexity of the data collected, measured in terms of the number of individuals, genetic variants, and phenotypes measured, has increased dramatically. For example, the UKBiobank project involves the collection of whole-genome genotype data as well as thousands of diverse phenotypes from around half a million individuals from the UK while other similar projects are underway (China Kadoorie Biobank,Biobank Japan, FinnGen, the UCLA ATLAS Biobank, the BioVU Biobank at Vanderbilt University, the BioMe Biobank at Mount Sinai, and the US National Institutes of Health AllofUs program). Additional efforts are ongoing to enable sharing of data across these diverse datasets to fully realize the power of the massive scale. An accurate understanding of relationships among populations (population structure) is critical to the sharing efforts. This is because genetic differences due to population structure can confound efforts to learn about disease heritability and can lead to false discoveries if not accurately inferred. The challenge arises in developing algorithms that can infer population structure and estimate heritability while scaling to these massive datasets.

While we, and others, have developed a number of classical algorithms for these key tasks, the growth of these datasets is expected to outgrow the ability of these algorithms.

### Objectives and Significance

The problem. The problem is to scale DNA analysis to datasets of the future. We can get a sense of the magnitude of the problem by comparing the size of the UK Biobank dataset with a possible future dataset. The UK Biobank dataset has 488,363 $\times 500,000$ data points. The classical representation of this dataset is nearly a trillion bits, that is, a terabyte. A possible future dataset may cover the entire world and have data for 11.5 million single nucleotide polymorphisms (SNPs). Thus, the dataset would have 8 billion $\times 11.5$ million data points, a classical representation of which would be 100,000 terabytes. We can also compare the time needed to do classical computing on the datasets. Our algorithms for natural selection, heritability of disorders, and risk of developing a disease take 30 minutes, 3 hours, and 51 hours, respectively to process the UK Biobank dataset. Those algorithms scale linearly with the data size, which means that for the possible future dataset, they would take a factor of 100,000 longer. Thus, our estimates of the running times with classical computing are 6 years, 34 years, and 582 years on a dataset for the entire World and all SNPs.

DNA datasets are rapidly increasing in size and the need for classical computing power to process them is increasing proportionally. We have pushed classical computing nearly as far as we can in this area! We must face that processing future datasets will require a prohibitive amount of classical computing time. If classical computing is the best we can do, we will miss out on insights for human health applications.

We believe that quantum computing will provide the scability that is needed to process a DNA dataset for the entire World. Moreover, we estimate that the number of logical qubits and the circuit depth needed for DNA processing are modest compared to some other applications. Specifically, we estimate that a quantum computer can process the UK Biobank dataset with 50 qubits and a circuit depth of 50,000. This is much less of a quantum volume (the product of number of qubits and circuit depth) than some other applications that give quantum computing an advantage over classical computing. In particular, the needed quantum volume for Shor's algorithm, Grover's algorithm, and DNA sequencing are much higher, if they are to give a quantum advantage. If we take the 50 qubits for processing the UK Biobank dataset as our baseline, we can process a dataset that is 100,000 times larger by adding $\left(\log _{2} 100,000\right)=17$ qubits, plus some helper qubits.

The problem of scaling DNA analysis has an important subproblem: verification. For the UK Biobank dataset, the quantum volume is large enough that verification through simulation seems impossible. Instead, we will have to do simulation of quantum algorithms for subsets of the dataset. However, other approaches to verification of quantum circuits are emerging and a question is whether those approaches can help verify aspects of quantum algorithms for the entire dataset.

![](https://cdn.mathpix.com/cropped/2023_06_10_dafc0691c19d9a8bb6a6g-09.jpg?height=434&width=1347&top_left_y=252&top_left_x=389)

Figure 2: System overview.

Objectives. We will replace the current classical algorithms with quantum algorithms, as illustrated in Figure [2. The dataset for our experiments continues to be the UK Biobank dataset, and we will derive the same kinds of conclusions that are useful for health. We will represent the dataset as a quantum state, which enables quantum algorithms to process the data.

Figure 凤 is simpler than what we intend: in each classical algorithm, we will replace a key subroutine with a faster quantum subroutine. Thus, the resulting algorithms will be a hybrid of classical and quantum.

One of the benefits of the design in Figure 】 is that we can readily compare the output of the existing classical algorithms and the new hybrid algorithms. This will help us validate that our hybrid algorithms are correct.

We will demonstrate scalability by running both the classical and the hybrid algorithms on larger and larger subsets of the UK Biobank dataset. We will record the execution times and plot them as a function of the size of the input dataset. The result will a plot that, if we are successful, shows that the execution time of the hybrid algorithms grow much more slowly. This will imply that for much larger datasets, classical computation will be infeasible, while hybrid computation will succeed.

Significance. Our demonstration of scalability will be a key step towards deriving new conclusions from future, larger datasets. Those conclusions will be useful for health.

The field of quantum computing is looking for useful applications that give quantum computers an advantage of classical computers. So far, such applications require massive numbers of qubits that will become available in a distant future. We estimate that DNA analysis is an example of an application that can give a quantum advantage with a much smaller number of qubits. Indeed, some quantum computers today already provide the 50-70 qubits that we need for DNA analysis. If we also want to add error correction to get 5070 perfect qubits, we will need fewer than 50,000-70,000 qubits, which are likely to become available this decade. In summary, we see DNA analysis as an application for which quantum algorithms will revolutionize the size of dataset that we can process.

![](https://cdn.mathpix.com/cropped/2023_06_10_dafc0691c19d9a8bb6a6g-10.jpg?height=623&width=1567&top_left_y=236&top_left_x=276)

Figure 3: Our research team at UCLA on Wed May 31, 2023.

### Our Team and Our Preliminary Investigation

Our research team consists of eight people, all shown in Figure [3:

- Abdulrahman Sahmoud (senior software engineer, Amazon AWS Center for Quantum Computing, on the left),
- Sriram Sankararaman (co-PI, second from the left),
- Jens Palsberg (PI, third from the left),
- Payal Kaushik (graduate student in physics, fourth from the left),
- Shane Woods (graduate student in physics, fourth from the right),
- Ali Pazoki (graduate student in computational medicine, third from the right),
- Jeffrey Ma (graduate student in computer science, second from the right),
- Yin Huang (graduate student in physics, on the right),

Yin Huang, Payal Kaushik, Jeffrey Ma, and Shane Woods have all taken Jens Palsberg's courses on quantum programming and on quantum algorithms. As part of those courses, they have learned many quantum algorithms and run them on quantum hardware, they have each built a quantum circuit simulator, and they have studied the foundations of quantum computing. Ali Pazoki is an expert on classical algorithms for DNA analysis.

This Spring, we have focused on getting a shared understanding of the existing classical algorithms, on understanding how to map the dataset to a unitary matrix and to quantum state, and on mastering the quantum algorithms that we need. In particular, we have done experiments with data loading, mainly by designing appropriate circuits by hand. We have also done experiments with running the quantum algorithms on microbenchmarks to see that they work as expected.

Our preliminary investigation has informed our proposed research, as we explain next.

### Proposed Research: Algorithms

Dataset. We begin with an example of made-up data for four individuals and four SNPs. The goal is to show how we organize the data and to explain what the data means. Later, we will also use this data to show how we will do data loading. The following matrix $A$ contains the data:

$$
\begin{aligned}
& A=\left(\begin{array}{llll}
2 & 0 & 1 & 2 \\
1 & 0 & 2 & 2 \\
1 & 2 & 2 & 1 \\
2 & 2 & 2 & 2
\end{array}\right) \begin{array}{l}
\text { this row has data for SNP 1 } \\
\text { this row has data for SNP 2 } \\
\text { this row has data for SNP 3 } \\
\text { this row has data for SNP 4 }
\end{array} \\
& \text { a column per individual }
\end{aligned}
$$

In the matrix $A$ above, we have one row for each SNP and one column for each individual. Each entry of $A$ is one of $0,1,2$. Notice that in the first row's third column, the entry is 0 . This means that for the individual represented in the third column, for SNP 1, no mutations happened compared to the father and the mother. In contrast, for the individual represented in the first column, for SNP 1, the entry is 2 so mutations happened compared to both the father and the mother. However, for the individual represented in the second column, for SNP 1, the entry is 1 so a single mutation happened compared to one of the father and the mother, but not both.

Let us take a closer look at the UK Biobank dataset, specifically for 291,273 individuals (columns) genotyped at 454,207 SNPs (rows). We counted the number of 0,1,2 entries across the SNPs and across the individuals. Here is the summary statistics:

|              | Each row contains |          |          | Each column contains |          |          |
| :----------- | ----------------: | -------: | -------: | -------------------: | -------: | -------: |
|              |          $\# 0$ | $\# 1$ | $\# 2$ |                   co | $\# 1$ | $\# 2$ |
| Minimum      |                 7 |    5,634 |   72,296 |               12,766 |   71,872 |  355,850 |
| 1st Quartile |               189 |   14,497 |  196,420 |               14,089 |   80,345 |  359,081 |
| Median       |               912 |   30,785 |  259,571 |               14,219 |   80,645 |  359,342 |
| Mean         |             9,121 |   51,708 |  230,444 |               14,223 |   80,632 |  359,351 |
| 3rd Quartile |             9,294 |   85,557 |  276,586 |               14,351 |   80,947 |  359,599 |
| Maximum      |            73,262 |  147,164 |  285,612 |               16,511 |   84,164 |  368,963 |

Notice that our example matrix $A$ has frequencies of $0 \mathrm{~s}, 1 \mathrm{~s}$, and $2 \mathrm{~s}$ that are consistent with the table above: few 0 s, more $1 \mathrm{~s}$, and many $2 \mathrm{~s}$.

Without loss of generality, we can choose a representation that maximizes the number of zeros. For this dataset, we switch 0 with 2 to get many more zeros. (In the jargon of the field, this change can be described as switching the major allele with the minor allele.)

Once we have made the switch, the matrix for the UK Biobank data contains 79 percent zeros. However, while the numbers of zeros in the columns vary little, the numbers of zeros in the rows vary significantly. In particular, one of the rows contains only 72,296 zeros. Thus, the matrix is sparse and the columns are sparse, but some rows are far from sparse. This observation will play a key role in our estimate of the number of qubits and of the circuit depth of our quantum algorithms, see below. Data loading. Lead investigator: Payal Kaushik.

Let us consider again the $4 \times 4$ matrix $A$ from above and let us switch 0 with 2 , as described above. The result is the following matrix $B$ :

$$
B=\left(\begin{array}{llll}
0 & 2 & 1 & 0 \\
1 & 2 & 0 & 0 \\
1 & 0 & 0 & 1 \\
0 & 0 & 0 & 0
\end{array}\right)
$$

For the purpose of quantum processing, we need to represent $B$ in two different ways: as a unitary matrix and as a quantum state. This is because one of the quantum algorithms requires the data to be presented as a unitary matrix while two others work with a quantum state. We describe our approach to getting this done next.

Let us first consider how to represent $B$ as a unitary matrix. We can see that $B$ is not unitary, for at least two reasons. First, the rows and columns are not unit vectors, hence $B$ is not unitary. Second, one of the rows of $B$ is 0 , which implies that $B$ is not invertible, hence $B$ is not unitary. However, we can do a block encoding of $B$, which will place $B$ as a block in a larger, unitary matrix. This enables quantum algorithms to work on the larger matrix and, as a part of that, to do the right thing for $B$.

The first step of doing a block encoding is to scale $B$ such that the larger matrix can have rows and columns that are unit vectors. If we scale $B$ by $\frac{1}{4}$, we achieve that goal. Let us call the scaled matrix $C=\frac{1}{4} B$.

The second step is to place $C$ as a block of a unitary matrix $U$ :

$$
U=\left(\begin{array}{ll}
C & * \\
* & *
\end{array}\right)
$$

Gilyen, $\mathrm{Su}$, Low, and Wiebe [9, Lemma 48] showed how to produce a good approximation of $U$ for a sparse matrix $C$. Recent papers by Camps et al. [5, I] pursued this further and showed how to do efficient block encoding of certain sparse matrices. The structure of the circuit that builds the block encoding of a matrix $C$ is as follows:

![](https://cdn.mathpix.com/cropped/2023_06_10_dafc0691c19d9a8bb6a6g-12.jpg?height=231&width=832&top_left_y=1782&top_left_x=625)

In the above circuit diagram, $m$ satisfies $s=2^{m}$, where $s$ is the maximum number of nonzero entries in any row or column, $|j\rangle$ encodes a column number, while $V$ and $W$ encode access to data in $C$. The main challenge is to produce circuits $V$ and $W$ with small depth. We will do this with the technique in the paper [22], which shows how to do efficient block encoding of matrices such as ours that contain just three different values such as 0,1 , and 2 . Specifically, for a dataset of size $2^{n}$, the approach in [22] requires $2 n+2$ qubits and a circuit of depth $O\left(n^{2}\right)$.

For the UK Biobank dataset, we saw above that the transformed matrix (after a switch of 0 and 2) is sparse, though some rows have many nonzeros. For simplicity, we need the matrix to be square. For additional simplicity, we need the number of rows to be a power of 2. Given that the UK Biobank dataset has data about 488,363 individuals, we will focus on $2^{18}$ rows because $2^{18}=262,144$. Thus, we will pick $2^{18}$ individuals and $2^{18}$ SNPs and form a $\left(2^{18} \times 2^{18}\right)$ matrix of the data. For a block encoding of our $\left(2^{18} \times 2^{18}\right)$ matrix, we will need $(2 \times 18)+2=38$ qubits and a circuit that we estimate to be of depth 6,000

Let us now turn to representing the matrix $B$ as a quantum state. The baseline approach is to use an amplitude encoding, which represents the entries in the matrix as the amplitudes of a quantum state. However, producing such an encoding may require a circuit of exponential depth. We will use a recent improvement of this approach, called approximate amplitude encoding [II] . The idea is to train a parameterized quantum circuit $U(\theta)$, where $\theta$ is a list of parameters, such that $U(\theta)\left|0^{n}\right\rangle$ produces an approxiate amplitude encoding of the data. The paper [19] shows how this can be successful with a circuit of depth $O\left(n^{2}\right)$.

The training phase requires many shots, where a shot is a single run of a quantum circuit. We will try several techniques for varying and optimizing the parameters.

Natural selection. Lead investigator: Jeffrey Ma.

For computing the principal components, we work with the standardized version of the matrix $A$. We know two papers [I7, I]] on quantum principal component analysis.

The goals are to write an implementation that is parameterized in the number of qubits, to experiment with simulations of instances with a varying number of qubits, and to write a report about the findings. Does the approach scale well? A key objective is to identify problems and obstacles, and then to solve and overcome them, or to argue why much more work is needed. If we discover more papers that are related to the algorithmic problem or are otherwise helpful, please cite them and share them. I am particularly interested to know whether some back-and-forth between classical and quantum is an essential part of the implementation.

I would love to have a clear statement of the required number of qubits and the required circuit depth, both expressed in terms of the size of the input. My hope is that for input of size $n$, the required number of qubits is $O(\log n)$, while the required circuit depth is $O\left((\log n)^{2}\right)$, or something similar. We shall see! Heritability of disorders. Lead investigator: Yin Huang.

We are computing the trace of a matrix derived from the given matrix, as follows.

$$
\begin{array}{rlrl}
\text { Step 1: } & A & =\text { the given } 0,1,2 \text { matrix } \\
\text { Step 2: } & X & =\text { the standardized version of } A \\
\text { Step 3: } & K & =(1 / \# \mathrm{SNP}) X \times X^{T} \\
\text { Step 4: } & S & =K \times K \\
\text { Step 5: result } & =\operatorname{trace}(S)
\end{array}
$$

Step 3 is $O\left(N^{2} M\right)$, where $N$ is the number of individuals and $M$ is the number of SNPs; computing the trace is $O\left(N^{2}\right)$. Current datasets have $N=10^{5}-10^{6}$ and $M=10^{6}-10^{7}$ and future datasets will have $N=10^{9}$ and $M=10^{8}-10^{9}$.

We know a paper on quantum trace estimation [18, Lemma 31]. The main question is whether we can use the technique from [18, Lemma 31] to estimate the trace, or whether we need a variation of the algorithm. The goal is to get to an estimate of the trace while using a reasonable amount of resources.

Read also the red and blue text above (under natural selection). Risk of developing a disease. Lead investigator: Shane Woods.

For computing a nonnegative matrix factorization, we work with the matrix $A$ itself. We know a paper $[8]$ on quantum nonnegative matrix factorization.

Read also the red and blue text above (under natural selection).

### Proposed Research: Simulation

Simulating via Amazon Braket. We want to be able to seemlessly go from circuit simulation to use of a quantum computer. We will achieve that by going via Amazon Braket. We begin by noting that for circuit simulation with fewer than 18 qubits, we can run on a laptop. For circuit simulation for 18-34 qubits, we can use the SV1 simulator. There is no limit on circuit depth, but there is a limit on the run time: 6 hours. The Braket website reports that a $34 \times 34$ circuit takes 1-2 hours to execute, which gives a practical limit on the circuit depth. For circuit simulation for $34-50$ qubits, we can use the TN1 simulator. This simulator has a circuit-depth limit of 1,000 and it may run well or poorly depending on how entangled the qubits are, which remains to be seen.

Comparison with ground truth. Figure ⿴囗口 illustrates why we can compare the results of our simulations with ground truth. The ground truth is available in our papers and comes from running our classical algorithms on the UK Biobank dataset, which is the upper path in Figure Ш. Simulation of our quantum algorithms on the UK Biobank dataset is the lower path in Figure Ш. We can compare the eigenvectors, the traces, and the nonnegative matrix factorizations found by the two approaches and determine how similar they are. Additionally, we can compare the overall conclusions that are useful for health care and determine how similar they are. We will define similarity measures and automate the comparison process.

We anticipate that the simulations and comparisons with ground truth will reveal bugs. Those bugs can be in both in our implementation of data loading and in our implementation of the quantum algorithms. We view Phase 2 of the project as an essential phase during which we fix and tune our implementations to be of high quality. At the end of Phase 2, we will have simulations for circuits with 30 qubits that produce results matching those produced by classical algorithms. This will give us confidence that the algorithms will continue to work well for higher numbers of qubits.

Debugging. Let us go into more detail of what we will do if we simulate one of the quantum algorithms and get an unexpected result. The question is: how would we know where something went wrong? We can let the simulator print intermediate states but this is helpful only if we know what to expect. We overcome this by writing down our expectations as assertions about some of the states. Now we can check that those states satisfy the assertions, as the simulation proceeds. If the simulation reaches a state for which an assertion fails, we know that the problem lies earlier. Indeed, likely the problem lies between the last assertion that succeeded and the first assertion that failed.

We plan to go a step further with the idea of using assertions for debugging. The idea is to restrict the kinds of assertions that we can write and, in return, get support for debugging that goes beyond simulation. Specifically, we use projections as our assertions, which enables us to use two recent techniques by Li et al. [16] and Yu and Palsberg [24]. The technique by Li et al. [16] supports assertion checking during runs on a quantum computer. In contrast, the technique by Yu and Palsberg [24] supports assertion checking without simulation and without use of a quantum computer. In both cases, the assertion checking scales way beyond the size of circuits that we can simulate.

### Proposed Research: Experiments

Access via Amazon Braket. We have budgeted $\$ 175,000$ for access to a quantum computer via Amazon Braket. At the moment, the best option that Amazon Braket offers is a Rigetti quantum computer called Aspen-M-3, which has 79 qubits. For this quantum computer, the budget of $\$ 175,000$ will give us 500 million shots.

During year-long Phase 3, we want to distribute the 500 million shots evenly on 50 work weeks, so 10 million shots per week. The coherence time of the Aspen-M-3 is 20 microseconds [2]. So, 10 million shots that each takes 20 microseconds can in principle be executed in 200 seconds. However, the time to start a new shot dwarfs the execution time of the shot itself. On Amazon Braket, in a version that will come out this Summer 2023, 10 million shots can be executed in 17 minutes, we have heard from our Amazon colleagues.

This has led us to design the following work cycle for each week of Phase 3 :

1. prepare a new experiment (most of the week),
2. do the experiment (in well less than an hour), and finally
3. learn from the experiment (rest of the week).

This will maximize the value of our access to the quantum computer.

Optimization. We estimate that a quantum computer can process the UK Biobank dataset with 50 qubits and a circuit depth of 50,000. However, the Aspen-M-3 can process circuits of a depth that is most 500. While we do hope for access to a better quantum computer than Aspen-M-3, we will also optimize our quantum circuits to decrease their depth. We do realize that cannot predict which quantum computers will become available in Phase 3 or which gates sets they will have. So, we will use Quartz [2:3], which our own quantum circuit superoptimizer. Quartz automatically generates and verifies circuit transformations for arbitrary quantum gate sets. For a given gate set, Quartz generates candidate circuit transformations by systematically exploring small circuits and verifies the discovered transformations using an automated theorem prover. To optimize a quantum circuit, Quartz uses a cost-based backtracking search that applies the verified transformations to the circuit. Our experiments show that Quartz is able to optimize a broad range of circuits for diverse gate sets, outperforming or matching the performance of hand-tuned circuit optimizers. For the Rigetti gate set, Quartz reduces the gate count by 49 percent on average. We will design and implement a more aggressive version of Quartz that will decrease the gate count even more.

Scalability. We will device a series of larger and larger subsets of the UK Biobank dataset. For simplicity, in each subset, the number of individuals will equal the number of SNPs. Thus, each subset can be represented by a matrix of size $2^{i} \times 2^{i}$, where $2 \leq i \leq 18$. Thus, the $(i+1)^{\prime}$ th dataset is 4 times larger than the $i$ 'th dataset. This will enable us to plot results with the data size on a log-scale x-axis and with the execution time on a linear-scale y-axis. The goal is to get plot points that forms a straight line, which will show that when we double the datasize, the execution time grows linearly.

## Key Personnel Bios, Facilities/Resources

Jens Palsberg. Research: programming languages, software engineering, quantum computing. Projects: NJR: A Normalized Java Resource; reasoning about the Java memory model; verification and optimization of quantum programs.

Education.

MBA, Executive MBA Program, UCLA Anderson School of Management, Los Angeles, 2017

PhD, Computer Science, University of Aarhus, Denmark, 1992

M.Sc., Computer Science and Mathematics, University of Aarhus, Denmark, 1988

Employment history.

2003-present Professor, UCLA.

2010-2015 Chair of Computer Science Department, UCLA.

2005-2007 Graduate Vice Chair of Computer Science Department, UCLA.

2002-2003 Professor and Associate Department Head, Purdue University.

1996-2002 Associate Professor, Purdue University.

1995-1996 Visiting Scientist, Massachusetts Institute of Technology.

1993-1994 Visiting Assistant Professor, Northeastern University.

Five recent publications.

a. Mingkuan Xu, Zikun Li, Oded Padon, Sina Lin, Jessica Pointing, Auguste Hirth, Henry Ma, Jens Palsberg, Alex Aiken, Umut A. Acar, Zhihao Jia. Quartz: superoptimization of Quantum circuits. PLDI 2022, International Conference on Programming Language Design and Implementation, 2022.

b. Akshay Utture, Shuyang Liu, Christian Gram Kalhauge, Jens Palsberg. Striking a Balance: Pruning False-Positives from Static Call Graphs. In ICSE'22, International Conference on Software Engineering, 2022.

c. Akshay Utture, Jens Palsberg. Fast and Precise Application Code Analysis using a Partial Library. In ICSE 2022, International Conference on Software Engineering, 2022.

d. Nengkun Yu, Jens Palsberg. Quantum abstract interpretation. In PLDI'21, ACM Conference on Programming Language Design and Implementation, 2021.

e. Christian Gram Kalhauge, Jens Palsberg. Logical bytecode reduction. In PLDI'21, ACM Conference on Programming Language Design and Implementation, 2021.

Five synergistic activities.

a. Director of the UCLA-Amazon Science Hub for Humanity and Artificial Intelligence, 2021-present.

b. Member of $22 \mathrm{NSF}$ review panels.

c. As a member of the ACM Executive Committee, 2020-present, championed successfully that the special interest groups get a break in their payment of overhead to ACM in Fiscal Year 2022, in view of the pandemic.

d. Incorporated the principles and practices of formal review into the Purdue CS Ph.D. education, smoothly and inexpensively, as part of the existing course work.

e. Created a project for the Purdue undergraduate compiler course, and based on that, co-authored a revision of Andrew Appel's textbook on Modern Compiler Implementation in Java. Sriram Sankararaman. I am a computational biologist with broad research interests in developing statistical and machine learning models to make sense of genomic and biomedical data. My lab develops novel statistical and computational tools and applies these tools to analyze large-scale genomic datasets with the goal of understanding the link between evolution, genes, and traits.

Education.

2010-2015 Post-doctoral fellow, Dept. of Genetics, Harvard Medical School.

2004-2010 Ph.D. Computer Science, UC Berkeley.

2000-2004 B.Tech, Computer Science and Engineering, Indian Inst. of Technology, Madras. Employment history.

2021-Present Associate Prof., UCLA; Depts. Comp. Sci., Comp. Medicine, Human Genetics. 2015-2021 Assistant Professor, UCLA.

2011-2015 Post-doctoral fellow, Department of Genetics, Harvard Medical School.

Honors.

2022 Invited participant to the China-America Frontiers of Engineering Symp., USA NAE. 2021 Invited participant to the Arab-American Frontiers symposium, US National Academies. 2020 Microsoft Investigator Fellowship.

2020 NSF Career Award.

2019 UCLA School of Engineering Excellence in Teaching Award.

2017 UCLA Hellman Fellow.

2017 Alfred P. Sloan fellow.

2017 Okawa Foundation Award.

2015 Semifinalist for Trainee Research Award, American Society of Human Genetics.

2014 NIH K99/R00 Pathway to Independence Award.

2014 Fellow at the Simons Institute for Theory of Computing, Berkeley.

2012 Fellow of the Harvard Initiative for Science of the Human Past.

Five recent publications.

a. Chiu et al. Inferring population structure in biobank-scale genomic data, American Journal of Human Genetics (2022).

b. Wu et al. Fast estimation of genetic correlation for Biobank-scale data. American Journal of Human Genetics (2021).

c. Agrawal, Chiu, et al. Scalable probabilistic PCA for large-scale genetic variation data, PLoS Genetics (2020).

d. Pazokitoroudi et al. Efficient variant components analysis across millions of genomes, Nature Communications (2020).

e. Durvasula and Sankararaman. Recovering signals of ghost archaic introgression in African populations, Science Advances (2020).

Facilities/resources. We have adequate facilities at UCLA to carry out the project. Our students and postdoc are housed in the labs of Palsberg and Sankararaman.

We will access a quantum circuit simulator and a quantum computer via Amazon Braket.

## Commercialization/Partner Strategy

Our research team is has members from UCLA and from the Amazon AWS Center for Quantum Computing. Our goal is to leverage both the classical computing resources provided by AWS and the quantum computing resources provided by Amazon Braket. This has three of the main advantages:

- AWS is a powerful and inexpensive resource for running quantum circuit simulators.
- Amazon Braket provides access to many quantum computers and we expect that by the time Phase 3 begins, additional ones will be accessible.
- AWS provides a seamless path to go from quantum circuit simulation to running the circuit on a quantum computer. This is a key benefit for our large-scale experiments.

Here are some examples of quantum computers to which Amazon Braket provides access already.

| Device                         | \# Qubits | Price per shot |
| :----------------------------- | --------: | :------------- |
| Rigetti - Aspen-M-3            |        80 | $\$ 0.00035$ |
| IonQ - Aria 1                  |        25 | $\$ 0.01$    |
| IonQ - Harmony                 |        11 | $\$ 0.03$    |
| Oxford Quantum Circuits - Lucy |         8 | $\$ 0.00035$ |

The above table shows that Amazon Braket already provides access to a quantum computer with a sufficient number of qubits for our purposes. A major concern for the AspenM-3 is its coherence time: we hope that Amazon Braket in Phase 3 can provide access to a quantum computer with both $50+$ qubits and longer coherence time.

Principal investigator Palsberg is well-connected to Amazon AWS in another way. Specifically, he is the director of the UCLA-Amazon Science Hub for Humanity and Artificial Intelligence. The mission of the science hub is to address humanity's pressing challenges by cross-pollinating academic and industry research that harnesses the power of artificial intelligence. The science hub has created many connections between researchers at UCLA and researchers at Amazon. In a similar manner, our project on quantum analysis of human DNA, as described in this proposal, is a connection between UCLA and Amazon. As the project moves forward, we hope to involve more people from Amazon.

We have no commercialization strategy at the moment. Principal investigator Palsberg has both a strong publication record and a patent record, with more than 180 publications and 3 USA patents. Our current plan is to publish our discoveries and to make our software available in open source. However, we are open to talk to commercial entities and we leave the door open to form a start-up company based on our discoveries.

## Detailed Project Activity, Schedule and Budget

### Project activities and schedule

Phase 1: algorithms (1 year). Phase 2: simulation (0.5 year). Phase 3: experiments (1 year).

### Budget and budget justification

We give the budget in the table below.

UCLA's fiscal year runs July 1 to June 30. Calendar effort is committed during this same period for faculty and other senior personnel. For faculty on an academic appointment, effort committed can include effort during the academic year (October 1st through June 30th) and/or during the summer (July 1st through September 30th). Salaries are escalated by 3 percent per year.

Principal Investigator: Professor Jens Palsberg. The PI is proposing the following effort: 2 months in Phase 1 and 1 month in Phase 2 and 2 months in Phase 3 . The PI will lead the research and oversee the entire project. The PI will also provide guidance to the graduate student researchers and postdoctoral scholar. Professor Palsberg's per-month summer salary is $\$ 26,511.11$.

Co-Principal Investigator: Professor Sririm Sankararaman. The Co-PIs are proposing the following effort: 2 months in Phase 1 and 1 month in Phase 2 and 2 months in Phase 3. The Co-PIs will lead sub-tasks of the research and provide guidance to the graduate student researchers. Professor Sankararman's per-month summer salary is $\$ 25,344.45$

Graduate Student Researchers. Two Graduate Student Researchers are proposed for the project. Effort is based on the following: Year 1 and 3: 50 percent for 9 academic months and 50 percent for the 3 summer months; Year 2: 50 percent for 4 academic months and 50 percent for the 2 summer months. The GSRs will work closely with the PI and Co-PIs on the proposed research directions. The GSRs will be paid at Step V with the current 100 percent salary rate of $\$ 6,861 / \mathrm{mo}$.

Postdoctural Scholar. One Postdoctural Scholar is proposed for the project. Effort is based on the following: 7 months in Phase 1 (starting Jan 1, 2024) and 6 months in Phase 2 and 12 months in Phase 3. The Postdoc's salary is calculated as follows: Year 1: $\$ 5,000 /$ month; Year 2: $\$ 5,185 /$ month and Year 3: $\$ 5,376.83 /$ month, per the approved salary rate for FY $2023 / 2024$

The Postdoc will work closely with the PI, Co-PI and GSRs to meet the milestones of the proposed research. The postdoctoral scholar will integrate the quantum algorithms (in the second half of Phase 1), scale the simulations (in Phase 2), and lead the experimental effort (in Phase 3). Total salaries, wages, and benefits. For the Principal Investigator, Co-Principal Investigator, Graduate Student Researchers, and Postdoctural Scholar, the total salaries and wages is $\$ 567,460$. Once we add employee benefits, the total of this budget item is $\$ 714,790$.

Travel. $\$ 36,000$ for the entire period. The travel funds requested to cover the cost for the PI or the graduate student to attend a domestic peer review panel of the program and domestic professional conferences for each year of the project.

Access to a quantum computer. $\$ 175,000$ in Phase 3. We will access a quantum computer via Amazon Braket. At the moment, the best option that Amazon Braket offers is a Rigetti quantum computer called Aspen-M-3, which has 79 qubits. The price for running on Aspen-M-3 is given by the formula:

$$
\text { Total price }=\text { Number of shots } \times \text { Price per shot }
$$

We estimate that we need to run 500 million shots. The price for a shot on Aspen-M-3 is $\$ 0.00035$. Thus, we get a total price of

$$
\text { Total price }=500 \text { million } \times \$ 0.00035=\$ 175,000
$$

Thus, we have budgeted for $\$ 175,000$ for access to a quantum computer via Amazon Braket.

Supplies and expenses. $\$ 24,000$ for the entire period. Material and supplies are request to purchase software/ hardware (laptop/desktop) and misc. items specific to the project.

Computer Services. $\$ 12,796$ for the entire period. Computer (ADPE) Services is the computer networking services that provides shared network services with the Computer Science Department. The ADPE services will maintain full-service computing environment to support research and institution. The network service has been established at $\$ 124$ per person per month.

Technology infrastructure fee. $\$ 2,948$ for the entire period.

General and Employment Liability Fees (GAEL). $\$ 8,172$ for the entire period.

Total Direct Cost. Once we sum up all the previous budget items, we get that the total direct cost is $\$ 973,705$.

Overhead (facilities and administrative costs). $\$ 381,619$ for the entire period. The overhead is based on a federally negotiated agreement dated 10/12/18. The on-campus research rate is currently 57 percent for FY $23 / 24$ and 57.5 percent for FY $24 / 25$. The new overhead rate agreement date is March 28, 2023.

![](https://cdn.mathpix.com/cropped/2023_06_10_dafc0691c19d9a8bb6a6g-23.jpg?height=2128&width=1619&top_left_y=264&top_left_x=253)

## References

[1] FABLE: Fast Approximate Quantum Circuits for Block-Encodings. In 2022 IEEE International Conference on Quantum Computing and Engineering (QCE), 2022.

[2] Aspen-M-3 Quantum Processor. Accessed on Jun 3, 2023.

[3] Aman Agrawal, Alec M. Chiu, Minh Le, Eran Halperin, and Sriram Sankararaman. Scalable Probabilistic PCA for Large-Scale Genetic Variation Data. PLOS Genetics, May 2020.

[4] C. Bycroft, C. Freeman, D. Petkova, G. Band, L.T. Elliott, K. Sharp, A. Motyer, D. Vukcevic, O. Delaneau, J. O'Connell, and Et Al. The UK Biobank Resource with Deep Phenotyping and Genomic Data. Nature, (562):203-209, 2018.

[5] Daan Camps, Lin Lin, Roel Van Beeumen, and Chao Yang. Explicit Quantum Circuits for Block Encodings of Certain Sparse Matrices. 2022.

[6] Alec M. Chiu, Erin K. Molloy, Zilong Tan, Ameet Talwalkar, and Sriram Sankararaman. Inferring Population Structure in Biobank-Scale Genomic Data. American Journal of Human Genetics, 109(4):727-737, 2022.

[7] Jonathan Cohen, Alexander Pertsemlidis, Ingrid K Kotowski, Randall Graham, Christine Kim Garcia, and Helen H Hobbs. Low LDL cholesterol in individuals of African descent resulting from frequent nonsense mutations in PCSK9. Nature Genetics, $37(2): 161-165,2005$.

[8] Yuxuan Du, Tongliang Liu, Yinan Li, Runyao Duan, and Dacheng Tao. Quantum Divide-and-Conquer Anchoring for Separable Non-Negative Matrix Factorization. In Proceedings of the 27 th International Joint Conference on Artificial Intelligence, pages 2093-2099. AAAI Press, 2018.

[9] Andras Gilyen, Yuan Su, Guang Hao Low, and Nathan Wiebe. Quantum Singular Value Transformation and Beyond: Exponential Improvements for Quantum Matrix Arithmetics. In Proceedings of the 51st Annual ACM SIGACT Symposium on Theory of Computing (STOC 2019), pages 193-204, 2019.

[10] Max Hunter Gordon, M. Cerezo, Lukasz Cincio, and Patrick J. Coles. Covariance Matrix Preparation for Quantum Principal Component Analysis. PRX Quantum, (3), 2022.

[11] Chen He, Jiazhen Li, Weiqi Liu, and Jane Wang. A Low Complexity Quantum Principal Component Analysis Algorithm. IEEE Transactions on Quantum Engineering, 2021.

[12] Alan Ho and Dave Bacon. Announcing Cirq: An open source framework for NISQ algorithms. Google AI Blog; Google AI Quantum Team; https://ai.googleblog. com/2018/07/announcing-cirq-open-source-framework.html, June 2018.

[13] Linda Kachuri, Thomas J Hoffmann, Yu Jiang, Sonja I Berndt, John P Shelley, Kerry Schaffer, Mitchell J Machiela, Neal D Freedman, and Wen-Yi Huang et al. Genetically adjusted psa levels for prostate cancer screening. Nature Medicine, 2023. [14] Amit V Khera, Mark Chaffin, Krishna G Aragam, Mary E Haas, Carolina Roselli, Seung Hoan Choi, Pradeep Natarajan, Eric S Lander, Steven A Lubitz, Patrick T Ellinor, and et al. Genome-wide polygenic scores for common diseases identify individuals with risk equivalent to monogenic mutations. Nature Genetics, 50(9):1219-1224, 2018.

[15] Emily A King, J Wade Davis, and Jacob F Degner. Are drug targets with genetic support twice as likely to be approved? revised estimates of the impact of genetic support for drug mechanisms on the probability of drug approval. PLoS Genetics, $15(12), 2019$.

[16] Gushu Li, Li Zhou, Nengkun Yu, Yufei Ding, Mingsheng Ying, and Yuan Xie. Projection-based runtime assertions for testing and debugging quantum programs. Proc. ACM Program. Lang., 4(OOPSLA), November 2020.

[17] Seth Lloyd, Masoud Mohseni, and Patrick Rebentrost. Quantum Principal Component Analysis. Nature Physics, 10:631-633, 2014.

[18] Alessandro Luongo and Changpeng Shao. Quantum Algorithms for Spectral Sums. 2020.

[19] Kouhei Nakaji, Shumpei Uno, Yohichi Suzuki, Rudy Raymond, Tamiya Onodera, Tomoki Tanaka, Hiroyuki Tezuka, Naoki Mitsuda, and Naoki Yamamoto. Approximate amplitude encoding in shallow parameterized quantum circuits and its application to financial market indicators. Phys. Rev. Res., 4, May 2022.

[20] Matthew R Nelson, Hannah Tipney, Jeffery L Painter, Judong Shen, Paola Nicoletti, Yufeng Shen, Aris Floratos, Pak Chung Sham, Mulin Jun Li, Junwen Wang, and et al. The support of human genetic evidence for approved drug indications. Nature Genetics, $47(8): 856-860,2015$.

[21] Ali Pazokitoroudi, Yue Wu, Kathryn S. Burch, Kangcheng Hou, Aaron Zhou, Bogdan Pasaniuc, and Sriram Sankararaman. Efficient Variance Components Analysis Across Millions of Genomes. Nature Communications, 11, 2020.

[22] Christoph Sünderhauf, Earl Campbell, and Joan Camps. Block-encoding Structured Matrices for Data Input in Quantum Computing. 2023.

[23] Mingkuan Xu, Zikun Li, Oded Padon, Sina Lin, Jessica Pointing, Auguste Hirth, Henry Ma, Jens Palsberg, Alex Aiken, Umut A. Acar, and Zhihao Jia. Quartz: Superoptimization of Quantum Circuits. In Proceedings of PLDI'22, ACM SIGPLAN Conference on Programming Language Design and Implementation, pages 625-640, June 2022.

[24] Nengkun Yu and Jens Palsberg. Quantum Abstract Interpretation. In Proceedings of PLDI'21, ACM SIGPLAN Conference on Programming Language Design and Implementation, June 2021.

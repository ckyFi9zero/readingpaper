# 4DenoiseNet: Adverse Weather Denoising From Adjacent Point Clouds

**论文信息：** Seppänen et al., IEEE Robotics and Automation Letters (RA-L), Vol. 8, No. 1, January 2023

---

## Abstract 解析

### 原文呈现

> Reliable point cloud data is essential for perception tasks e.g. in robotics and autonomous driving applications. Adverse weather causes a specific type of noise to light detection and ranging (LiDAR) sensor data, which degrades the quality of the point clouds significantly. To address this issue, this letter presents a novel point cloud adverse weather denoising deep learning algorithm (4DenoiseNet). Our algorithm takes advantage of the time dimension unlike deep learning adverse weather denoising methods in the literature. It performs about 10% better in terms of intersection over union metric compared to the previous work and is more computationally efficient. These results are achieved on our novel SnowyKITTI dataset, which has over 40000 adverse weather annotated point clouds. Moreover, strong qualitative results on the Canadian Adverse Driving Conditions dataset indicate good generalizability to domain shifts and to different sensor intrinsics.

### 逐句解构与功能标注

| 编号 | 原文                                                                                                                                                                          | 功能标注                     |
| -- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------ |
| S1 | Reliable point cloud data is essential for perception tasks e.g. in robotics and autonomous driving applications.                                                           | **背景铺垫/重要性声明**：建立研究的宏观意义 |
| S2 | Adverse weather causes a specific type of noise to light detection and ranging (LiDAR) sensor data, which degrades the quality of the point clouds significantly.           | **问题定义**：明确指出待解决的核心问题    |
| S3 | To address this issue, this letter presents a novel point cloud adverse weather denoising deep learning algorithm (4DenoiseNet).                                            | **贡献声明**：正式提出本文方法        |
| S4 | Our algorithm takes advantage of the time dimension unlike deep learning adverse weather denoising methods in the literature.                                               | **核心差异化**：与已有方法的关键区别     |
| S5 | It performs about 10% better in terms of intersection over union metric compared to the previous work and is more computationally efficient.                                | **量化结果摘要**：性能优势的数字化呈现    |
| S6 | These results are achieved on our novel SnowyKITTI dataset, which has over 40000 adverse weather annotated point clouds.                                                    | **数据贡献声明**：附带贡献——新数据集    |
| S7 | Moreover, strong qualitative results on the Canadian Adverse Driving Conditions dataset indicate good generalizability to domain shifts and to different sensor intrinsics. | **泛化能力声明**：强调实用价值        |

### 深度分析

**S1** 的写法非常典型——用一句不可反驳的共识性陈述开场。"Reliable point cloud data is essential" 属于领域内公理级别的判断，任何审稿人都不会对此产生异议。这种策略的目的是快速与读者建立共同基础（common ground），让读者进入作者预设的逻辑轨道。注意 "e.g. in robotics and autonomous driving applications" 的使用，"e.g." 表明应用场景不限于此，但特意点出了机器人和自动驾驶这两个热门且资金充裕的领域，这是对论文**影响力范围**的隐性定位。

**S2** 承接S1，从"可靠数据很重要"自然过渡到"恶劣天气破坏了这种可靠性"。逻辑链条为：重要的东西被破坏了→这是一个值得解决的问题。"a specific type of noise" 这个表述很精准——作者有意将恶劣天气噪声与一般性点云噪声区分开，为后文强调需要**专门方法**（而非通用去噪）埋下伏笔。"significantly" 这个程度副词强化了问题的严重性，为研究必要性加码。

**S3** 是标准的贡献声明句，"To address this issue" 直接回扣S2的问题。"novel" 一词是学术论文中声明新颖性的标准用词。值得注意的是，作者在摘要中就完成了方法命名——"4DenoiseNet"，这个名字本身就是信息压缩：4D暗示时空维度，DenoiseNet直指任务。好的方法命名能在读者心智中建立快速索引。

**S4** 是整个摘要中**最关键的差异化句子**。"takes advantage of the time dimension" 精确指出了技术贡献的核心点。"unlike deep learning adverse weather denoising methods in the literature" 直接将本文方法与所有已有深度学习方法进行对立。这种 "unlike X" 的句式是学术写作中建立novelty的经典手法——不仅说"我做了什么"，更说"我做了别人没做的什么"。这里隐含的逻辑是：已有的深度学习方法忽略了时间维度，而这恰恰是本文成功的关键。

**S5** 提供了量化证据支撑S4的声明。"about 10%" 用了近似表述，这在摘要中是合理的——避免过度精确导致读者质疑特定实验条件。同时提出了两个优势维度：准确性（IoU提升约10%）和效率（computationally efficient），这是一种"双赢"叙事——不是以牺牲速度换精度，而是两者兼优。

**S6** 引入了第二个贡献——SnowyKITTI数据集。"over 40000" 这个数字的作用是传递规模感，暗示数据集足够大以支持可靠的训练和评估。将数据贡献放在摘要中是一个策略性选择：它增加了论文的可引用维度（其他研究者可能仅为使用数据集而引用本文）。

**S7** 以"Moreover"递进，引入泛化性论证。这里有两个关键信息点：（1）在真实数据集（CADC）上的定性结果良好；（2）能够跨域迁移（domain shifts）和适应不同传感器参数（different sensor intrinsics）。这一句回应了审稿人可能提出的最大质疑——"你用仿真数据训练，在真实场景中能用吗？"作者提前在摘要中就给出了肯定回答。

### 结构总结与迁移指导

本摘要遵循了经典的 **"背景→问题→方法→差异化→结果→附加贡献→泛化"** 七步结构。可迁移的核心原则：

1. **开头用共识性陈述建立信任**，不要以争议性观点开场。
2. **差异化声明必须明确且具体**——不是泛泛地说"我们的方法更好"，而是说"我们利用了X，这是别人没做的"。
3. **量化结果在摘要中要适度概括**，给出数量级即可，细节留给正文。
4. **提前回应最大质疑**——如果你的方法有明显的潜在弱点（如sim-to-real gap），在摘要中就需要主动给出答案。
5. **附加贡献（如数据集）可以提升论文的引用潜力**，值得在摘要中占一席之地。

---

## I. Introduction 解析

Introduction较长，我按段落逐一分析。

### 第一段

#### 原文呈现

> ADVERSE weather conditions can have a huge impact on light detection and ranging (LiDAR) sensor data. Airborne particles, such as rain droplets [1], [2], [3], fog [1], [3], [4], [5], or snowflakes [3], [6], [7], [8], [9] cause undesired reflections, refractions, and absorptions of the laser, which results in missing and cluttered points. This is a major problem since point clouds are often used for determining the open volume of the environment, e.g. autonomous robots use point clouds for obstacle avoidance. Moreover, the clutter also affects other downstream perception algorithms, such as object detection [10], [11], [12], [13], which are an essential component of autonomous road vehicles. Thus, robust perception data in adverse weather is crucial as fatality rates for human drivers are notably higher in such conditions, as reported by the European Commission [14] and the US Department of Transportation [15].

#### 逐句解构与功能标注

| 编号 | 功能标注                       |
| -- | -------------------------- |
| S1 | **问题域声明**：恶劣天气对LiDAR的影响    |
| S2 | **问题细化+文献群引**：具体化噪声来源与物理机制 |
| S3 | **影响阐述（直接）**：噪声对基础任务的影响    |
| S4 | **影响阐述（间接/级联）**：噪声对下游算法的影响 |
| S5 | **社会意义升华+权威背书**：与人命安全挂钩    |

#### 深度分析

**S1** 是摘要S1-S2的展开版。注意 "huge impact" 的用法——在Introduction中使用略带感情色彩的表述是被允许的（摘要中更克制），目的是制造紧迫感。

**S2** 是本段信息密度最高的句子。作者将恶劣天气细分为三类——雨、雾、雪——并为每类配备了密集的引用群。这种写法的深层目的不仅仅是"列举"，而是**展示作者对领域的全面掌握**。

引用分析：

* **[1] Wallace et al.** 同时出现在rain和fog中，说明这是一篇涵盖多种天气条件的综合性研究。
* **[3] Bijelic et al. (2020)** 出现在所有三类中，是一篇核心的多模态感知论文，在此作为恶劣天气影响LiDAR的"全景式"证据。
* **[2] Goodin et al.** 专注于雨对LiDAR的影响。
* **[4] Bijelic et al. (2018)**, **[5] Heinzler et al. (2019)** 专注于雾。
* **[6]-[9]** 四篇聚焦于雪。雪的引用数量最多（4篇），这不是偶然——本文的实验重点正是雪，作者通过引用密度**预先强调雪的研究重要性和已有研究基础**。

物理机制描述 "undesired reflections, refractions, and absorptions" 是精确的光学术语，展示了作者对问题物理本质的理解。"missing and cluttered points" 指出了两种互补的降质模式——点的丢失和点的杂乱。

**S3-S4** 构成了一个影响力递进结构：S3谈**直接影响**（点云本身不可靠→障碍物检测出错），S4谈**级联影响**（下游目标检测算法受损）。引用[10]-[13]均为3D目标检测在恶劣天气下的研究，其中[12] Hahner et al. (CVPR 2022) 是本文训练数据仿真模型的来源（后文会揭示），在此先以"受影响的下游任务"角色出场，后文再以"方法工具"角色出场——一篇文献在不同语境中承担不同角色，这是成熟引用策略的体现。

**S5** 将问题从技术层面升华到**社会安全层面**。引用欧盟委员会[14]和美国交通部[15]——两个**政府权威机构**的数据。这种策略的目的是：（1）不容置疑的权威性；（2）暗示此研究有政策和社会层面的需求，提升论文的影响力叙事。"fatality rates" 一词直接将读者的注意力从技术问题引向人命关天的紧迫感。

### 第二段

#### 原文呈现

> Our task is to remove points from LiDAR point clouds that are caused by airborne particles. The motivation for this is to provide clean point cloud data for all downstream tasks e.g. mapping, localization, object detection, and navigation. Previous work uses either a classical approach [16], [17], [18], [19], [20] or a learned approach [21]. Unlike previous work, our work utilizes spatial-temporal data as an input to a neural network. We do this by feeding adjacent point clouds (P^{(t)} \in \mathbb{R}^{n \times 3}) and (P^{(t-1)} \in \mathbb{R}^{n \times 3}) to a novel neural network that predicts the points that are caused by airborne particles. Then the predictions are used for removing these points from the point cloud, yielding a clean point cloud (\tilde{P}^{(t)}). The neural network architecture can be optimized for multiple types of adverse weather e.g. rain, fog, and snowfall. Moreover, our algorithm is also tested with more challenging clutter caused by light, medium, and heavy snowfall, whereas previous work [21] was tested only in fog and rain. We obtained better performance than WeatherNet [21] and general-purpose state-of-the-art semantic segmentation networks [22], [23]. Furthermore, the experiments show that our model generalizes better to other adverse weather conditions.

#### 逐句解构与功能标注

| 编号  | 功能标注                   |
| --- | ---------------------- |
| S1  | **任务定义**：精确界定本文任务边界    |
| S2  | **动机声明**：解释任务的实用价值     |
| S3  | **文献二分法**：将已有工作划分为两大阵营 |
| S4  | **核心差异化声明**（与摘要S4呼应）   |
| S5  | **方法概述**：技术流程的高层描述     |
| S6  | **结果呈现**：从输入到输出的完整管道   |
| S7  | **通用性声明**：适用于多种天气      |
| S8  | **实验范围对比**：暗示本文实验更全面   |
| S9  | **性能声明**：胜过已有方法        |
| S10 | **泛化性声明**              |

#### 深度分析

**S1** 开门见山——"Our task is to remove points..."。这种直接定义任务的方式在工程导向的论文中非常有效。注意措辞是 "remove points...caused by airborne particles"，而不是更模糊的 "denoise point clouds"。精确的任务定义帮助审稿人理解评估标准。

**S3** 使用了**二分法（dichotomy）**策略："either a classical approach...or a learned approach"。引用[16]-[20]归为classical，[21]归为learned。这种分类的巧妙之处在于：learned approach只有**一篇**（WeatherNet [21]），这直接传递了一个信息——**深度学习在这个细分领域几乎是空白**，本文是先驱之一。如果已有learned approaches很多，作者就需要更细致地区分差异化。

**S4** 再次使用 "Unlike previous work" 这个对比句式，与摘要S4几乎平行。在Introduction中重复强调核心novelty是必要的——因为很多审稿人只读Abstract和Introduction来形成初步判断。

**S5** 引入了数学符号 (P^{(t)} \in \mathbb{R}^{n \times 3}) 和 (P^{(t-1)} \in \mathbb{R}^{n \times 3})，在Introduction中就使用形式化表示是一个信号：本文不是纯应用文章，而是有严谨的数学建模。同时，"adjacent point clouds" 的概念在此首次形式化，清晰传达了"时间维度"的具体含义——不是整个视频序列，而是**相邻两帧**。

**S8** 做了一个精心设计的**范围对比**——"whereas previous work [21] was tested only in fog and rain"。"only" 一词是关键——暗示WeatherNet的实验不够全面。本文测试了 "light, medium, and heavy snowfall"，这个三级划分显示了更系统的实验设计。

引用[21] (WeatherNet) 在此段出现了两次（S3和S8），这是因为它是**最直接的竞争对手**（唯一的deep learning baseline）。引用[22] (SalsaNext) 和 [23] (Cylinder3D) 是通用语义分割网络，作者将其纳入比较范围的策略是：即使把通用的强力方法拿来做这个任务，也不如我们的专用方法。

### 第三段

#### 原文呈现

> The problem of removing noise caused by adverse weather is not trivial because of the nature of the LiDAR sensor, the sparsity of the point cloud, occlusions caused by the noise, and the varying density of the noise. This leads to statistical or hard-coded filters [16], [17], [18], [19], [20] to remove valid points and preserve the clutter. To address this problem, we use a deep learning architecture that learns an equivariance function. A deep learning method is also able to utilize the complex patterns of adverse weather noise. Due to the nature of the LiDAR sensor, the reflectance and position of solid structures affect the pattern of the noise. Our method is trained with partly simulated semi-synthetic data. Since labels are "free lunch" from the simulation, the training set can be built effortlessly, and our model can be trained in a supervised manner. However, we want to emphasize that our model is tested quantitatively with real data captured in adverse weather. The tests indicate that our model generalizes to real data and also to different sensor intrinsics.

#### 逐句解构与功能标注

| 编号 | 功能标注                 |
| -- | -------------------- |
| S1 | **难度论证**：解释为什么问题不简单  |
| S2 | **已有方法的失败原因**        |
| S3 | **方法正当性论证**：为什么用深度学习 |
| S4 | **方法优势补充**           |
| S5 | **物理依据**：噪声模式的复杂性根源  |
| S6 | **训练策略声明**：半合成数据     |
| S7 | **训练策略优势**：标注成本低     |
| S8 | **主动防御**：强调在真实数据上测试  |
| S9 | **泛化性重申**            |

#### 深度分析

**S1** 列举了四个困难因素：传感器本身特性、点云稀疏性、噪声遮挡、噪声密度变化。这种**列举式难度论证**的目的是让审稿人认识到："这不是一个简单的滤波问题"。越是让审稿人理解问题的难度，越能提升解决方案的价值感知。

**S2** 精准指出经典方法的失败模式——"remove valid points and preserve the clutter"，即误删真实点、保留噪声点。这里再次引用[16]-[20]，但角色从第二段的"分类标签"变为"失败案例"。同一组引用在不同语境下服务于不同论证目的。

**S3** 中 "equivariance function" 是一个值得注意的术语选择。严格来说，这里的等变性指的是网络学习到的映射对输入的某些变换具有一致的响应。但在这个语境中，它更像是在说"网络能学到稳健的模式"。这个术语的使用提升了方法描述的数学严谨感。

**S6-S8** 构成了一个精心设计的**"先承认后反驳"**结构。S6承认使用了仿真数据（这是审稿人会质疑的点），S7将其包装为优势（"free lunch"——标签几乎零成本），S8用 "However, we want to emphasize" 这个强转折句式，主动引导读者注意到真实数据测试的事实。"we want to emphasize" 这个表述在学术论文中较少见——它传递了一种作者的**主观意愿和坚持**，暗示作者预料到了审稿人的质疑并希望提前化解。

### 第四段

#### 原文呈现

> We show that the key to robust adverse weather denoising is the efficient utilization of spatial-temporal data. Spatial information, in metric space, is useful because clutter has a relatively low density. Temporal information is crucial because valid points follow predictable trajectories. Contrarily, noise points caused by airborne particles have a chaotic nature. Our architecture exploits these phenomena by a k-nearest neighbor convolution kernel that captures spatial-temporal information, and with a motion-guided attention mechanism.

#### 逐句解构与功能标注

| 编号 | 功能标注              |
| -- | ----------------- |
| S1 | **核心洞见声明**        |
| S2 | **空间信息的价值解释**     |
| S3 | **时间信息的价值解释**     |
| S4 | **对比论证**：噪声的混沌特性  |
| S5 | **架构概述**：如何利用上述洞见 |

#### 深度分析

这一段是全文的**核心直觉（intuition）段落**。S1提出了一个强有力的命题——"the key to robust adverse weather denoising is..."。使用 "the key" 而非 "a key" 表明作者认为这是**决定性因素**而非众多因素之一。

**S2-S4** 构成了一个美观的**对称论证结构**：

* 空间维度：噪声密度低 → 可以通过局部密度判断
* 时间维度：有效点轨迹可预测 vs 噪声点运动混沌

"Contrarily"（S4）这个转折词建立了一个清晰的二元对立——有效点可预测，噪声点混沌。这种物理直觉的清晰阐述是说服审稿人的关键：在展示数学和实验之前，先让读者相信**你的方法在物理上是合理的**。

**S5** 将直觉映射为技术实现——kNN卷积核捕捉时空信息，运动引导注意力机制（MGA）融合特征。

### 第五段（Contribution声明）

#### 原文呈现

> Our contribution is two-fold.
>
> * We present the first deep learning approach for LiDAR adverse weather denoising utilizing spatial and temporal information. This is realized with a novel k-nearest neighbors search convolution on consecutive point clouds, which captures spatial and temporal information. We surpass existing methods in performance by a large margin, with a lower computational cost.
> * Since point-wise annotations are laborious, we train with semi-synthetic data generated by a highly realistic physics-based model [12]. That is, synthetic effects of adverse weather are added to real point clouds captured in clear weather. We are the first to use this data to train a model and test its performance on real data, captured in adverse weather. The excellent performance indicates that our model is robust in this domain shift. Given the excellent performance, our model will be an essential component in outdoor LiDAR sensor applications, enabling clean perception data for all downstream tasks. Moreover, we present the first point-wise annotated adverse weather dataset, i.e. SnowyKITTI, based on this simulation model which has approximately 40000 LiDAR scans.

#### 逐句解构与功能标注

**贡献1：**

| 编号    | 功能标注                  |
| ----- | --------------------- |
| C1-S1 | **先驱性声明**："the first" |
| C1-S2 | **技术具体化**             |
| C1-S3 | **性能优势声明**            |

**贡献2：**

| 编号    | 功能标注                                      |
| ----- | ----------------------------------------- |
| C2-S1 | **训练策略动机**                                |
| C2-S2 | **训练策略解释**                                |
| C2-S3 | **先驱性声明**："the first to use this data..." |
| C2-S4 | **鲁棒性声明**                                 |
| C2-S5 | **愿景声明**：展望应用价值                           |
| C2-S6 | **数据集贡献**                                 |

#### 深度分析

"Our contribution is two-fold" 是Robotics/CV领域最经典的贡献声明句式。用 "two-fold" 明确限定贡献数量，给审稿人一个清晰的检查清单。

**贡献1** 中 "the first deep learning approach...utilizing spatial and temporal information" 是一个极强的优先权声明。"the first" 在学术论文中是最有力的novelty词汇，但也最容易被审稿人反驳。作者在此使用它是有底气的——因为当时确实没有利用时间维度的深度学习恶劣天气去噪方法。"by a large margin" 进一步强化了性能优势。

**贡献2** 中引用[12] (Hahner et al., CVPR 2022) 扮演的角色是**方法工具**——提供了用于生成训练数据的物理仿真模型。这与第一段中[12]作为"受天气影响的目标检测工作"的角色完全不同。再次出现了**同一引用的角色转换**。

"The excellent performance indicates that our model is robust in this domain shift" 和 "our model will be an essential component" 这两句的语气非常自信，几乎到了学术写作的舒适区边缘。"will be an essential component" 是一个**愿景声明（vision statement）**，这在Letters格式中可以接受，因为篇幅限制下需要在有限空间内建立最大影响力。

### 结构总结与迁移指导

本Introduction遵循了**"宏观问题→问题具体化→已有方法分类→本文差异化→核心直觉→技术概述→贡献列表"**的经典结构。可迁移的核心原则：

1. **Introduction第一段建立问题的社会重要性**，引用权威机构数据是加分项。
2. **将已有方法进行二分法或多分法分类**，然后指出你的方法所在的类别中的空白。
3. **在展示技术细节之前，先阐述物理直觉**——让读者理解"为什么你的方法应该work"。
4. **对方法的弱点（如使用仿真数据）主动承认并转化为优势**，而不是回避。
5. **贡献声明要具体、可核实**——"the first to do X" 比 "a new method for Y" 强得多，但前提是确实属实。
6. **同一篇参考文献可以在不同段落承担不同论证角色**——这是高级引用策略。

---

## II. Related Work 解析

### 开头段

#### 原文呈现

> Adverse weather denoising from sparse LiDAR point clouds is an emerging field, and only a handful of studies have been conducted. Dense point cloud denoising is a more established field but the methods have not been tested for denoising adverse weather in sparse point clouds. Therefore, we do not cover that area of research.

#### 逐句解构与功能标注

| 编号 | 功能标注           |
| -- | -------------- |
| S1 | **领域定位+稀缺性声明** |
| S2 | **相邻领域排除**     |
| S3 | **综述范围限定**     |

#### 深度分析

**S1** "an emerging field" 和 "only a handful of studies" 是两个关键信号。"emerging" 暗示该领域处于早期阶段——这对作者有利，因为在新兴领域发表的工作更容易成为 "foundational"。"only a handful" 直接告诉审稿人：你不必期待一个冗长的文献综述。

**S2-S3** 预防了一个可能的审稿意见——"为什么不讨论dense point cloud denoising？"。作者主动解释：那些方法没有在sparse LiDAR上验证过，所以不相关。"Therefore, we do not cover that area" 是一个干净的范围切割。这种写法是成熟的——提前封堵审稿人的潜在追问。

### A. Classical Approaches

#### 原文呈现

> Typically, the clutter caused by adverse weather has a relatively low density. Radius outlier removal (ROR) and statistical outlier removal (SOR), presented in [24], remove outliers based on local density. ROR removes points that do not have another point in distance r. SOR computes the mean distance to k nearest neighbors and decides if a point is an outlier based on the global mean distance between the points and the standard deviation. These methods do not work well with point clouds that have inherently varying density, e.g. LiDAR point clouds whose density is proportional to the measured range. This leads to the removal of distant points, and therefore these methods are not suited for adverse weather denoising.

> Charron et al. [16] proposed dynamic radius outlier removal (DROR) which adjusts the distance r based on the range of the point from the sensor. They achieved good results in removing points caused by snowfall. Dynamic statistical outlier removal (DSOR) [17] combines SOR and DROR. It removes outliers based on a threshold that is defined by the global mean distance between the points and the standard deviation and the measured range of the point. Low-intensity outlier removal (LIOR) [18] is designed to remove points caused by snowfall. The threshold is derived from LiDAR-measured intensity, and it is a function of the measured range. LIOR includes the ROR filter for preserving points that have low intensity but high density. That is, LIOR takes advantage of the typical low intensity and density of airborne snowflakes. However, valid points are removed from light-absorbent and semi-transparent surfaces. Dynamic distance–intensity outlier removal (DDIOR) [19] fuses DSOR and LIOR to achieve better performance. Li et al. utilized spatial-temporal features for removing points caused by snowfall [20]. They showed that temporal information is valuable in this task by performing well compared to other methods. Their method thresholds points to relative distances in W-T-space where W and T denote spatial dimensions and time, respectively.

#### 深度分析

第一段建立了一个**"从通用到失败"**的叙事。先介绍ROR和SOR [24]（PCL库的基础方法），然后指出它们在LiDAR场景下的致命缺陷——LiDAR点云密度随距离变化，这导致远处的有效点被误删。引用[24] (Rusu & Cousins, PCL) 是点云处理领域的经典引用，在此作为"原始工具"角色出场。

第二段按时间线梳理了经典方法的**演进路径**：

* **DROR [16]**：调整距离阈值→部分解决了密度变化问题
* **DSOR [17]**：融合SOR和DROR
* **LIOR [18]**：利用强度信息→但对吸光和半透明表面失效
* **DDIOR [19]**：融合DSOR和LIOR

这种叙事呈现了一个**方法叠加但问题未根本解决**的图景——每个新方法修补了前一个方法的缺陷，但又引入了新的局限。这种 "patch upon patch" 的叙事暗示：经典方法的路径已经接近天花板，需要范式转换（即深度学习）。

**[20] Li et al.** 是一个特殊的引用——他们也使用了时空特征。作者坦率地承认 "They showed that temporal information is valuable in this task"，这与本文的核心主张一致。但注意：Li et al. 用的是**经典阈值方法**（"thresholds points to relative distances in W-T-space"），而不是深度学习。所以本文的novelty仍然成立——"第一个用深度学习利用时空信息的方法"。引用[20]的策略是：承认其贡献，但明确指出方法范式的差异。

### B. Learned Approaches

#### 原文呈现

> Since our method is based on segmentation with a neural network, we present related work from this area. LiDAR point cloud semantic segmentation networks are focusing on general segmentation, and they can be trained to segment highly abstract shapes. Most successful approaches use voxelized [23], [25], bird's eye view [26], or spherical projection input [27], [28], [29], [30]. However, raw point input approaches exist as well [31], [32], [33], [34], [35], [36], [37], [38]. Cylinder3D [23] parts the point cloud into cylindrical voxels. Then a 3D convolutional neural network extracts features and produces the predictions. PolarNet [26] uses a bird's eye view pseudo image representation for feature extraction. Spherical projection image input is beneficial for memory usage because of the dense representation [22], [39]. Another benefit of the projection image is that a 2D convolutional neural network can be used for feature extraction. However, 2D convolution kernels fail to capture local spatial information accurately due to the nature of the projection. Work by Xu et al. combines projection, voxel, and point inputs to produce more accurate segmentation results [40].

> The semantic segmentation networks are well-proven and general-purpose. Thus, they can be trained for segmenting the clutter caused by adverse weather. However, they require a lot of labeled training data, memory, and computational power due to the enormous amount of trainable parameters. Recent work by Heinzler et al. [21] proposed the WeatherNet, an optimized semantic segmentation network for segmenting the clutter caused by fog and rain. Their method has a significantly lower amount of trainable parameters while having equal or even better performance compared to the state-of-the-art general-purpose segmentation networks. While their work is focused on segmenting the clutter caused by rain and fog, our method presents a novel spatial-temporal feature encoder and benchmarks the performance of light, medium, and heavy snowfall, which causes more severe clutter. Furthermore, our method has only 0.6 M trainable parameters while theirs has 1.5 M. Therefore, our method generally requires less labeled data and generalizes better.

#### 深度分析

**第一段**按输入表示方式将语义分割网络分为四类：体素化[23][25]、鸟瞰图[26]、球面投影[22][27]-[30][39]、原始点输入[31]-[38]。引用量巨大——这段引用了约20篇文献。这种密集引用的目的是**展示全面的领域视野**，同时为读者提供一个关于LiDAR分割的入门索引。

关键的转折出现在 "However, 2D convolution kernels fail to capture local spatial information accurately" 这句话。作者在综述球面投影方法时特意指出其缺陷——因为本文正是基于球面投影的，而kNN卷积正是为了解决这个缺陷。这是一个精心设计的**铺垫**：在Related Work中指出问题，在Methods中给出解决方案。引用[41] (Sirohi et al.) 支持了2D卷积失效的论点。

**第二段**聚焦于最直接的竞争者WeatherNet [21]。叙事策略是**先肯定后超越**：

1. 肯定："Their method has a significantly lower amount of trainable parameters while having equal or even better performance"
2. 指出局限："their work is focused on...rain and fog"（隐含：范围较窄）
3. 超越："our method presents a novel spatial-temporal feature encoder"
4. 量化优势："our method has only 0.6M trainable parameters while theirs has 1.5M"

最后一句 "Therefore, our method generally requires less labeled data and generalizes better" 使用了 "Therefore" 进行因果推理——参数少→需要的数据少→泛化更好。这个推理链条在机器学习中是合理的（Occam's razor），但 "generally" 这个限定词保留了适度的谨慎。

### 结构总结与迁移指导

Related Work部分遵循了**"范围限定→经典方法演进→经典方法的天花板→深度学习方法分类→直接竞争者的优缺点→本文的定位"**结构。核心迁移原则：

1. **开头主动限定综述范围**，解释为什么不讨论看似相关的领域。
2. **经典方法应按演进路径叙述**，展示"问题一直没有被根本解决"的图景。
3. **在Related Work中为Methods埋伏笔**——指出已有方法的缺陷，恰好是你后文解决的问题。
4. **对最直接竞争者要"先肯定后超越"**——不贬低他人的工作，而是清晰地指出你的额外贡献。
5. **参数量对比是轻量级模型论文中的有力武器**——但要注意连带给出性能对比，避免给人"轻量但弱"的印象。

---

## III. Methods 解析

### A. Ordered Point Cloud Representation

#### 原文呈现

> Point coordinates from a typical LiDAR sensor (c = (x, y, z)) are mapped (\Gamma : \mathbb{R}^{n \times 3} \rightarrow \mathbb{R}^{s_h \times s_w \times 3}) to spherical coordinates, and finally to image coordinates, as defined by
> [\binom{u}{v} = \binom{\frac{1}{2}(1 - \tan^{-1}(yx^{-1})\pi^{-1})s_w}{(1 - (\sin^{-1}(z|c|^{-1}) + f_{vup})f_v^{-1})s_h}]
> where ((s_h, s_w)) are the height and width of the desired projection image representation, (f_v) is the total vertical field-of-view of the sensor, and (f_{vup}) is the vertical field-of-view spanning upwards from the horizontal origin plane. The resulting list of image coordinates is used to construct a ((x, y, z))-channel image i.e. ordered point cloud (P_o \in \mathbb{R}^{s_h \times s_w \times (3+C_f)}), where (C_f) denotes the number of feature channels, in our case, (C_f = 1) for intensity.

#### 深度分析

这一节定义了从3D点云到2D投影图像的映射 (\Gamma)。公式(1)是LiDAR球面投影的标准公式——将笛卡尔坐标 ((x,y,z)) 转换为像素坐标 ((u,v))。这不是本文的原创，而是LiDAR语义分割领域的**通用前处理步骤**（如RangeNet++, SalsaNext等都使用类似表示）。

作者在此给出形式化定义的目的是：（1）明确后续kNN卷积操作的输入数据格式；（2）建立符号系统，后文可直接使用 (P_o)。"(C_f = 1) for intensity" 指明了额外特征通道是LiDAR反射强度，这在后续的domain shift实验中是一个关键变量——不同传感器的强度分布不同。

### B. Utilization of Spatial Information

#### 原文呈现

> Classical methods DROR [16], DSOR [17], and DDIOR [19] show that local point density is a useful indicator for determining if a given point is caused by an airborne particle. Therefore, enabling the neural network to capture this information is crucial. Since our method is projection-based and a traditional convolution fails to capture local points [41], a measure has to be taken. We define the first convolution layer to capture k-nearest neighbors (kNN) in metric space via kNN-convolution. An illustrative schematic is presented in Fig. 1. This convolution kernel considers the closest k points in the metric space instead of the neighboring points based on the pixel coordinates, enabling better spatial information for the network. To mitigate the computational burden of the kNN-search, we search only in the neighboring area of the anchor point in the ordered point cloud. We show an improvement compared to a traditional convolution in an ablation study (Section IV-C).

然后给出公式(2)-(4)。

#### 深度分析

这一节的叙事结构非常优雅：**从已有方法的观察出发，推导出设计决策**。

S1引用[16][17][19]（经典方法）不是为了批评它们，而是为了**借用它们的洞见**——局部点密度是有用的判据。这种写法体现了学术传承：即使你的方法是全新的范式，也应该承认前人的启发。

S2-S3构成了**问题-解决方案**对：问题是球面投影+传统卷积无法捕获度量空间中的局部点（引用[41]支持），解决方案是kNN卷积。

公式(3)定义了空间kNN卷积。核心思想是：对于锚点 (\vec{p})，不是取投影图像上的相邻像素，而是在度量空间（range通道）中搜索最近的k个点。公式(4)中的 (\vec{\xi}) 限制了搜索范围，这是计算效率的关键——不做全局kNN搜索，只在局部邻域内搜索。

"We show an improvement compared to a traditional convolution in an ablation study (Section IV-C)" 是一个**前向引用**——在Methods中承诺，在Experiments中兑现。这种写法给审稿人一个心理预期："这个设计选择是有实验验证的"。

### C. Utilization of Temporal Information

#### 原文呈现

> The effects of adverse weather in LiDAR point clouds have a more chaotic nature than valid points. This is caused by a reflection of the beam from an airborne particle. The reflections caused by these particles are more unpredictable since they are small and are moved by turbulent airflow. This chaotic behavior is on a much smaller scale in other points. Thus, temporal information can be utilized in our task. An empirical study shows that a reflection from an airborne particle, e.g. snowflake, is extremely unlikely to be occurring twice in the same place. That is, a single beam reflected from an airborne particle is highly unlikely to occur in the adjacent scan for a given beam, whereas reflections of other surfaces are more predictable.

然后介绍时间kNN卷积公式(5)-(6)以及球面坐标变换公式(7)。

#### 深度分析

这一节开头的物理论证是全文最有说服力的段落之一。逻辑链条：

1. 气象粒子体积小、受湍流气流驱动 → 反射不可预测
2. 相邻帧中，气象噪声几乎不可能出现在同一位置 → 噪声点缺乏时间一致性
3. 固体表面的反射是可预测的 → 有效点具有时间一致性
4. 结论：时间维度可以区分噪声和有效点

这个论证之所以有力，是因为它从**第一性原理（first principles）**出发——不是说"时间信息经验上有效"，而是解释了"物理上为什么时间信息应该有效"。

公式(5)定义了时间kNN卷积。关键设计是 (\mathbf{d} = \mathbf{a} - \mathbf{k}^{(t-1)})，即当前帧的锚点与前一帧kNN点之间的差值。这个差值近似了局部运动。公式(7)将差值从笛卡尔坐标转换为球面坐标 ((r, \theta, \phi))——这一步的动机是将运动分解为幅值（距离变化）和方向，这种表示更自然地反映了LiDAR感知场景中的几何关系。

### D. Neural Network Design and Training

#### 原文呈现

> Based on the above insights, a function that captures both spatial and temporal features should have superior performance over its counterparts. We approximate this function by a novel neural network, namely 4DenoiseNet (Fig. 3), where 4D is a reference to time as the fourth dimension. It has two branches: spatial and temporal. The spatial branch processes the spatial features of the current point cloud (P^{(t)}), and the temporal branch processes the temporal features of the previous point cloud (P^{(t-1)})...

然后介绍MGA、残差块、损失函数等。

#### 深度分析

这一节的结构清晰地遵循了**"洞见→架构→训练"**的叙事。

**双分支设计**（空间分支+时间分支）直接映射了III-B和III-C的两个洞见。这种**设计与直觉的一一对应**是审稿人喜闻乐见的——你的每一个架构选择都有明确的动机。

**MGA (Motion Guided Attention)**引用了[43] (Li et al., ICCV 2019)，这是一篇视频显著性检测论文。从视频处理领域借鉴运动引导注意力机制到LiDAR时序处理，这是一个**跨领域迁移**的设计选择。引用[43]的角色是"方法借鉴"——作者没有声称MGA是自己发明的，而是明确指出了来源。

损失函数由两部分组成：Lovász-Softmax损失[44]和标准交叉熵损失。Lovász-Softmax直接优化IoU指标（即Jaccard Index [45]），这是一个务实的选择——评价指标用什么，损失函数就优化什么。引用[44]和[45]分别提供了损失函数和评价指标的学术来源。

残差块设计引用了[22] (SalsaNext) 和 [42] (SalsaNet)，说明编码器部分的设计受到了这两篇工作的启发。这体现了学术诚实——明确声明哪些组件是借鉴的，哪些是原创的。

### 结构总结与迁移指导

Methods部分遵循了**"数据表示→空间特征提取→时间特征提取→整体架构与训练"**的递进结构。核心迁移原则：

1. **每个架构设计选择都应有明确的动机**——理想情况下从物理直觉或已有方法的观察推导。
2. **从第一性原理论证比纯经验论证更有说服力**——"物理上为什么应该work"比"实验上work了"更能打动审稿人。
3. **跨领域借鉴要明确引用来源**，既展示了广阔视野，又保持了学术诚信。
4. **在Methods中嵌入前向引用（指向ablation study）**——给审稿人信心：你的设计选择会在实验中得到验证。
5. **评价指标与损失函数的一致性**是实验设计的基本功。

---

## IV. Experiments 解析

### A. Experimental Setup

#### 原文呈现

> **Datasets:** We conduct qualitative tests on the Canadian Adverse Driving Conditions dataset [46]. It is captured in real-world adverse weather conditions which include light, medium, heavy, and extreme snowfall. Since this dataset does not have point-wise annotations, we train our model on our SnowyKITTI dataset. SnowyKITTI is a modified KITTI odometry benchmark dataset [47] with synthetic snowfall created with a highly realistic physics-based simulation model presented in [12]...

> **Evaluation metrics:** We use the Jaccard index [45] i.e. IoU...We are only interested in the IoU value of the noise class.

> **Training and inference details:** The parameters of the network are optimized with the Adam optimizer [48]. We fix the spatial dropout probability to 0.2...

#### 深度分析

**数据集设计**是本文实验的核心创新之一。两个数据集承担不同角色：

* **SnowyKITTI**（训练+定量测试）：基于KITTI [47]（自动驾驶领域最经典的benchmark之一），使用[12]的物理仿真添加合成降雪。引用[47]提供了基础数据来源的权威性，引用[12]提供了仿真方法的可信度（CVPR 2022）。
* **CADC [46]**（定性测试）：真实恶劣天气数据，无逐点标注。

这种"用仿真数据训练、用真实数据测试"的策略巧妙地回应了sim-to-real gap的质疑。Table I的训练子集划分（不同降雪强度的组合）是一个精心设计的实验变量——用于研究训练数据组成对泛化性的影响。

**评估指标**选择噪声类的IoU，而不是平均IoU或整体精度。这是因为在二分类问题中（噪声 vs 有效点），数据严重不平衡（有效点远多于噪声点），整体精度会被多数类主导。这个选择展示了对评估方法论的深入理解。

**训练细节**中引用[48] (Adam optimizer) 是标准引用。L2正则化 (\lambda = 1 \times 10^4) 和数据增强策略（随机丢点、平移、旋转、翻转）的详细列举确保了**实验可复现性**。

### B. Quantitative Results

#### 原文呈现

> The main results are presented in Table II. Our 4DenoiseNet is compared with the other adverse weather filtering model WeatherNet [21], and with general-purpose state-of-the-art semantic segmentation networks [22], [23]. The models are evaluated in terms of Jaccard index, runtime, and parameter count in Light, Medium, and Heavy snowfall...Overall our model performs the best in both accuracy and runtime. Moreover, our model has fewer trainable parameters compared to the other learned models. There is a large gap in accuracy between classical DROR and LIOR compared to learned approaches, highlighting the difficulty of this task.

> Fig. 4 presents the performance when models are trained with different training subsets...Most notably, our model is the most robust as there is a smaller variance in IoU compared to other models...

#### 深度分析

**Table II** 是全文的核心结果表。比较维度设计精当——IoU（准确性）、Runtime（效率）、Parameters（模型复杂度）三位一体。比较对象覆盖了两个维度：经典方法（DROR, LIOR）和深度学习方法（WeatherNet, SalsaNext, Cylinder3D）。

"There is a large gap in accuracy between classical DROR and LIOR compared to learned approaches" 这句话的策略是：先用经典方法的低性能衬托深度学习方法的价值，再在深度学习方法内部突出本文方法的优势。这是一种**两层对比叙事**。

**Fig. 4** 的训练子集实验是一个亮点。通过展示在不同训练集配置下各方法的IoU变化，作者不仅比较了**绝对性能**，还比较了**鲁棒性（variance）**。"our model is the most robust as there is a smaller variance" 将论证从"更准"扩展到"更稳"——这是一个额外的竞争优势维度。

关于SalsaNext在Subset2上表现与本文方法持平的讨论，作者给出了假设："it is more unlikely to overfit with Subset2 because it has more variance in conditions"。这种坦诚讨论竞争方法在特定条件下的良好表现，展现了**学术诚实**，也增强了读者对作者其他结论的信任。

### C. Ablation Study

#### 原文呈现

> To study the importance of spatial-temporal kNN-convolution, we conducted an ablation study where four 4DenoiseNet variants were compared. Table III describes the variants and their performance, runtime, and the number of trainable parameters...Based on the ablation study, the spatial kNN-convolution increases the performance slightly more than the temporal kNN-convolution. Overall, both spatial and temporal kNN-convolution modules improved the performance significantly.

#### 深度分析

消融实验（Table III）是验证Methods中设计选择的关键证据。四个变体的组合设计（有/无空间kNN × 有/无时间kNN）构成了一个 (2 \times 2) 的因子实验，这是最清晰的消融设计方式——可以独立评估每个组件的贡献以及它们的交互效应。

关键发现——"spatial kNN-convolution increases the performance slightly more than temporal kNN-convolution"——兑现了Methods中III-B和III-C所做的承诺：两者都重要，空间信息略微更重要。这与物理直觉一致：局部密度是最直接的噪声判据，时间一致性是辅助判据。

同时展示runtime影响也很重要——读者需要知道增加kNN搜索的计算开销。这预防了"性能好但代价过高"的质疑。

### D. Qualitative Results and Discussion

#### 原文呈现

> We conducted qualitative tests on real LiDAR data captured in adverse weather. The data is from the Canadian Adverse Driving Conditions dataset [46]...Fig. 5 illustrates the denoising performance...In medium and heavy snowfall, some objects are not visible in the input point cloud, but after applying our algorithm they are clearly visible. Based on visual analysis, our model does not seem to remove valid points albeit being sparse...

> To further highlight the challenge of this task, the LiDAR used from this dataset has different intrinsic parameters compared to the LiDAR used for training...Furthermore, the performance on the domain shift improves when the intensity channel is omitted...

#### 深度分析

定性实验在CADC [46]上进行，这是一个与训练数据完全不同的数据集（不同传感器、真实天气）。Fig. 5通过视觉对比（输入vs输出），让读者直观感受去噪效果。这种可视化策略在点云处理论文中非常有效——因为数字指标难以传达"恢复了之前看不到的物体"这种定性改善。

关于传感器差异的讨论（训练：0.44° vs 测试：1.25° 垂直分辨率）是一个**主动披露风险并展示鲁棒性**的策略。作者没有隐藏传感器差异，而是将其作为泛化能力的证据。

"the performance on the domain shift improves when the intensity channel is omitted" 是一个有趣的实践发现——强度信息在跨传感器迁移时会造成bias。这个发现对后续使用者非常有实用价值，体现了论文的**工程洞察**。

### 结构总结与迁移指导

Experiments部分遵循了**"实验设置→主结果→消融实验→定性分析与讨论"**的标准结构。核心迁移原则：

1. **比较对象应覆盖不同方法范式**——既有经典方法做底线，又有强力的深度学习通用方法做上界。
2. **消融实验应设计为因子实验**——(2 \times 2)或更高阶的组合设计，而非只移除单一组件。
3. **定性结果在跨域场景中特别有价值**——当目标域没有标注时，可视化是唯一的评估手段。
4. **主动披露方法的局限性**（如强度通道导致的bias），并给出解决方案——这增加了论文的可信度和实用价值。
5. **不回避竞争方法在特定条件下的良好表现**，给出合理解释即可。

---

## V. Conclusion 解析

### 原文呈现

> We presented 4DenoiseNet, the first deep learning algorithm for adverse weather denoising on adjacent LiDAR point clouds. Quantitive results on our annotated SnowyKITTI dataset, qualitative results on the Canadian Adverse Driving Conditions dataset, and runtime indicate that our model is the new state-of-the-art on adverse weather denoising. 4DenoiseNet is based on the spatial-temporal kNN-convolution module that is presented in this work. We show via ablation study the importance of spatial and temporal information in metric space in adverse weather denoising tasks. Given the light computational demand and the performance, our algorithm will be an essential component in outdoor LiDAR applications, enabling clean point cloud data for all downstream tasks. For more qualitative results we refer to our repository page.

### 逐句解构与功能标注

| 编号 | 功能标注           |
| -- | -------------- |
| S1 | **贡献重申+先驱性声明** |
| S2 | **证据概括**：三方面验证 |
| S3 | **核心技术重申**     |
| S4 | **消融研究价值重申**   |
| S5 | **愿景声明**       |
| S6 | **外部资源引导**     |

### 深度分析

**S1** 再次使用 "the first"——这与Introduction中的声明形成首尾呼应。在Conclusion中重复最强的novelty声明是标准做法，因为有些审稿人跳过中间部分直接读结论。

**S2** 将三种证据类型并列——定量结果、定性结果、运行时间——形成了"准确、可迁移、高效"的三维优势总结。"the new state-of-the-art" 是一个强有力的声明。

**S4** 特意强调消融研究的结论——空间和时间信息在度量空间中的重要性。这不仅是总结本文结果，也是为**后续研究**指明方向：未来的方法也应该重视时空信息。

**S5** 的 "will be an essential component" 与Introduction中的措辞完全一致，形成完美闭环。

注意本Conclusion**没有Future Work部分**。在Letters格式（篇幅限制严格）中，这是可以接受的。但如果是长文（如T-RO或IJRR），通常需要讨论局限性和未来方向。

### 结构总结与迁移指导

本Conclusion简短而有力，遵循了**"重申贡献→概括证据→技术核心→影响力展望"**的结构。核心迁移原则：

1. **Conclusion应与Introduction形成闭环**——使用相似的核心措辞。
2. **概括证据时要覆盖所有评估维度**，不要遗漏。
3. **Letters格式下Conclusion要极其精炼**——每句话都必须有实质信息。
4. **提供代码/数据仓库链接**是当代论文的标配，增强可复现性和影响力。

---

## 全文论证结构总图

```
问题重要性（安全、社会）
    ↓
恶劣天气对LiDAR的破坏（物理机制）
    ↓
经典方法的局限性（密度变化导致失效）
    ↓
深度学习方法的空白（无时间维度利用）
    ↓
物理直觉：噪声混沌 vs 有效点可预测
    ↓
技术实现：空间kNN + 时间kNN + MGA
    ↓
实验验证：定量(SnowyKITTI) + 定性(CADC) + 消融
    ↓
结论：新SOTA + 为未来研究指明方向
```

这篇论文的写作质量整体很高，其最大优势在于**物理直觉与架构设计的紧密对应**——每一个技术选择都有清晰的物理动机。其引用策略成熟，同一文献在不同语境中承担不同角色。作为IEEE RA-L的Letters，篇幅控制得当，论证紧凑而完整。

#### 💻 变更类型 | Change Type
- [x] feat    <!-- 引入新功能 | Introduce new features -->
- [ ] fix    <!-- 修复 Bug | Fix a bug -->
- [ ] refactor    <!-- 重构代码（既不修复 Bug 也不添加新功能） | Refactor code that neither fixes a bug nor adds a feature -->
- [ ] perf    <!-- 提升性能的代码变更 | A code change that improves performance -->
- [ ] style    <!-- 添加或更新不影响代码含义的样式文件 | Add or update style files that do not affect the meaning of the code -->
- [ ] test    <!-- 添加缺失的测试或纠正现有的测试 | Adding missing tests or correcting existing tests -->
- [x] docs    <!-- 仅文档更新 | Documentation only changes -->
- [ ] ci    <!-- 修改持续集成配置文件和脚本 | Changes to our CI configuration files and scripts -->
- [ ] chore    <!-- 其他不修改 src 或 test 文件的变更 | Other changes that don’t modify src or test files -->
- [ ] build    <!-- 进行架构变更 | Make architectural changes -->

#### 🔀 变更说明 | Description of Change
本 PR 补充并整理了 **Fundamentals of AI** 中两节无监督学习核心内容：

- Section 9：**Unsupervised Learning Algorithms（无监督学习算法）**
- Section 10：**K-Means Clustering（K 均值聚类）**

目标是形成“总览概念 → 代表算法 → 选型与评估”的连续学习路径，帮助读者先建立无监督学习框架，再落地到 K-Means 实践。

主要更新点如下：

1. 无监督学习总览（Section 9）
- 明确无监督学习与监督学习的差异：无标签数据、无显式目标输出、以发现数据结构为主。
- 梳理三类典型任务：
  - Clustering（聚类）
  - Dimensionality Reduction（降维）
  - Anomaly Detection（异常检测）
- 补充关键术语与分析视角：
  - Unlabeled Data
  - Similarity Measures（Euclidean / Cosine / Manhattan）
  - Clustering Tendency、Cluster Validity（Cohesion / Separation）
  - Dimensionality 与 Intrinsic Dimensionality
  - Anomaly 与 Outlier 区别
  - Feature Scaling（Min-Max、Z-score）
- 强调高维数据与距离度量的关系，说明特征缩放在无监督算法中的必要性。

2. K-Means 聚类方法（Section 10）
- 系统说明 K-Means 的目标：将数据划分为 K 个互不重叠簇，并最小化簇内方差。
- 梳理 K-Means 迭代流程：
  1) 初始化 K 个质心
  2) 按最近距离分配样本
  3) 更新质心为簇内均值
  4) 重复直到收敛
- 补充常用距离定义：
  - `d(x, y) = sqrt(Σ (xi - yi)^2)`（欧氏距离）
- 说明 K 选择方法：
  - Elbow Method（WCSS 拐点）
  - Silhouette Analysis（平均轮廓系数）
- 强调业务与工程因素在选 K 时的重要性：可解释性、计算成本、业务可执行粒度。

3. K-Means 数据假设与边界条件
- 说明 K-Means 适用前提：
  - 簇形状近似球形
  - 特征量纲需统一（对尺度敏感）
  - 对离群点敏感
- 明确算法局限与实践注意事项，避免“机械套用 K-Means”。

#### ✅ 价值与收益 | Benefits
- 同时覆盖无监督学习总览与代表算法，知识闭环更完整。
- 读者可从“概念理解”自然过渡到“参数选择与结果评估”。
- 为后续学习 PCA、DBSCAN、层次聚类等方法提供统一参考框架。

#### 🧪 验证说明 | Validation
- 本次为学习文档更新，不涉及运行时代码逻辑变更。
- 已完成术语、公式与章节衔接自检，确保内容一致且可直接用于 PR 描述。

#### 💻 变更类型 | Change Type
- [ ] feat    <!-- 引入新功能 | Introduce new features -->
- [ ] fix    <!-- 修复 Bug | Fix a bug -->
- [ ] refactor    <!-- 重构代码（既不修复 Bug 也不添加新功能） | Refactor code that neither fixes a bug nor adds a feature -->
- [ ] perf    <!-- 提升性能的代码变更 | A code change that improves performance -->
- [ ] style    <!-- 添加或更新不影响代码含义的样式文件 | Add or update style files that do not affect the meaning of the code -->
- [ ] test    <!-- 添加缺失的测试或纠正现有的测试 | Adding missing tests or correcting existing tests -->
- [x] docs    <!-- 仅文档更新 | Documentation only changes -->
- [x] chore    <!-- 其他不修改 src 或 test 文件的变更 | Other changes that don’t modify src or test files -->
- [ ] ci    <!-- 修改持续集成配置文件和脚本 | Changes to our CI configuration files and scripts -->
- [ ] build    <!-- 进行架构变更 | Make architectural changes -->

#### 🔀 变更说明 | Description of Change
本 PR 主要完善 **Anomaly Detection（异常检测）** 学习章节，围绕“定义与价值 → 异常类型 → 常见方法 → 代表算法 → 数据假设”进行结构化补充，帮助读者建立从概念理解到算法选择的完整框架。

本次更新重点包括：
- 明确异常检测在无监督学习中的定位：识别显著偏离常态的数据点，用于欺诈识别、系统故障预警、医疗异常监测等场景。
- 梳理三类异常：
  - Point Anomalies（点异常）：单个样本显著偏离
  - Contextual Anomalies（上下文异常）：在特定时间/环境下异常
  - Collective Anomalies（群体异常）：单点不异常但整体行为异常
- 总结三类主流技术路线：
  - Statistical Methods（统计方法：z-score、modified z-score、boxplot）
  - Clustering-Based Methods（聚类方法：小簇/离群点识别）
  - ML-Based Methods（机器学习方法：One-Class SVM、Isolation Forest、LOF）
- 增强三种代表算法说明：
  - One-Class SVM：学习包围正常样本的边界，边界外判定为异常
  - Isolation Forest：通过随机切分构建隔离树，路径越短越可能异常
  - LOF（Local Outlier Factor）：比较局部密度，密度显著更低者为异常点
- 补充关键公式及含义：
  - Isolation Forest 分数：`score(x) = 2^(-E(h(x))/c(n))`
  - LOF 分数：`LOF(p) = (Σ lrd(o) / k) / lrd(p)`
  - 局部可达密度：`lrd(p) = 1 / (Σ reach_dist(p, o) / k)`
- 补充方法使用前提：分布假设、特征相关性、部分算法对标注数据需求差异。

#### ✅ 价值与收益 | Benefits
- 帮助读者快速理解“何时用哪类异常检测方法”的决策逻辑。
- 将算法直觉与数学定义联结，降低抽象概念学习门槛。
- 为后续实战中的异常评分解释、阈值设定与告警策略打好基础。

#### 🧪 验证说明 | Validation
- 本次为课程文档增强，不涉及运行时代码逻辑变更。
- 已完成术语、公式与章节一致性自检，确保概念定义准确、结构连贯。

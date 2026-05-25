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
本 PR 主要完善 **Unsupervised Learning Algorithms（无监督学习算法）** 章节内容，围绕“定义与目标 → 任务类型 → 核心概念 → 实践注意事项”进行系统化补充，帮助读者建立无标签学习场景下的完整认知框架。

本次更新涵盖以下重点：
- 明确无监督学习与监督学习的区别：无标签数据、无显式目标输出、以发现结构为主。
- 梳理三类典型任务及直观场景：
  - Clustering（聚类）：按相似性分组（如客户分群、文档分组）
  - Dimensionality Reduction（降维）：保留关键信息并降低特征维度
  - Anomaly Detection（异常检测）：识别偏离常态的数据点
- 补充核心概念与术语解释：
  - Unlabeled Data（无标签数据）
  - Similarity Measures（相似度度量：Euclidean / Cosine / Manhattan）
  - Clustering Tendency（聚类倾向）
  - Cluster Validity（聚类有效性：Cohesion / Separation）
  - Dimensionality & Intrinsic Dimensionality（维度与内在维度）
  - Anomaly 与 Outlier 的关系与区别
  - Feature Scaling（特征缩放：Min-Max、Z-score）
- 强调高维数据挑战（维度灾难）及特征缩放在距离计算中的必要性。

#### ✅ 价值与收益 | Benefits
- 让读者在进入具体算法（如 K-Means、PCA、DBSCAN）前先建立任务地图与评价标准。
- 降低术语理解成本，提升章节可读性与前后知识衔接。
- 为后续实践中的“算法选择、特征处理、结果评估”提供统一思考框架。

#### 🧪 验证说明 | Validation
- 本次为课程文档内容增强，不涉及运行时代码修改。
- 已完成文本一致性与术语完整性检查，确保章节逻辑连贯、定义准确。

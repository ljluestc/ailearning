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
本 PR 主要完善 **Principal Component Analysis (PCA)** 学习章节内容，围绕“降维目标 → 数学基础 → 算法流程 → 成分选择 → 数据假设”进行系统化补充，帮助读者建立从概念到实践的完整理解。

本次更新重点包括：
- 明确 PCA 的核心目标：在尽可能保留原始信息（方差）的前提下降低特征维度。
- 增强直观解释：以“寻找数据最重要方向”说明主成分含义，连接可视化、特征提取与降噪应用场景。
- 补充三大基础概念与关系：
  - Variance（方差）：衡量数据离散程度，PCA 优先保留高方差方向
  - Covariance（协方差）：描述特征间联动关系，用于构建协方差矩阵
  - Eigenvectors / Eigenvalues（特征向量 / 特征值）：分别表示方向与该方向解释的方差大小
- 梳理 PCA 标准步骤：
  1) 数据标准化  
  2) 计算协方差矩阵  
  3) 求解特征值与特征向量  
  4) 按特征值降序排序  
  5) 选择前 k 个主成分  
  6) 投影得到低维表示
- 增加特征值方程与矩阵变换表达：
  - `C * v = λ * v`
  - `Y = X * V`
- 补充组件数选择方法：基于 explained variance ratio（解释方差比）选择覆盖率较高的主成分（如 95%）。
- 强调 PCA 关键前提：线性关系、特征相关性、尺度敏感（需标准化）。

#### ✅ 价值与收益 | Benefits
- 帮助读者将 PCA 的“几何直觉”与“线性代数表达”建立映射。
- 降低对特征值/特征向量、协方差矩阵等概念的理解门槛。
- 为后续在高维数据场景中的降维、可视化、建模提效提供理论基础。

#### 🧪 验证说明 | Validation
- 本次为课程文档增强，不涉及运行时代码逻辑修改。
- 已完成内容一致性检查，确保术语定义、步骤顺序与公式表达前后一致。

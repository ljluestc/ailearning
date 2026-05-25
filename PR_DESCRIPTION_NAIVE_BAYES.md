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
本 PR 补充并整理了 **Fundamentals of AI** 中两节核心监督学习内容：

- Section 7：**Naive Bayes（朴素贝叶斯）**
- Section 8：**Support Vector Machines（支持向量机，SVM）**

目标是形成“概率分类方法 + 最大间隔分类方法”的连续学习路径，帮助读者在模型思想上建立横向对比。

主要更新点如下：

1. Naive Bayes 章节增强
- 系统说明 Bayes 定理：
  - `P(A|B) = [P(B|A) * P(A)] / P(B)`
- 引入疾病检测案例，完整推导后验概率并解释“低基率场景下阳性结果的直觉偏差”。
- 明确 Naive Bayes 的条件独立性假设及其实际局限。
- 梳理分类流程：
  1) 计算先验概率
  2) 估计似然
  3) 计算后验概率
  4) 选择后验最大类别
- 对比三种常见变体及适用场景：
  - Gaussian NB（连续特征）
  - Multinomial NB（离散计数特征，常见文本任务）
  - Bernoulli NB（二值特征）

2. SVM 章节增强
- 解释 SVM 的核心目标：寻找最大化间隔（margin）的最优超平面。
- 引入支持向量（support vectors）在决策边界定义中的关键作用。
- 区分线性 SVM 与非线性 SVM，并说明适用场景差异。
- 补充核技巧（Kernel Trick）直觉与常见核函数：
  - Polynomial
  - RBF
  - Sigmoid
- 给出 SVM 优化目标形式，帮助读者建立“几何直觉 + 优化问题”双视角理解。

3. 对比式学习价值补充
- 通过 Naive Bayes 与 SVM 的并行学习，强化对以下差异的理解：
  - 概率建模 vs 间隔最大化
  - 强分布/独立性假设 vs 少分布假设
  - 文本分类常用模型 vs 高维复杂边界建模模型

#### ✅ 价值与收益 | Benefits
- 章节结构更完整，概念过渡更自然，降低入门学习断层。
- 同时覆盖“概率分类”与“间隔分类”两种经典范式，提升模型比较能力。
- 为后续内容（如核方法、集成模型、文本分类实践）奠定统一术语和方法基础。

#### 🧪 验证说明 | Validation
- 本次为学习文档更新，不涉及运行时代码逻辑变更。
- 已完成文案自检，确保术语、公式与概念前后一致。

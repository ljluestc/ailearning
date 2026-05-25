#### 💻 变更类型 | Change Type
- [ ] feat    <!-- 引入新功能 | Introduce new features -->
- [ ] fix    <!-- 修复 Bug | Fix a bug -->
- [ ] refactor    <!-- 重构代码（既不修复 Bug 也不添加新功能） | Refactor code that neither fixes a bug nor adds a feature -->
- [ ] perf    <!-- 提升性能的代码变更 | A code change that improves performance -->
- [ ] style    <!-- 添加或更新不影响代码含义的样式文件 | Add or update style files that do not affect the meaning of the code -->
- [ ] test    <!-- 添加缺失的测试或纠正现有的测试 | Adding missing tests or correcting existing tests -->
- [x] docs    <!-- 仅文档更新 | Documentation only changes -->
- [ ] ci    <!-- 修改持续集成配置文件和脚本 | Changes to our CI configuration files and scripts -->
- [x] chore    <!-- 其他不修改 src 或 test 文件的变更 | Other changes that don’t modify src or test files -->
- [ ] build    <!-- 进行架构变更 | Make architectural changes -->

#### 🔀 变更说明 | Description of Change
本 PR 主要补充并完善 **Naive Bayes（朴素贝叶斯）** 学习章节，围绕“理论基础 → 算法机制 → 变体选择 → 数据假设”形成更完整的学习路径，帮助读者从概率直觉平滑过渡到分类建模实践。

本次文档更新重点包括：
- 系统阐明 Bayes 定理公式及各项概率含义（先验、似然、后验）。
- 增加医疗检测案例，逐步推导 `P(A|B)`，并解释“检测准确但阳性后患病概率仍可能较低”的原因。
- 明确 Naive Bayes 的核心“条件独立性”假设及其现实局限。
- 梳理 Naive Bayes 推断流程：
  1) 计算各类别先验概率  
  2) 估计特征在类别条件下的似然  
  3) 应用 Bayes 定理计算后验概率  
  4) 选择后验概率最大的类别作为预测结果
- 对比三种常见变体及适用场景：
  - Gaussian Naive Bayes（连续特征，近似高斯分布）
  - Multinomial Naive Bayes（离散计数特征，常见于文本词频）
  - Bernoulli Naive Bayes（二值特征，关注是否出现）
- 补充数据前提说明：特征独立性、分布匹配、训练样本规模等。

#### ✅ 价值与收益 | Benefits
- 章节结构更清晰，降低初学者对公式与术语的理解门槛。
- 通过案例计算增强“概率更新”直觉，提升可解释性。
- 为后续文本分类、垃圾邮件识别、情感分析等实战主题提供理论铺垫。

#### 🧪 验证说明 | Validation
- 本次为学习文档更新，不涉及运行时代码逻辑变更。
- 已完成文档内容自检，确保术语与公式表达一致、章节衔接完整。

#### 💻 变更类型 | Change Type
- [ ] feat    <!-- 引入新功能 | Introduce new features -->
- [x] fix    <!-- 修复 Bug | Fix a bug -->
- [ ] refactor    <!-- 重构代码（既不修复 Bug 也不添加新功能） | Refactor code that neither fixes a bug nor adds a feature -->
- [ ] perf    <!-- 提升性能的代码变更 | A code change that improves performance -->
- [ ] style    <!-- 添加或更新不影响代码含义的样式文件 | Add or update style files that do not affect the meaning of the code -->
- [ ] test    <!-- 添加缺失的测试或纠正现有的测试 | Adding missing tests or correcting existing tests -->
- [x] docs    <!-- 仅文档更新 | Documentation only changes -->
- [ ] ci    <!-- 修改持续集成配置文件和脚本 | Changes to our CI configuration files and scripts -->
- [ ] chore    <!-- 其他不修改 src 或 test 文件的变更 | Other changes that don’t modify src or test files -->
- [ ] build    <!-- 进行架构变更 | Make architectural changes -->

#### 🔀 变更说明 | Description of Change
本 PR 聚焦于 `Logistic Regression` 学习内容的完善与梳理，主要用于提升相关章节的可读性、结构完整性与学习连贯性。

本次内容覆盖：
- Logistic Regression 的核心定位（分类而非回归）
- 二分类任务与概率输出的关系
- Sigmoid 函数的作用、数学表达式与直观解释
- 决策边界与高维超平面的概念说明
- 阈值（Threshold）对分类结果的影响
- 逻辑回归常见数据假设（如二分类目标、log-odds 线性关系、低多重共线性、样本量需求）

通过本次更新，章节结构从“定义 → 原理 → 数学形式 → 决策机制 → 适用前提”更加完整，便于读者从概念理解过渡到后续实战。

#### 📝 补充信息 | Additional Information
- 本次变更属于学习文档增强，不引入运行时逻辑变更。
- 重点在于减少概念混淆（例如 logistic regression 命名与实际任务类型的混淆）。
- 适用于 AI 基础学习路径中“分类模型入门”阶段内容衔接。

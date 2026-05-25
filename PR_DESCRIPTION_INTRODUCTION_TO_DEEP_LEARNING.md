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
本 PR 新增并整理 **Fundamentals of AI - Section 16 / 24: Introduction to Deep Learning（深度学习导论）** 学习内容，围绕“为什么需要深度学习 → 神经网络结构 → 训练机制 → 调参要点”构建完整入门路径，帮助读者从传统机器学习自然过渡到深度学习范式。

主要更新内容如下：

1. 深度学习定位与价值
- 明确深度学习是机器学习的重要分支，核心是通过多层神经网络自动学习数据中的高层特征表示。
- 强调其在图像识别、自然语言处理、语音识别等复杂任务中的优势，解释其成为现代 AI 核心技术的原因。

2. 学习动机与核心思想
- 说明传统机器学习在复杂非线性问题上的局限，突出“手工特征工程成本高、表达能力受限”等痛点。
- 引入“受人脑神经结构启发”的建模思想，解释深层网络如何逐层抽取更抽象的特征。

3. 人工神经网络（ANN）基础结构
- 系统梳理神经网络三类核心层级：
  - Input Layer（输入层）：接收原始特征
  - Hidden Layer（隐藏层）：执行特征变换与抽象表示学习
  - Output Layer（输出层）：给出最终预测结果
- 说明“深度”主要体现为隐藏层层数增加，以及由此带来的表示学习能力提升。

4. 激活函数作用与常见类型
- 解释激活函数的关键作用：引入非线性能力，使网络可拟合复杂函数关系。
- 补充常见激活函数及适用直觉：
  - Sigmoid：输出映射到 (0,1)，常见于二分类输出层
  - ReLU：计算简单、缓解梯度消失，隐藏层应用最广
  - Tanh：输出范围 (-1,1)，零中心特性在部分场景更稳定

5. 训练过程关键机制
- Backpropagation（反向传播）：根据预测误差逐层计算梯度并回传。
- Loss Function（损失函数）：衡量预测值与真实值差异，是优化目标的核心度量。
- Optimizer（优化器）：基于梯度更新参数（如 SGD、Adam），驱动模型收敛到更优解。

6. 超参数与调优认知
- 梳理超参数概念与影响范围（学习率、批大小、网络层数、训练轮数等）。
- 强调超参数调优对训练稳定性、收敛速度与最终泛化性能的决定性作用。

#### ✅ 价值与收益 | Benefits
- 建立深度学习入门所需的统一概念体系，降低后续 CNN、RNN、Transformer 学习门槛。
- 将“结构（网络层）+ 机制（反向传播/优化）+ 实践（调参）”串联成可执行学习框架。
- 为后续模型训练实战、损失曲线分析与性能优化提供理论基础。

#### 🧪 验证说明 | Validation
- 本次为学习文档更新，不涉及运行时代码与业务逻辑变更。
- 已完成内容自检，确保术语定义准确、逻辑层次清晰、章节衔接一致。

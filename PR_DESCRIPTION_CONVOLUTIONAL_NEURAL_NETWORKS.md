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
本 PR 新增并整理 **Fundamentals of AI - Section 19 / 24: Convolutional Neural Networks（卷积神经网络）** 学习内容，围绕“CNN 核心结构 → 特征图与层次化表示学习 → 图像识别流程 → 数据假设与训练前提”构建系统化认知框架，帮助读者从通用 MLP 过渡到视觉任务专用网络。

主要更新内容如下：

1. CNN 基础定位与适用场景
- 明确 CNN 是为网格结构数据（尤其图像）设计的专用神经网络。
- 强调其在图像分类、目标检测、图像分割等任务中的优势来源：能够高效捕获空间局部模式与层次特征。

2. 核心网络结构与层间协作
- 系统梳理 CNN 三类核心层：
  - Convolutional Layers（卷积层）：通过可学习卷积核在局部感受野上滑动，提取边缘、纹理、角点等特征并生成 Feature Maps（特征图）。
  - Pooling Layers（池化层）：通过 Max/Avg Pooling 进行下采样，降低计算成本并提升平移鲁棒性。
  - Fully Connected Layers（全连接层）：在网络后端进行高层语义组合，完成分类或回归预测。
- 说明典型堆叠方式：卷积层与池化层交替构建特征层级，末端展平后接全连接层输出结果。

3. 特征图与层次化特征学习机制
- 解释每个卷积核对应一张特征图，不同卷积核学习不同视觉模式（如边缘/角点/纹理）。
- 总结层次化学习路径：
  - 初始层：学习低级特征（边缘、简单纹理）
  - 中间层：组合低级特征形成更复杂结构（角点、局部形状）
  - 深层：抽取高级语义特征（物体部件与类别相关模式）
- 结合手写数字示例，说明网络如何从“边界检测”逐步过渡到“结构语义识别”。

4. 图像识别任务中的端到端流程
- 输入层：接收图像张量（高度、宽度、通道）。
- 多层卷积：由低到高逐步提取视觉特征。
- 池化降维：压缩空间维度并增强泛化鲁棒性。
- 展平与全连接：将高层特征映射为类别概率或回归输出。
- 强调该分层流水线是 CNN 在视觉任务中高性能表现的关键。

5. CNN 的关键数据假设与训练前提
- Grid-Like Structure（网格结构）：输入需具有空间拓扑（如图像/视频）。
- Spatial Hierarchy（空间层次性）：高级语义由低级模式逐层组合而成。
- Feature Locality（局部相关性）：邻近像素关联更强，适合局部卷积建模。
- Feature Stationarity（特征平稳性）：同一特征在不同空间位置语义一致，可通过权重共享统一检测。
- Sufficient Data & Normalization（数据量与归一化）：
  - 需要足够标注数据避免过拟合
  - 输入归一化可提升训练稳定性与收敛效率

#### ✅ 价值与收益 | Benefits
- 建立 CNN 从“结构设计”到“表示学习”再到“训练前提”的完整认知路径。
- 强化对卷积核、特征图、池化与权重共享等核心机制的工程理解。
- 为后续学习 ResNet、目标检测与图像分割等视觉深度学习主题打下基础。

#### 🧪 验证说明 | Validation
- 本次为学习文档更新，不涉及运行时代码、配置或依赖变更。
- 已完成内容自检，确保术语定义准确、层次结构清晰、章节逻辑一致。

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
本 PR 补充并整理了 **Fundamentals of AI - Section 13: Reinforcement Learning Algorithms（强化学习）** 章节内容，目标是建立“学习范式 → 交互机制 → 核心要素 → 任务类型”的完整认知框架，帮助读者从监督/无监督学习顺利过渡到序列决策学习。

主要更新点如下：

1. 强化学习范式定位
- 明确强化学习与监督学习、无监督学习的区别：
  - 强化学习以 **与环境交互** 为核心
  - 通过 **奖励/惩罚反馈** 进行试错学习
  - 目标是最大化长期累计回报
- 使用“训练宠物”类比强化反馈机制，降低概念理解门槛。

2. RL 工作机制补充
- 说明 Agent 与 Environment 的闭环过程：
  - 观察状态（State）
  - 选择动作（Action）
  - 接收奖励（Reward）
  - 转移到新状态并持续迭代
- 引入 Policy（策略）作为决策规则核心，强调学习目标是找到最优策略。

3. Model-Based 与 Model-Free 对比
- Model-Based RL：
  - 学习环境模型并用于规划
  - 更偏“先预测后决策”
- Model-Free RL：
  - 不显式建模环境，直接从经验中学习
  - 更偏“直接试错优化策略”
- 通过“有地图/无地图走迷宫”直觉类比解释二者差异。

4. 核心概念体系化
- 补充并统一 RL 关键术语：
  - Agent、Environment、State、Action、Reward、Policy
  - Value Function（状态价值/动作价值）
  - Discount Factor（γ）
- 强调价值函数用于估计长期收益，指导策略改进。
- 解释折扣因子含义：
  - `γ=0` 强调即时回报
  - `γ→1` 更重视长期回报

5. 任务形态说明
- Episodic Tasks（回合式任务）：有终止状态（如走迷宫到达终点）
- Continuous Tasks（持续任务）：无明确终止（如连续控制问题）
- 明确不同任务形态会影响训练目标与评估方式。

#### ✅ 价值与收益 | Benefits
- 构建强化学习入门所需的统一术语体系，降低后续算法学习成本。
- 通过“概念 + 直觉类比”方式增强可解释性与记忆点。
- 为后续学习 Q-Learning、DQN、Policy Gradient、Actor-Critic 等算法奠定基础。

#### 🧪 验证说明 | Validation
- 本次为学习文档更新，不涉及运行时代码变更。
- 已完成内容自检，确保术语定义、逻辑层次与章节衔接一致。

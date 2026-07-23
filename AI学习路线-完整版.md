---
AIGC:
    Label: "1"
    ContentProducer: 001191110102MACQD9K64018705
    ProduceID: 4228057399312748_0/project_7665691046931726601-files/AI学习路线-完整版.md
    ReservedCode1: ""
    ContentPropagator: 001191110102MACQD9K64028705
    PropagateID: 4228057399312748#1784814716069
    ReservedCode2: ""
---
# 🤖 AI 完整学习路线（由浅入深）

> 分阶段目标 + 学习重点 + 实操建议 + B站/YouTube/海外公开课资源 · 2026版

---

## 📋 学习阶段总纲

| 阶段 | 主题 | 核心目标 | 预计周期 |
|------|------|----------|----------|
| 一 | 数学基础 | 看懂模型权重、梯度推导、向量检索底层逻辑 | 4-6周 |
| 二 | 机器学习基础 | 理解拟合、优化、泛化三大核心问题 | 4-6周 |
| 三 | 神经网络入门 | 从零搭建MLP，手写反向传播 | 3-4周 |
| 四 | 深度学习进阶 | 图像分类CNN、文本时序预测LSTM | 4-6周 |
| 五 | Transformer & 预训练 | 精读论文，微调BERT/GPT | 4-6周 |
| 六 | 大模型工程扩展 | RAG/GraphRAG/Function Calling/Prompt工程/低代码平台 | 4-6周 |
| 七 | Agent智能体开发 | LangGraph有状态工作流、多Agent协作、Coding Agent | 4-6周 |
| 八 | 模型微调与私有化部署 | LoRA微调、量化部署、对齐技术、API服务化 | 4-6周 |
| 九 | 多模态大模型 | 视觉理解、图文生成、视频生成基础 | 4-6周 |

---

## 📐 阶段一：数学基础（AI 底层根基）

### 1.1 线性代数（向量 / 矩阵 / 范数）

**核心知识点：**
- **向量**：向量运算、内积、余弦相似度、线性无关、特征向量
- **矩阵**：矩阵乘法、转置、逆矩阵、秩、特征值、奇异值分解 SVD
- **范数**：L1、L2、无穷范数，矩阵 F 范数（损失、正则化高频用到）

**学习目标：** 看懂模型权重、梯度推导、向量检索底层逻辑

### 1.2 微积分（梯度）

**核心知识点：**
- 多元偏导、链式法则、梯度、极值、泰勒展开

**学习目标：** 看懂反向传播、梯度下降优化原理

### 1.3 概率论（基础分布）

**核心知识点：**
- 期望 / 方差、最大似然估计、正态分布、伯努利、二项分布、条件概率、贝叶斯公式

**学习目标：** 理解损失函数、分类概率、模型不确定性

### 📌 实操
- 用 NumPy 手写矩阵运算、梯度计算、概率采样

### 🎬 学习资源

#### B站资源

| 资源 | UP主 | 搜索关键词 | 覆盖内容 |
|------|------|-----------|----------|
| 可视化理解（优先） | 3Blue1Brown | `线性代数的本质 合集`、`微积分的本质 合集` | 向量、矩阵运算、特征值、范数几何含义、梯度可视化 |
| 系统推导课 | 宋浩老师官方 | `宋浩 线性代数完整版`、`宋浩 高等数学`、`宋浩 概率论与数理统计` | L1/L2范数、多元偏导、链式法则、正态/伯努利分布、贝叶斯公式 |
| 精简课 | 苏德矿（矿爷） | `苏德矿 机器学习专用数学精简课` | 机器学习数学精简版 |

#### YouTube / 海外公开课

| 资源 | 平台 | 链接/搜索关键词 | 覆盖内容 |
|------|------|----------------|----------|
| MIT 18.06 Linear Algebra | YouTube / MIT OCW | `MIT 18.06 Gilbert Strang Linear Algebra` | 经典线代课程，向量空间、矩阵分解、特征值 |
| 3Blue1Brown Essence of Linear Algebra | YouTube | `3Blue1Brown Essence of Linear Algebra` | 几何直觉可视化，与B站合集同源英文版 |
| 3Blue1Brown Essence of Calculus | YouTube | `3Blue1Brown Essence of Calculus` | 微积分几何直觉 |
| Khan Academy Mathematics | YouTube | `Khan Academy Linear Algebra / Calculus / Statistics` | 数学基础全覆盖，适合查漏补缺 |
| Harvard Stat 110 Probability | YouTube / edX | `Harvard Stat 110 Probability` | 概率论系统课，贝叶斯、分布、期望 |
| Stanford CS229 (数学部分) | YouTube / Stanford Online | `Stanford CS229 Andrew Ng Machine Learning` | ML所需数学基础，梯度推导 |

**阶段验收：** 能独立看懂损失函数求导、SVM 间隔推导、向量相似度计算逻辑

---

## 🤖 阶段二：机器学习基础（传统 ML）

### 2.1 核心模型
- 线性回归、逻辑回归、SVM、决策树 / 随机森林 / XGBoost

### 2.2 核心通用概念（重中之重）

**损失函数：**
- MSE、交叉熵、Hinge 损失

**优化算法：**
- 梯度下降 SGD、批量梯度下降、正则化 L1/L2

**基础工程：**
- 训练集 / 验证集 / 测试集划分
- 评估指标：准确率、MSE、召回率

### 📌 实操
- sklearn 实现分类 / 回归任务
- 手动推导逻辑回归梯度

### 🎬 学习资源

#### B站资源

| 资源 | UP主 | 搜索关键词 | 特点 |
|------|------|-----------|------|
| 理论+代码（推荐A） | 李沐 | `动手学深度学习 B站完整247集` | 线性回归、逻辑回归、SGD、正则化、决策树、SVM，配套 PyTorch |
| 公式通俗（推荐B） | 李宏毅 | `李宏毅 机器学习2025` | 公式通俗，重点拆解梯度下降、损失函数、模型泛化 |

#### YouTube / 海外公开课

| 资源 | 平台 | 链接/搜索关键词 | 覆盖内容 |
|------|------|----------------|----------|
| Andrew Ng ML Specialization | Coursera | `Coursera Machine Learning Specialization Andrew Ng` | ML最经典入门课，2022年更新版，Python实现 |
| Stanford CS229 | YouTube | `Stanford CS229 Machine Learning` | 理论深度极高，数学推导完整 |
| fast.ai Practical Deep Learning | YouTube / fast.ai | `fast.ai Practical Deep Learning for Coders` | 自顶向下实操派，边做边学 |
| Georgia Tech ML on Udacity | Udacity | `Udacity Georgia Tech Machine Learning` | 系统ML课程，理论+编程作业 |

**阶段验收：** 明白拟合、优化、泛化三大核心问题，独立完成1个分类/回归项目

---

## 🧠 阶段三：神经网络入门（深度学习地基）

### 3.1 核心知识点
- **MLP 多层感知机**：全连接层结构
- **反向传播**：链式法则推导权重更新全过程
- **激活函数**：Sigmoid、Tanh、ReLU、LeakyReLU、GELU
- **过拟合解决方案**：Dropout、早停 Early Stop、权重衰减、数据增强

### 📌 实操
- PyTorch/TensorFlow 从零搭建 MLP
- 手写简易反向传播

### 🎬 学习资源

#### B站资源

| 资源 | UP主 | 搜索关键词 | 覆盖内容 |
|------|------|-----------|----------|
| 理论推导 | 李宏毅 | `李宏毅 深度学习 MLP反向传播` | 完整链式求导推导、激活函数对比 |
| 实战代码 | 借我两毛五 | `深度学习全套实战 PyTorch` | 从零搭建MLP、Dropout、早停、权重衰减、数据增强 |

#### YouTube / 海外公开课

| 资源 | 平台 | 链接/搜索关键词 | 覆盖内容 |
|------|------|----------------|----------|
| Andrew Ng Deep Learning Specialization | Coursera | `Coursera Deep Learning Specialization Andrew Ng` | 5门课覆盖NN、CNN、RNN、超参数调优 |
| Geoffrey Hinton Neural Networks | Coursera | `Coursera Neural Networks Hinton` | NN之父亲授，理论深度极高 |
| Hugo Larochelle Deep Learning | YouTube | `Hugo Larochelle Neural Networks` | 完整深度学习课程，反向传播讲解极佳 |
| 3Blue1Brown Neural Networks | YouTube | `3Blue1Brown Neural Networks series` | 可视化理解NN、反向传播几何直觉 |

**阶段验收：** 独立完成MLP搭建项目，手写反向传播

---

## 🚀 阶段四：深度学习进阶（经典网络架构）

### 4.1 CNN 卷积神经网络
- 卷积、池化、Padding、经典结构 ResNet
- 图像任务核心

### 4.2 RNN/LSTM/GRU
- 时序建模、循环梯度消失问题
- 传统文本处理方案

### 4.3 注意力机制
- 自注意力、多头注意力前置知识
- Transformer 核心铺垫

### 📌 实操
- 图像分类 CNN
- 文本时序预测 LSTM

### 🎬 学习资源

#### B站资源

| 资源 | UP主 | 搜索关键词 | 覆盖内容 |
|------|------|-----------|----------|
| CNN | 李沐 | `动手学深度学习 CNN ResNet` | 卷积网络完整实战 |
| LSTM | 李沐 | `动手学深度学习 LSTM GRU` | 循环网络实战 |
| NLP实战 | 黑马程序员 | `PyTorch LSTM文本分类实战` | RNN梯度消失、自注意力铺垫 |
| 补充 | - | `PyTorch手写CNN图像分类` | 手写CNN实操 |

#### YouTube / 海外公开课

| 资源 | 平台 | 链接/搜索关键词 | 覆盖内容 |
|------|------|----------------|----------|
| Stanford CS231n CNN | YouTube | `Stanford CS231n Convolutional Neural Networks` | Fei-Fei Li / Karpathy，CNN最经典课程 |
| Stanford CS224n NLP | YouTube | `Stanford CS224n NLP with Deep Learning` | NLP深度学习，LSTM/Attention/RNN |
| Oxford Deep Learning | YouTube | `Oxford Deep Learning Nando de Freitas` | CNN/RNN/Attention系统讲解 |
| Andrej Karpathy "Zero to Hero" | YouTube | `Andrej Karpathy Neural Networks Zero to Hero` | 从零构建NN，micrograd项目 |

**阶段验收：** 独立完成图像分类或文本分类项目

---

## 📖 阶段五：Transformer & 预训练大模型

### 5.1 理论
- 精读论文《Attention Is All You Need》
- 吃透编码器 Encoder、解码器 Decoder、位置编码、多头自注意力

### 5.2 工具栈
- Hugging Face 生态：Transformers、Datasets、Evaluate、Accelerate

### 📌 实操
- 加载预训练 BERT/GPT
- 微调小模型、文本生成、分类任务

### 🎬 学习资源

#### B站资源

| 资源 | UP主 | 搜索关键词 | 覆盖内容 |
|------|------|-----------|----------|
| 理论吃透 | 李宏毅 | `李宏毅 Transformer 完整讲解` | 逐段拆解论文、位置编码、多头自注意力、Encoder-Decoder |
| 通俗讲解 | 五道口纳什 | `Transformer底层原理大白话讲解` | 通俗理解Transformer |
| HF实操 | - | `Hugging Face完整实战教程 PyTorch` | Transformers库、BERT/GPT加载、微调、文本生成、Embedding |

#### YouTube / 海外公开课

| 资源 | 平台 | 链接/搜索关键词 | 覆盖内容 |
|------|------|----------------|----------|
| Stanford CS25 Transformers United | YouTube | `Stanford CS25 Transformers United` | Transformer全方位深度解读 |
| Andrej Karpathy "Let's build GPT" | YouTube | `Andrej Karpathy Let's build GPT from scratch` | 从零手搓GPT，代码级理解 |
| HuggingFace NLP Course | huggingface.co/learn | `HuggingFace NLP Course` | 官方免费课程，Transformer实操 |
| DeepLearning.AI "Generative AI with LLMs" | Coursera | `Coursera Generative AI with LLMs` | LLM原理、微调、部署全链路 |

**阶段验收：** 独立完成BERT/GPT微调项目

---

## 🔧 阶段六：大模型工程扩展（扩展版）

### 6.1 MoE 混合专家模型
- 稀疏激活、大模型高效扩容原理

### 6.2 RAG 检索增强生成
- 文档切片、向量化、检索 + LLM 生成完整链路

### 6.3 向量数据库
- FAISS、Chroma、Milvus

### 6.4 Prompt Engineering
- 提示词设计、Few-shot、CoT 思维链、格式约束

### 6.5 Function Calling / Tool Use（🆕）
- **概念**：大模型工具调用的标准协议，让 LLM 具备调用外部工具/API 的能力
- **核心机制**：模型输出结构化 JSON 函数调用指令 → 外部执行 → 结果回传模型
- **主流支持**：OpenAI Function Calling、通义千问 Function Call、Claude Tool Use
- **结构化输出**：JSON Mode、Response Format 约束、instructor 库、Pydantic 模型映射
- **最佳实践**：工具描述撰写规范、参数校验、错误处理与重试机制

### 6.6 结构化输出（🆕）
- **JSON Mode**：强制模型输出合法 JSON，保证下游解析可靠性
- **instructor 库**：基于 Pydantic 的强类型结构化输出框架，自动校验+重试
- **Outlines / Guidance**：基于正则/JSON Schema约束生成，确保输出格式100%合规
- **应用场景**：信息抽取、数据标注、表单填写、API参数生成

### 6.7 GraphRAG（🆕）
- **概念**：图谱增强的 RAG，将文档构建为知识图谱（实体+关系+社区摘要）
- **优势**：解决传统 RAG 无法处理全局性问题的局限
- **核心流程**：文本切片 → 实体/关系抽取 → 图谱构建 → 社区检测 → 社区摘要 → 检索增强
- **工具**：微软 GraphRAG、Neo4j 图数据库、LlamaIndex 图谱索引

### 6.8 模型评估方法论（🆕）
- **自动化指标**：Perplexity（语言模型困惑度）、BLEU（翻译质量）、ROUGE（摘要质量）
- **人工评估**：偏好评估（Elo排名）、安全性评估、事实性核查
- **LLM-as-Judge**：用 GPT-4 等大模型自动评分，替代部分人工评估
- **评估框架**：Ragas（RAG专项评估）、DeepEval、OpenAI Evals

### 6.9 低代码 AI 平台（🆕）
- **Dify**：开源 LLM 应用开发平台，可视化 Workflow 编排 + RAG 内置
- **Coze（扣子）**：字节跳动 AI Bot 搭建平台，插件生态丰富
- **FastGPT**：开源知识库问答系统，文档上传即用

### 📌 实操
- 用 LangChain + Milvus 搭建完整 RAG 系统
- 使用 Function Calling 构建一个能查天气+搜索的工具调用应用
- 用 Dify 或 Coze 搭建一个知识库问答 Bot
- 对比 GraphRAG 与传统 RAG 在全局性问题上的效果差异

### 🎬 学习资源

#### B站资源

| 资源 | 搜索关键词 | 覆盖内容 |
|------|-----------|----------|
| RAG完整项目 | `LangChain RAG完整项目 Milvus向量库` | 文档切片、文本向量化、RAG全链路 |
| MoE理论 | `五道口纳什 MoE混合专家模型详解` | 混合专家模型原理 |
| Prompt工程 | `李宏毅 大模型Prompt Engineering` | Few-shot、CoT思维链、输出格式约束 |
| GraphRAG | `GraphRAG 知识图谱增强检索 实战` | 图谱构建、社区检测、全局问答 |
| Function Calling | `OpenAI Function Calling 工具调用实战教程` | 工具Schema定义、结构化输出 |
| Dify平台 | `Dify 开源AI应用平台完整部署教程` | 可视化Workflow、RAG编排 |
| Coze平台 | `Coze扣子 AI Bot搭建 从零到一` | Bot创建、插件配置、知识库 |
| 模型评估 | `LLM大模型评估方法 Perplexity BLEU ROUGE` | 自动指标、LLM-as-Judge |

#### YouTube / 海外公开课

| 资源 | 平台 | 链接/搜索关键词 | 覆盖内容 |
|------|------|----------------|----------|
| DeepLearning.AI "Building and Evaluating Advanced RAG" | Coursera | `Coursera Building Evaluating Advanced RAG` | 高级RAG技术、评估方法论 |
| DeepLearning.AI "Functions, Tools and Agents with LangChain" | Coursera | `Coursera Functions Tools Agents LangChain` | Function Calling、工具调用 |
| DeepLearning.AI "LangChain for LLM App Dev" | Coursera | `Coursera LangChain for LLM Application Development` | LangChain核心、RAG、Agent |
| Full Stack LLM Bootcamp | YouTube | `Full Stack LLM Bootcamp 2024` | RAG/微调/评估/部署全链路 |

**阶段验收：** 独立完成 RAG 全链路项目 + 搭建一个低代码平台应用

---

## 🤖 阶段七：Agent 智能体开发（扩展版）

### 7.1 框架学习
- **LangChain**：核心组件 Chain、Memory、Tool、Loader
- **LlamaIndex**：数据索引、查询引擎、Agent 集成

### 7.2 核心范式
- **ReAct Agent**：推理 + 工具调用循环（Thought → Action → Observation）

### 7.3 LangGraph 有状态 Agent 工作流（🆕 核心升级）
- **核心能力**：状态管理、循环与条件分支、Human-in-the-loop、持久化、子图
- **vs LangChain**：LangChain 适合简单链式调用，LangGraph 适合复杂有状态 Agent
- **核心概念**：State（状态定义）、Node（节点逻辑）、Edge（条件路由）、Checkpoint（断点恢复）
- **典型模式**：Plan-and-Execute、Supervisor、Hierarchical Multi-Agent

### 7.4 多 Agent 系统（🆕）
- **CrewAI**：角色扮演式多 Agent 协作，支持任务编排与委派
- **MetaGPT**：多角色软件工程流水线（产品经理→架构师→工程师）
- **AutoGen**：微软多 Agent 对话框架，GroupChat 多轮协作

### 7.5 Coding Agent（🆕）
- **Cursor**：AI 代码编辑器，Agent 模式自动读写文件+执行命令
- **Claude Code**：Anthropic 终端编程助手，直接操作代码仓库
- **核心思路**：让 LLM 具备文件系统读写、Shell 执行、代码搜索能力
- **构建要点**：工具设计（read_file / write_file / bash）、上下文管理、沙箱安全

### 📌 实操
- 用 LangGraph 构建一个带条件分支的研究助手（搜索→分析→写作）
- 用 CrewAI 搭建多 Agent 协作系统（研究员+写手+审核员）
- 用 Claude Code / Cursor 进行日常开发，理解 Coding Agent 工作流程

### 🎬 学习资源

#### B站资源

| 资源 | 搜索关键词 | 覆盖内容 |
|------|-----------|----------|
| LangChain系统课 | `LangChain v1全栈6小时实战教程` | Chain、记忆、工具、智能体架构 |
| ReAct实战 | `从零构建ReAct智能体 LangChain Ollama` | 推理循环、工具调用Demo |
| LlamaIndex | `LlamaIndex入门完整教程` | 数据索引、查询Agent |
| LangGraph | `LangGraph 有状态Agent工作流 实战` | 状态图、条件分支、Human-in-the-loop |
| LangGraph进阶 | `LangGraph 构建复杂AI Agent 项目实战` | 子图、持久化、Plan-and-Execute |
| CrewAI | `CrewAI 多Agent协作 入门教程` | 角色定义、任务编排、协作模式 |
| MetaGPT | `MetaGPT 多智能体协作 完整教程` | 多角色软件工程 |
| AutoGen | `AutoGen 微软多Agent对话框架 教程` | GroupChat |
| Coding Agent | `Cursor AI编辑器 Agent模式 实战教程` | 自动读写文件、代码生成 |

#### YouTube / 海外公开课

| 资源 | 平台 | 链接/搜索关键词 | 覆盖内容 |
|------|------|----------------|----------|
| DeepLearning.AI "Multi AI Agent Systems with crewAI" | Coursera | `Coursera Multi AI Agent Systems crewAI` | crewAI多Agent协作官方课 |
| DeepLearning.AI "AI Agents in LangGraph" | Coursera | `Coursera AI Agents in LangGraph` | LangGraph Agent开发官方课 |
| LangGraph 官方教程 | 官网 | `langchain-ai.github.io/langgraph` | 官方教程、示例、API文档 |
| Andrej Karpathy "Building a Coding Agent" | YouTube | `Andrej Karpathy Building a Coding Agent` | 从零构建Coding Agent原理 |

**阶段验收：** 基于 LangGraph 搭建有状态多步骤 Agent + 多 Agent 协作系统

---

## ⚡ 阶段八：模型微调与私有化部署（🆕 新增）

### 8.1 参数高效微调（PEFT）
- **LoRA / QLoRA**：低秩分解原理，显存降低 60%+，秩 r 的选择策略
- **Adapter Tuning / Prefix Tuning / Prompt Tuning**：不同 PEFT 方法对比
- **工具链**：Unsloth（2x 加速 + 显存优化）、LLaMA-Factory（一站式训练 WebUI）、HuggingFace PEFT 库
- **数据准备**：Alpaca 格式、ShareGPT 格式、数据清洗与质量过滤

### 8.2 量化技术
- **训练后量化（PTQ）**：GPTQ（GPU 优化）、AWQ（激活感知）、GGUF（llama.cpp 生态）
- **量化精度**：INT4 / INT8 / FP16 / BF16 对比，精度-速度-显存权衡
- **bitsandbytes**：动态量化，QLoRA 训练基础
- **选型建议**：推理部署选 AWQ/GPTQ，本地 CPU 推理选 GGUF

### 8.3 部署框架
- **vLLM**：生产首选，PagedAttention 高吞吐推理引擎
- **Ollama**：本地开发利器，一行命令运行开源模型
- **TGI（Text Generation Inference）**：HuggingFace 官方推理服务
- **Docker 容器化**：模型镜像打包、GPU 透传、Compose 编排

### 8.4 对齐技术
- **RLHF**：SFT → 奖励模型训练 → PPO 强化学习
- **DPO**：直接偏好优化，跳过奖励模型，更简单稳定
- **工具**：TRL 库（HuggingFace）、OpenRLHF

### 8.5 API 服务化
- **FastAPI**：构建推理 API，支持流式输出（SSE）、异步推理
- **OpenAI 兼容接口**：标准化 API 格式，方便上游应用对接
- **生产加固**：限流、鉴权、日志监控、健康检查

### 8.6 分布式训练基础
- **DeepSpeed**：ZeRO 优化器状态分片，多卡训练显存管理
- **FSDP**：PyTorch 原生分布式训练方案
- **基础概念**：数据并行、模型并行、流水线并行

### 📌 实操
- 用 Unsloth + LoRA 微调一个 7B 模型完成特定任务
- 用 QLoRA 在单卡消费级 GPU（如 RTX 4090）上完成微调
- 用 Ollama 本地部署量化模型 + FastAPI 封装 API
- 用 vLLM 部署模型并对比推理吞吐量

### 🎬 学习资源

#### B站资源

| 资源 | 搜索关键词 | 覆盖内容 |
|------|-----------|----------|
| LoRA微调 | `大模型LoRA微调实战 HuggingFace PEFT` | 低秩微调原理、PEFT库实操 |
| Unsloth | `Unsloth 大模型微调加速 教程` | 2x加速、显存优化 |
| LLaMA-Factory | `LLaMA-Factory 一站式微调 从零到部署` | WebUI训练、多模型支持 |
| 模型量化 | `大模型量化 AWQ GPTQ GGUF 详解` | 量化原理、精度对比、选型 |
| vLLM部署 | `vLLM部署大模型 教程` | PagedAttention、生产部署 |
| Ollama | `Ollama本地部署大模型 入门` | 一键运行、模型管理 |
| DPO/RLHF | `李宏毅 大模型微调 RLHF DPO` | 对齐原理、偏好优化 |
| FastAPI | `FastAPI 部署大模型推理 API服务` | 流式输出、Docker部署 |
| Docker | `Docker Compose 部署AI模型 完整教程` | 容器化、GPU透传 |
| DeepSpeed | `DeepSpeed 分布式训练 入门教程` | ZeRO分片、多卡训练 |

#### YouTube / 海外公开课

| 资源 | 平台 | 链接/搜索关键词 | 覆盖内容 |
|------|------|----------------|----------|
| DeepLearning.AI "Finetuning Large Language Models" | Coursera | `Coursera Finetuning Large Language Models` | 微调方法论、PEFT、评估 |
| HuggingFace PEFT 课程 | huggingface.co/learn | `huggingface.co/learn` | LoRA/QLoRA/Adapter实操文档 |
| Full Stack Deep Learning | YouTube | `Full Stack Deep Learning course` | 端到端ML工程 |
| MLOps Zoomcamp | YouTube / DataTalksClub | `MLOps Zoomcamp DataTalksClub` | 模型部署、Docker、CI/CD |
| Andrej Karpathy "Let's reproduce GPT-2" | YouTube | `Andrej Karpathy Let's reproduce GPT-2` | 从零复现GPT-2训练全过程 |

**阶段验收：** 完成 LoRA 微调专属模型 + 量化 + 本地部署 + API 服务化全链路项目

---

## 🎨 阶段九：多模态大模型（🆕 新增）

### 9.1 视觉基础与编码器
- **CLIP**：对比学习、图文匹配、零样本分类
- **ViT（Vision Transformer）**：图像 Patch 化、视觉 Transformer 架构
- **进阶编码器**：SigLIP（改进损失函数）、InternViT（多分辨率）

### 9.2 多模态大模型
- **LLaVA**：LLM + 视觉编码器，图文对话经典架构
- **Qwen-VL**：通义千问视觉模型，支持 OCR/图表/公式理解
- **InternVL**：书生万象，高性能开源多模态模型
- **核心能力**：图像理解、OCR、图表分析、VQA（视觉问答）、多图对比

### 9.3 图像理解与生成
- **Stable Diffusion**：扩散模型原理、去噪过程、采样器
- **ControlNet**：精准控制生成（边缘/深度/姿态/线稿）
- **IP-Adapter**：图像风格迁移、角色一致性
- **LoRA 风格微调**：训练专属画风
- **FLUX**：新一代高质量图像生成模型

### 9.4 视频生成基础
- **DiT 架构**：Diffusion Transformer，视频生成的核心范式
- **CogVideoX**：开源文生视频模型
- **Open-Sora / Wan2.1**：开源视频生成方案
- **关键概念**：时序建模、运动一致性、长视频生成挑战

### 9.5 语音多模态（🆕）
- **Whisper**：OpenAI 语音识别模型，多语言转写
- **TTS（文本转语音）**：ChatTTS、Fish Speech、CosyVoice
- **语音对话**：语音输入 → ASR → LLM → TTS 全链路
- **实时语音**：流式 ASR + 流式 TTS 的端到端方案

### 📌 实操
- 用 LLaVA / Qwen-VL 搭建一个图像理解应用
- 用 Stable Diffusion + ControlNet 搭建精准图像生成工作流
- 用 Whisper 搭建语音转文字 + LLM 总结的语音助手
- 本地部署一个视频生成模型体验 DiT 架构

### 🎬 学习资源

#### B站资源

| 资源 | 搜索关键词 | 覆盖内容 |
|------|-----------|----------|
| 多模态总览 | `多模态大模型 李沐 2025` | CLIP/LLaVA/多模态架构讲解 |
| CLIP原理 | `CLIP 视觉语言模型 原理讲解` | 对比学习、零样本分类 |
| Stable Diffusion | `Stable Diffusion WebUI全套教程` | 扩散模型、采样器、参数调节 |
| ControlNet | `ControlNet 精准控制 教程` | 边缘/深度/姿态控制生成 |
| ComfyUI | `ComfyUI Stable Diffusion 工作流教程` | 可视化生图工作流 |
| LLaVA | `LLaVA 多模态大模型 原理与部署` | 图文对话架构 |
| Qwen-VL | `Qwen-VL 通义千问视觉模型 实战教程` | 图文理解、OCR |
| 视频生成 | `AI视频生成 CogVideoX Sora架构 原理` | DiT架构、文生视频 |
| Whisper | `Whisper 语音识别 部署教程` | 多语言ASR |
| TTS | `ChatTTS CosyVoice 语音合成 教程` | 文本转语音 |

#### YouTube / 海外公开课

| 资源 | 平台 | 链接/搜索关键词 | 覆盖内容 |
|------|------|----------------|----------|
| DeepLearning.AI "Generative AI with Multimodal Models" | Coursera | `Coursera Generative AI Multimodal Models` | 多模态AI应用 |
| Stanford CS231n (多模态部分) | YouTube | `Stanford CS231n multimodal` | CLIP/多模态视觉模型 |
| Yannic Kilcher 论文解读 | YouTube | `Yannic Kilcher` | CLIP/LLaVA/DALL-E/Stable Diffusion论文深度解读 |
| HuggingFace Diffusion Models Course | YouTube | `HuggingFace Diffusion Models Course` | 扩散模型从原理到实践 |

**阶段验收：** 独立完成多模态理解应用或图像/视频生成项目

---

## 📐 配套学习规划建议

| 序号 | 建议 | 说明 |
|------|------|------|
| 1 | 严格按顺序学习 | 数学不跳过，否则深度学习公式完全看不懂 |
| 2 | 理论+实操并行 | 每阶段遵循「理论推导 + 代码实操」，只看书不动手极易遗忘 |
| 3 | 统一工具栈 | Python + NumPy/Pandas + PyTorch + HuggingFace + LangChain/LangGraph 生态 |
| 4 | 阶段验收 | 每阶段独立完成1个完整可运行项目 |
| 5 | 收藏管理 | B站/YouTube创建合集，按阶段分类收藏课程 |
| 6 | 海外资源辅助 | 英文基础好的推荐结合Coursera/Stanford课程，理解更深刻 |
| 7 | 阶段八/九可选 | 如专注应用层开发，阶段八/九可延后；如想深入模型层，务必完成 |

---

## 🛠️ 统一技术栈

```
Python → NumPy/Pandas → PyTorch → HuggingFace生态
                                    ├── Transformers / Datasets / Evaluate / Accelerate
                                    ├── PEFT (LoRA/QLoRA) ← Unsloth 加速
                                    └── TRL (DPO/RLHF)
                                    
LangChain → LangGraph → Agent工作流
              ↓
         多Agent系统: CrewAI / MetaGPT / AutoGen
              ↓
         Coding Agent: Cursor / Claude Code

微调部署: Unsloth / LLaMA-Factory → vLLM / Ollama / TGI / Docker
量化方案: AWQ / GPTQ / GGUF / bitsandbytes
分布式: DeepSpeed / FSDP

多模态: CLIP / SigLIP → LLaVA / Qwen-VL / InternVL
        Stable Diffusion / ControlNet / IP-Adapter / FLUX
        视频: CogVideoX / Open-Sora / Wan2.1
        语音: Whisper / ChatTTS / CosyVoice

低代码平台: Dify / Coze / FastGPT

向量数据库: FAISS / Chroma / Milvus
图数据库: Neo4j (GraphRAG)

评估工具: Ragas / DeepEval / LLM-as-Judge
```

---

## 🏆 各阶段验收项目清单

| 阶段 | 验收项目 |
|------|----------|
| 一 | 手写矩阵运算 + 梯度计算 + 概率采样 |
| 二 | sklearn 分类/回归完整项目 |
| 三 | PyTorch 搭建 MLP + 手写反向传播 |
| 四 | CNN 图像分类 或 LSTM 文本分类项目 |
| 五 | BERT/GPT 微调项目（文本分类或生成） |
| 六 | RAG 全链路项目 + 低代码平台应用搭建 |
| 七 | LangGraph 有状态 Agent + 多 Agent 协作系统 |
| 八 | **LoRA 微调专属模型 + 量化 + 本地部署 + API 服务化** |
| 九 | **多模态应用（图像理解/图像生成/语音助手任选其一）** |

---

> 📅 预计总学习周期：36-54周（9-13个月）
> 🎯 最终目标：具备从数学原理到工程落地、从模型微调到多模态应用的全栈AI能力

---

> 本内容由 Coze AI 生成，请遵循相关法律法规及《人工智能生成合成内容标识办法》使用与传播。

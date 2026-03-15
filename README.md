# CPHOS 技术组新同学学习指南

## 这份指南是给谁的

这份指南面向刚进入大学、编程基础较少，但希望尽快参与 CPHOS 技术组实际工作的同学。

目标不是让大家一上来就学很多“高深算法”，而是尽快达到下面这个状态：

- 能在自己的电脑上安装并运行 Python。
- 能看懂简单脚本，敢改一点小功能。
- 能在 AI 工具帮助下写出基础自动化程序。
- 能理解 Agent、MCP、RAG 这些词到底在说什么。
- 能围绕 CPHOS 现有项目做一些真实的小任务，例如整理题库、导入数据、处理 Excel、写自动阅卷原型、维护脚本等。

## 一、先说结论：你们最需要学什么

结合技术组内部各类项目的普遍要求，新同学最需要掌握的不是“竞赛式算法编程”，而是下面 8 类能力：

1. Python 基础语法与脚本编写。
2. 文件读写、路径处理、命令行运行。
3. Excel 自动化处理。
4. 数据库基础与简单 SQL。
5. API 的基本概念与简单后端阅读能力。
6. Git、README、文档、目录结构这些工程化习惯。
7. 会用 Claude Code 或 VS Code 中的 AI 插件辅助开发。
8. 理解生成式 AI、RAG、MCP、Agent 的基本逻辑，知道它们分别适合解决什么问题。

换句话说，第一阶段的要求不是“会造模型”，而是“会借助 AI 和 Python 做事情”。

## 二、在 CPHOS 技术组，你们将来会遇到哪些工作

虽然大家现在还没接触到核心代码库，但在技术组的日常中，我们主要会处理以下几类真实任务：

### 1. 结构化的 Python 开发项目

未来你们会接触到一些结构比较规范的 Python 服务端或工具项目。从这类项目中，大家需要慢慢掌握：

- 看懂 Python 包结构，知道模块、函数、导入是怎么回事。
- 运行脚本，例如 `python scripts/init_db.py`。
- 了解 SQLite、数据表、字段以及数据导入导出的基本流程。
- 看懂命令行参数解析（例如使用 `argparse`）。
- 处理本地路径、文件遍历以及常见的表格文件。
- 理解一个简单的 API 是如何从数据库读取数据并返回给前端的。

### 2. 日常脚本与数据处理工具箱

技术组有大量的日常事务需要通过脚本来提效。典型的场景包括：

- 读取和写入 Excel 表格。
- 批量处理各类名单、指导老师信息、学校信息等。
- 查询数据库、修改并清洗数据。
- 写小工具解决特定活动中的临时需求。

在这个过程中，大家会发现安全和稳妥非常重要。比如，我们会尽量使用参数化查询来操作数据库，避免数据出错或丢失。

### 3. 系统维护与业务支持

技术组不仅写代码，还要服务真实的业务流程，比如：

- 阅卷系统的搭建与维护。
- 题库的整理与格式化。
- 各类业务数据的导入与归档。
- 编写并维护操作说明，为非技术成员提供工具使用支持。

所以大家可以慢慢建立一种意识：技术工作不只是写程序，更是把一个实际的流程变得更稳定、更快、更少出错。

## 三、建议学习路线图

推荐按照下面顺序学，不要一开始就跳到很复杂的 Agent 框架。

### 阶段 0：先搭环境

目标：把电脑准备好，能跑最简单的 Python 程序，能开始用 AI 工具。

需要完成：

- 安装 Python 3。
- 安装 VS Code。
- 学会打开终端。
- 学会运行 `python --version`、`pip --version`。
- 学会创建文件夹、打开项目目录。
- 了解什么是扩展、插件、命令行工具。

建议掌握程度：

- 能在终端里进入某个目录。
- 能运行一个 `.py` 文件。
- 能安装一个常见库。

### 阶段 1：Python 快速入门

目标：能自己写基础脚本。

必须掌握：

- 变量、字符串、数字、布尔值。
- 列表、字典。
- `if`、`for`、`while`。
- 函数。
- `import`。
- 文件读写。
- 异常处理 `try/except`。
- 路径处理 `pathlib`。

建议尽快练的最小项目：

- 读取一个 txt 或 markdown 文件并统计字数。
- 批量重命名某个文件夹下的文件。
- 读取一个 Excel 或 csv，并做简单筛选。
- 根据一份题目描述，生成一个固定格式的输出文件。

### 阶段 2：面向技术组工作的 Python

目标：能看懂并改动仓库中的实际脚本。

必须掌握：

- `openpyxl` 或 `pandas` 的基本用法。
- `argparse` 命令行参数。
- JSON、CSV、Excel 三种数据格式的差别。
- SQLite 基础。
- SQL 基础：`SELECT`、`INSERT`、`UPDATE`、`WHERE`。
- API 基础：什么是请求、响应、JSON、接口路径。

建议能看懂：

- 常见的 Python 开源短脚本或者工具的 README。
- AI 生成的几十行规模但包含函数的完整代码。
- 基础的数据库增删改查 SQL 语句及其在 Python 中的执行。
- 简单的 FastAPI 或 Flask 后端接口返回语句。

### 阶段 3：生成式 AI 基础

目标：先把概念搞清楚，不被名词吓住。

必须搞懂：

- 什么是大语言模型。
- 什么是 token、上下文窗口、系统提示词、用户提示词。
- 为什么模型会“看起来懂了但其实会胡说”。
- 为什么提示词越清晰，输出越稳定。
- 为什么要做评估，而不是“感觉好像可以”。

建议理解到这一步即可：

- 知道模型不是数据库。
- 知道模型不是搜索引擎。
- 知道模型不是完全可靠的执行器。
- 知道它适合做“生成、归纳、改写、初步规划、辅助编码”，但不适合无验证地直接替代人类判断。

### 阶段 4：RAG、MCP、Agent 的基本逻辑

目标：知道这些词分别在解决什么问题。

#### 1. RAG 是什么

RAG 可以简单理解为：“先找资料，再让模型基于资料回答。”

在技术组里的可能用途：

- 用历年题库和文档回答内部问题。
- 用阅卷指南和操作说明做问答助手。
- 用项目文档辅助新同学理解代码仓库。

#### 2. MCP 是什么

MCP 可以简单理解为：“给 AI 一个统一的接口，让它能安全地接到外部工具和数据源上。”

#### 3. Agent 是什么

Agent 不只是“会聊天的模型”，而是：

- 能理解目标。
- 会分步骤。
- 可能调用工具。
- 会根据结果继续行动。

对于新同学，最重要的不是立刻学会复杂多 Agent 编排，而是先学会：

- 给 AI 明确目标。
- 给足上下文。
- 限定输入输出格式。
- 学会验证结果。

### 阶段 5：Claude Code / VS Code AI 插件实操

目标：让 AI 真正帮你干活，而不是只陪你聊天。

你们至少要会做这几件事：

- 让它读一个项目并总结结构。
- 让它解释某个 Python 文件。
- 让它根据 markdown 需求写出一个基础脚本。
- 让它改 bug。
- 让它补注释、补 README、补测试。
- 让它根据已有代码风格继续写新功能。

## 四、建议重点关注的技能方向

为了能更轻松地融入团队工作，建议大家在学习时可以多关注以下几个方向：

### 1. Python 基础

这是我们日常使用的核心工具。多写多练，把基础语法打牢，后面的工作会顺畅很多。强烈建议优先掌握。

### 2. Excel 自动化

在实际工作中，我们会遇到大量基于 Excel 的信息处理任务。掌握 `pandas` 或 `openpyxl` 会让你有如神助，处理速度翻倍。

### 3. 数据库与 SQL

非常推荐大家了解一些数据库基础，这对理解我们数据系统的流转大有裨益。

重点内容：

- 表、行、列的基本概念。
- 主键、外键的作用。
- 基础增删改查（CRUD）。
- 了解“参数化查询”的意义。
- 培养“不要随意操作正式库”的安全意识。

### 4. API 基础

现代应用大多通过 API 交互，了解 HTTP 的 GET/POST 和 JSON 数据格式，能帮你更好地理解系统是怎么运转的。

### 5. 文档与工程习惯

养成写注释、看 README、按规范命名文件和变量的好习惯，这会让你和他人的合作变得非常顺畅和愉快。

### 6. AI 协作开发

把 AI 当成学长学姐，遇到不懂的报错、不理解的代码，多向 AI 提问。熟练配合 AI 开发能极大地缩短你的摸索时间。

## 五、推荐学习资料

### A. 必须看：建立整体直觉

#### 0. 快速入门当前生成式 AI 的原理和逻辑

推荐入口：

- Anthropic Prompt Engineering 文档  
  https://docs.anthropic.com/en/docs/prompt-engineering
- OpenAI Agents 文档  
  https://platform.openai.com/docs/guides/agents

#### 1. 【闪客】一口气拆穿 Skill / MCP / RAG / Agent / OpenClaw 底层逻辑

- https://www.bilibili.com/video/BV1ojfDBSEPv/?share_source=copy_web&vd_source=0546dc1fbd4b2f18e73bc480c8ee827a

#### 2. “如何用 10 个 Claude Code 给自己打工”

推荐官方入口：

- Claude Code Overview  
  https://docs.anthropic.com/en/docs/claude-code/overview
- Claude Code SDK Overview  
  https://docs.anthropic.com/en/docs/claude-code/sdk

### B. Python 基础

1. 菜鸟教程 Python 3  
   https://www.runoob.com/python3/python3-tutorial.html
2. Python 官方教程  
   https://docs.python.org/3/tutorial/

### C. MCP / RAG / Agent

- MCP 官方网站  
  https://modelcontextprotocol.io/
- OpenAI Cookbook：Evaluate RAG with LlamaIndex  
  https://cookbook.openai.com/examples/evaluation/evaluate_rag_with_llamaindex
- OpenAI Cookbook：Multi-Tool Orchestration with RAG approach  
  https://cookbook.openai.com/examples/responses_api/responses_api_tool_orchestration
- OpenAI Agents SDK  
  https://openai.github.io/openai-agents-python/
- OpenAI Agent Evals  
  https://platform.openai.com/docs/guides/agent-evals

### D. 实操时再看

- FastAPI 官方文档  
  https://fastapi.tiangolo.com/
- openpyxl 官方文档  
  https://openpyxl.readthedocs.io/en/stable/
- Pro Git 中文版  
  https://git-scm.com/book/zh/v2

## 六、第三步：自己摸索着安装 Claude Code 或 VS Code 插件

你提到“需要梯子”，这点要实话实说：部分工具和文档访问确实可能受网络环境影响。

建议这样做：

### 方案 A：先装 VS Code 插件

适合刚开始的同学。

### 方案 B：再尝试 Claude Code

适合已经能基本使用终端的同学。

建议安装后先练这几类命令式任务：

- “请先阅读这个项目结构，再告诉我哪些文件最重要。”
- “请解释 `api/main.py` 的每个接口在做什么。”
- “请根据这个 markdown 需求，写一个最小可运行版本。”
- “请先不要改代码，先告诉我你的计划。”
- “请帮我给这个脚本增加异常处理和日志输出。”

## 七、第四步：怎么玩 Claude Code

### 场景 1：读懂项目

```text
请阅读这个项目目录，告诉我：
1. 它是做什么的
2. 入口文件在哪里
3. 哪些文件是我作为新人最该先看的
4. 如果我要修改一个小功能，建议从哪里开始
```

### 场景 2：解释旧脚本

```text
请解释这个 Python 脚本在做什么。
请分成：
1. 输入是什么
2. 处理流程是什么
3. 输出是什么
4. 有哪些风险点
5. 如果要重构，最先改哪三处
```

### 场景 3：根据 markdown 需求生成工具

```text
请根据这个 markdown 文档里的规则，写一个最小可运行的自动阅卷脚本。

要求：
1. 使用 Python
2. 输入为一个 csv 文件，包含学号、题号、学生答案
3. 参考答案从另一个 json 文件读取
4. 输出一个新的 csv，包含每题得分和总分
5. 请先给出实现计划，再开始写代码
6. 代码里加上必要注释
7. 如果规则有歧义，请先列出来，不要直接瞎猜
```

## 八、给新同学的 2 周入门计划

### 第 1 周

- 安装 Python、VS Code。
- 学会运行最简单的 Python 程序。
- 配好一个 AI 插件或 Claude Code。
- 学变量、列表、字典、循环、函数。
- 学文件读写、CSV、Excel 基础。

### 第 2 周

- 尝试阅读开源社区中一个小型 Python 项目的 README 和核心入口文件（如包含 `def main:` 的脚本文件）。
- 阅读并理解一个能够处理 CSV 文件并执行简单条件判断的脚本逻辑。
- 做一个小项目，例如“根据 markdown 里的题目描述要求，写一个能够比对参考答案与学生答案，并输出最终得分到 Excel 的自动化阅卷原型程序”。

## 九、最后的建议

真正的入门标志是：

- 你能把一个需求写成 prompt。
- 你能让 AI 生成一个初版脚本。
- 你能把脚本跑起来。
- 你能修掉第一个报错。

请记住一句话：

**AI 可以帮你更快，但不能帮你免掉理解和验证。**

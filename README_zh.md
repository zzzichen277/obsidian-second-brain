<p align="center">
  <a href="https://github.com/eugeniughelbur/obsidian-second-brain">
    <img src="media/banner.png" alt="obsidian-second-brain：面向 Obsidian 的 Claude Code 技能，让你的知识库成为会自我进化的第二大脑" width="100%" />
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Claude_Code-Skill-blueviolet?style=for-the-badge&logo=anthropic" alt="Claude Code Skill" />
  <img src="https://img.shields.io/badge/Obsidian-Plugin_Ready-7C3AED?style=for-the-badge&logo=obsidian&logoColor=white" alt="Obsidian" />
  <img src="https://img.shields.io/github/v/release/eugeniughelbur/obsidian-second-brain?style=for-the-badge&color=green" alt="Release" />
  <img src="https://img.shields.io/github/license/eugeniughelbur/obsidian-second-brain?style=for-the-badge" alt="License" />
  <img src="https://img.shields.io/github/stars/eugeniughelbur/obsidian-second-brain?style=for-the-badge&color=yellow" alt="Stars" />
</p>

<p align="center">
  <a href="https://oosmetrics.com/repo/eugeniughelbur/obsidian-second-brain"><img src="https://img.shields.io/badge/oosmetrics-%F0%9F%8F%86%20Trending%20repo-DAA520?style=for-the-badge&labelColor=2C2C2C" alt="oosmetrics: trending repo" /></a>
</p>

<h1 align="center">obsidian-second-brain</h1>

<p align="center">
  <strong>这是对 <a href="https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f">Karpathy 的 LLM Wiki 模式</a> 的进化：一个会重写自己的知识库。</strong>
  <br /><br />
  <em>每个新来源都会更新已有页面，而不是只追加新笔记。冲突会自动调和。你睡觉时，知识库也在复利增长。</em>
  <br /><br />
  <em>31 条命令 · 自动综合 · 可“反驳你”的思考工具 · 来自 X / Web / YouTube 的实时研究 · 4 个定时代理 · 4 种角色预设</em>
  <br /><br />
  <a href="#安装后会发生什么">效果演示</a> ·
  <a href="#31-条命令">全部命令</a> ·
  <a href="#安装">安装</a> ·
  <a href="#选择你的预设">预设</a> ·
  <a href="https://github.com/eugeniughelbur/obsidian-second-brain/discussions">讨论区</a>
</p>

<p align="center">
  <strong>长文深度解读：</strong> <a href="https://ghelburlabs.substack.com/p/i-rebuilt-karpathys-llm-wiki-heres">“我重建了 Karpathy 的 LLM Wiki：原版缺了什么”</a><br/>
  <em>为什么仅追加式 LLM Wiki 在规模化后会失效、什么是 AI-First Vault Principle、以及我在第一版踩过的三个坑。</em>
</p>

<p align="center">
  <strong>研究工具箱</strong>：<code>/x-read</code> · <code>/x-pulse</code> · <code>/research</code> · <code>/research-deep</code> · <code>/youtube</code><br/>
  <em>将 X 实时帖子、带引用的网页研究、YouTube 转录直接拉进你的知识库，并以 AI-First 方式保存。<br/>
  Vault-first 综合会先识别你已知内容，再只补齐缺口。</em>
</p>

<p align="center">
  <a href="https://github.com/eugeniughelbur">
    <img src="https://github.com/eugeniughelbur.png" width="72" height="72" alt="Eugeniu Ghelbur" style="border-radius: 50%;" />
  </a>
</p>

<p align="center">
  作者：<strong>Eugeniu Ghelbur</strong> · AI Automation Engineer @ Single Grain<br />
  <em>公开构建 · 分享有效方法</em>
</p>

<p align="center">
  <a href="https://x.com/eugeniu_ghelbur"><img src="https://img.shields.io/badge/Follow_on_X-000?style=for-the-badge&logo=x&logoColor=white" alt="Follow on X" /></a>
  <a href="https://www.linkedin.com/in/eugeniu-ghelbur/"><img src="https://img.shields.io/badge/Connect_on_LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="Connect on LinkedIn" /></a>
  <a href="https://ghelburlabs.substack.com"><img src="https://img.shields.io/badge/Subscribe_on_Substack-FF6719?style=for-the-badge&logo=substack&logoColor=white" alt="Subscribe on Substack" /></a>
  <a href="https://github.com/eugeniughelbur"><img src="https://img.shields.io/badge/Follow_on_GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="Follow on GitHub" /></a>
</p>

---

## 问题

你每天都在用 Claude，但每次会话都从零开始。你要反复解释上下文。对话结束后，信息就散失了。

你也在 Obsidian 记了很多笔记，但它们只是堆在那里。半年前做过的决策又做一遍，想法沉没在 Daily Note 里，没人把点连成线。

**两个强大工具，却彼此割裂。**

---

## 这项技能如何扩展 Karpathy 的 LLM Wiki

Karpathy 的模式很优秀：丢入资料，LLM 生成 wiki 页，再进行问答。这个技能把它推进到下一阶段：

| | Karpathy 的 LLM Wiki | obsidian-second-brain |
|---|---|---|
| **新来源进入** | 追加新页面并交叉引用 | **重写已有页面**：人物更新、观点修订、陈旧事实替换 |
| **冲突处理** | 标记后你手动解决 | `/obsidian-reconcile` 自动调和 |
| **模式发现** | 你问了才出现 | `/obsidian-synthesize` 主动发现未命名模式并写入综合页 |
| **触发方式** | 按需手动运行 | 4 个定时代理：夜间收束、周复盘、冲突清扫、健康检查 |
| **笔记格式** | 面向人阅读的 wiki | AI-First：`## For future Claude` 前言 + frontmatter，优先机器检索与推理 |

如果说 Karpathy 方案是“你用 LLM 维护知识库”，这里就是“知识库自己维护自己”。

---

## 安装后会发生什么

**会后**：`/obsidian-save`  
Claude 自动提取决策、人物、任务、想法并写入对应笔记。

**你录了语音备忘**：`/obsidian-ingest meeting.m4a`  
Whisper 转录、识别说话人、提取承诺和行动项，分发到实体页、任务板和日报。

**你拍了白板**：`/obsidian-ingest photo.png`  
Claude 识别图像结构与文本，创建概念笔记并关联项目。

**你遇到好视频**：`/obsidian-ingest https://youtube.com/...`  
不是做一条摘要，而是直接重写相关页面，自动调和冲突，触发新综合页。

**重大决策前**：`/obsidian-challenge`  
Claude 会用你过去的失败案例和反转决策来“反驳”你，避免重蹈覆辙。

**看全局结构**：`/obsidian-visualize`  
生成可视化 Canvas：中心节点、类型配色、孤儿节点一目了然。

**你睡觉时**：夜间代理会跑 5 个阶段：收束当日、冲突调和、跨源综合、修复孤儿笔记、重建索引。

**新的一天开始**：`/obsidian-daily`  
拉取日历、逾期任务和隔夜变化，形成今日开局上下文。

**有人发来 X 帖子**：`/x-read https://x.com/...`  
Grok 抓取正文、串楼与回复，返回原文、TL;DR、关键观点、情绪分布与重点账号。

**你要规划今日内容**：`/x-pulse "AI automation"`  
扫描 X 热点，给出主题、空白点、有效 hook 和可直接发布的选题。

**你需要严肃研究**：`/research "AI memory tools"`  
Perplexity Sonar Pro 生成带引用档案：摘要、关键事实、时间线、关键玩家、反向观点、延伸阅读、开放问题。

**你要 Vault-first 深度研究**：`/research-deep "AI memory tools"`  
先扫你的库，识别认知缺口，再做定向检索，只补缺不重做，输出增量报告与待更新项。

**你刷到高价值 YouTube**：`/youtube https://youtu.be/...`  
抓转录（免费），可选元数据与热评，再由 Grok 总结成 AI-First 笔记。

**你甚至不需要打开 Obsidian。** 所有动作都能在 Claude 完成。

---

## 前后对比

| | 没有这个技能 | 使用这个技能 |
|---|---|---|
| 保存决策 | 手动复制或遗失 | 自动写入正确项目页 |
| 日报 | 手写且常漏 | 自动创建与更新 |
| 发现模式 | 重读大量笔记 | `/emerge` 自动挖掘 |
| 反思校验 | 没人挑战你 | `/challenge` 用你历史反证 |
| 会话连续性 | 每次重讲背景 | `/world` 10 秒加载上下文 |
| 内容摄入 | 看完就忘 | `/ingest` 1 个来源重写 5-15 页 |
| 冲突事实 | 不知道冲突在哪 | `/reconcile` 自动处理 |
| 综合能力 | 手动连点成线 | `/synthesize` 自动跨源综合 |
| 数据可移植 | 只有 Claude 能读 | `/export` 给任意 AI 工具 |
| 事实随时间变化 | 新信息覆盖旧信息 | 双时间事实记录“何时为真”与“何时得知” |
| 新会话启动 | 重复介绍自己 | `CRITICAL_FACTS.md` 用约 120 token 载入身份 |
| 阅读 X 线程 | 开 X、截图、粘贴 | `/x-read [url]` 一步返回完整分析 |
| 内容选题 | 猜热点 | `/x-pulse` 返回热点+空白+hooks+选题 |
| 网页研究 | 开一堆标签页抄引用 | `/research [topic]` 直接给带时效标记的档案 |
| 已知内容再研究 | 从头重查 | `/research-deep` 先扫库再补缺 |
| YouTube 内容吸收 | 被动观看后遗忘 | `/youtube [url]` 自动沉淀转录与摘要 |
| 面向未来 Claude 的笔记 | 面向人类阅读 | AI-First 规则：前言+时效标记+引用 |

---

## 工作原理

```
  +------------------------------------------+
  |                                          |
  |   LAYER 1: Operations (21 commands)      |
  |   Claude remembers everything            |
  |                                          |
  +------------------------------------------+
  |                                          |
  |   LAYER 2: Thinking Tools (4 commands)   |
  |   Claude thinks with you                 |
  |                                          |
  +------------------------------------------+
  |                                          |
  |   LAYER 3: Context Engine (1 command)    |
  |   Claude knows who you are               |
  |                                          |
  +------------------------------------------+
  |                                          |
  |   LAYER 4: Research Toolkit (5 commands) |
  |   Claude pulls knowledge in              |
  |                                          |
  +------------------------------------------+
  |                                          |
  |   ALWAYS ON                              |
  |   Background agent + 4 scheduled agents  |
  |   Auto-synthesis + save reminders        |
  |                                          |
  +------------------------------------------+
```

**第 1 层**：保存、整理、摄入、调和、导出、维护。  
**第 2 层**：挑战假设、发现隐含模式、跨域连接、把想法升级为项目。  
**第 3 层**：加载你的身份与状态，让会话无缝接续。  
**第 4 层**：引入外部实时知识（X、Web、YouTube），并与本库融合。  
**Always On**：后台代理和定时代理持续维护知识库。

---

## 31 条命令

### Operations（记忆层）

| 命令 | 作用 |
|---|---|
| `/obsidian-save` | 从当前对话保存决策、任务、人物、想法 |
| `/obsidian-ingest` | 输入 URL/PDF/音频/截图，知识库会重写自身（每源可影响 5-15 页） |
| `/obsidian-synthesize` | 自动发现跨来源模式并创建综合页 |
| `/obsidian-reconcile` | 发现并调和冲突 |
| `/obsidian-export` | 导出任意 AI 可读的 JSON/Markdown 快照 |
| `/obsidian-daily` | 创建或更新今日日报 |
| `/obsidian-log` | 记录工作会话并自动回链 |
| `/obsidian-task` | 把任务写入正确看板（含优先级与截止时间） |
| `/obsidian-person` | 创建或更新人物笔记 |
| `/obsidian-decide` | 把决策写入对应项目笔记 |
| `/obsidian-capture` | 零摩擦灵感捕获 |
| `/obsidian-find` | 带上下文的智能检索 |
| `/obsidian-recap` | 日/周/月总结 |
| `/obsidian-review` | 结构化周复盘或月复盘 |
| `/obsidian-board` | 看板查看与更新 |
| `/obsidian-project` | 项目页（含看板与日报关联） |
| `/obsidian-health` | 知识库体检（冲突、缺口、陈旧断言、孤儿笔记） |
| `/obsidian-adr` | 架构决策记录（ADR） |
| `/obsidian-visualize` | 生成可视化 Canvas 地图 |
| `/obsidian-learn` | 回顾学习条目、清理陈旧内容、提炼可升级规则 |
| `/obsidian-init` | 生成 `_CLAUDE.md`、`index.md`、`log.md` |

### Thinking（思考层）

| 命令 | 作用 |
|---|---|
| `/obsidian-challenge` | 用你的历史来质疑你的当前想法 |
| `/obsidian-emerge` | 从近 30 天笔记中发现你未命名的模式 |
| `/obsidian-connect [A] [B]` | 连接两个不相关领域，激发新思路 |
| `/obsidian-graduate` | 把碎片想法升级为完整项目与任务 |

### Context（上下文层）

| 命令 | 作用 |
|---|---|
| `/obsidian-world` | 以渐进 token 预算（L0-L3）加载身份和状态 |

### Research（研究层）

由 xAI Grok（X 实时访问）+ Perplexity Sonar（Web 研究）+ YouTube 驱动。结果会作为 AI-First 笔记保存到 `Research/`。

| 命令 | 作用 |
|---|---|
| `/x-read [url]` | 深读 X 帖子：原文+线程+TL;DR+观点+情绪+关键账号 |
| `/x-pulse [topic]` | 扫描 X 热点：主题、声音、hook、选题 |
| `/research [topic]` | 带引用的网页研究档案，含时效标记与开放问题 |
| `/research-deep [topic]` | Vault-first 深研：先扫库找缺口，再定向检索并回写 |
| `/youtube [url]` | 提取转录+元数据+热评并生成 AI-First 摘要 |

**设置方式**：复制 `.env.example` 到 `~/.config/obsidian-second-brain/.env` 并填入密钥。运行 `install.sh` 并在研究工具提示时输入 `y` 可自动完成。

<details>
<summary><strong>查看 thinking 工具示例</strong></summary>

<br />

**`/obsidian-challenge`**

你说：“我想把 API 全部重写成 Rust。”

Claude 会找到你 2025 年 Rust 重写失败复盘，也会找到你曾承诺 2 年内坚持 TypeScript 的决策记录，然后反问你是否仍要推进。

---

**`/obsidian-emerge`**

Claude 扫描近 30 天日报，发现你在 4 个看似无关项目中都提到“onboarding friction”。

它会指出：“这是你跨项目的瓶颈，只是你还没给它命名。”

---

**`/obsidian-connect "distributed systems" "cooking"`**

它沿着链接图追踪两簇知识，发现“预处理、负载分配”等共通机制，产出可执行的交叉想法。

---

**`/obsidian-graduate`**

三周前的一个想法碎片，Claude 会自动补齐目标、阶段、任务与看板条目，并打上 `graduated` 标签。

</details>

<details>
<summary><strong>查看 /obsidian-ingest 示例</strong></summary>

<br />

```text
/obsidian-ingest https://youtube.com/watch?v=example
```

1. 原始资料保存到 `raw/videos/`（不可变）
2. 重写实体页面
3. 若新增深度或发生冲突则重写概念页
4. 出现模式时生成综合页
5. 调和冲突并记录原因
6. 更新 `index.md`、`log.md`、日报

**一个 URL 进来，整库会自我重写。**

</details>

<details>
<summary><strong>查看研究工具箱示例</strong></summary>

<br />

**`/x-read https://x.com/garrytan/status/2048121438914154664`**

使用具备 X 实时访问能力的 Grok 抓取正文与回复，返回原文、TL;DR、关键观点、情绪结构、反方观点与“值得跟踪的声音”。约 `$0.05/次`。

---

**`/x-pulse "AI automation"`**

```text
WHAT'S HOT (last 24-72h)
  1. Agentic AI vs Basic Automation
  2. Self-Improving Sovereign Agents
  3. Control Layers & Execution Gaps

WHAT'S UNDEREXPLORED
  - 非开发者小企业用户的 ROI 数据
  - 数字代理与实体机器人协作

HOOKS THAT ARE WORKING
  - "Automation executes. Autonomy reasons."

POST IDEAS FOR YOU TODAY
  1. 线程：开源代理如何在独立仓库中自我改进
  2. 单条：为什么“自动化执行，自治推理”是控制层分界线
```

你原本可能要刷 2 小时，30 秒左右可得结果。约 `$0.13/次`。

---

**`/research "AI memory tools"`**

输出结构化档案：Summary、Key Facts（每条含 `(as of YYYY-MM, source.com)`）、Timeline、Key Players、Contrarian Views、Further Reading、Open Questions。保存到 `Research/Web/`。约 `$0.05/次`。

---

**`/research-deep "AI memory tools"`（核心能力）**

```text
Phase 1: Vault scan
  找到 8 条相关笔记（例如 Mem0 vs Letta）

Phase 2: Gap analysis
  识别 3-5 条定向检索问题

Phase 3: Targeted research
  [web] Claude memory tool 2026 新特性
  [web] Mem0 融资后的争议点
  [x]   Letta vs Mem0 开发者观点

Phase 4: Synthesis
  - 与知识库基线相比的新信息
  - 已确认信息
  - 待调和冲突（含 [[wikilinks]]）
  - 建议更新动作（供 /obsidian-save 执行）
```

Vault-first 的意义是：不再浪费 token 重查已知内容。约 `$0.40/次`。

---

**`/youtube https://youtu.be/...`**

通过 `youtube-transcript-api` 免费获取转录；可选调用 YouTube Data API v3 获取元数据和评论；再由 Grok 生成 TL;DR、要点、引用、主题、评论情绪与后续建议。约 `$0.04/次`。

---

**自动打开新笔记**：每次保存后可自动在 Obsidian 打开。批量写入时可设置 `RESEARCH_AUTOOPEN=0` 关闭。

</details>

---

## 你的知识库是“活的”

传统知识库像档案柜：放进去，就静置。

这个知识库每次输入都会自我更新：

- **摄入新来源**：重写已有页面、调和冲突、合成模式
- **保存会话**：实体、概念、决策自动分发
- **发起提问**：Two-Output Rule 让答案同时变成更新
- **事实变化**：双时间事实记录“何时真实”与“何时被知识库学习到”
- **你什么都不做**：后台与定时代理继续维护
- **等一周**：自动综合会写出跨来源连接页

一周后的知识库，会和初始状态本质不同。

---

## 选择你的预设

初始化时选择角色。每个预设会生成对应目录结构、模板和看板。

| 预设 | 适用人群 | 看板风格 |
|---|---|---|
| **executive** | 创始人、运营、管理者 | OKRs / Quarterly / Weekly |
| **builder** | 开发者、工程师、架构师 | Backlog / Sprint / Done |
| **creator** | 写作者、YouTuber、营销人员 | Ideas / Drafts / Published |
| **researcher** | 学术研究者、分析师、深度研究者 | Reading / Processing / Synthesized |

```bash
python bootstrap_vault.py --path ~/my-vault --name "Your Name" --preset builder
```

如果不选预设，会创建通用结构。

---

## 后台代理与定时代理

**后台代理**：每次 context compact 后触发。你继续工作，库在后台更新。

```text
PostCompact -> obsidian-bg-agent.sh -> claude -p (headless) -> vault updated
```

**定时代理：**

| 代理 | 时间 | 工作内容 |
|---|---|---|
| `morning` | 早 8 点 | 生成今日日报 + 逾期任务 |
| `nightly` | 晚 10 点 | 日终收束：收尾 + 调和 + 综合 + 修复孤儿 |
| `weekly` | 周五晚 6 点 | 周复盘 |
| `health` | 周日晚 9 点 | 知识库健康审计 |

**保存提醒**：当对话超过 10 轮或你说“done/thanks”时，Claude 会提醒执行 `/obsidian-save`，避免会话信息丢失。

---

## 知识库架构

### Wiki 风格（默认）- LLM First

Claude 既是读者也是写者，Vault 是数据库。

```text
vault/
+-- _CLAUDE.md          # 操作手册
+-- index.md            # 页面目录（Claude 最先读取）
+-- log.md              # 活动时间线
+-- SOUL.md             # 你的身份画像
+-- CRITICAL_FACTS.md   # 约 120 token，始终加载（时区、上级、地点等）
+-- raw/                # 不可变原始资料
+-- wiki/               # Claude 工作区
|   +-- entities/       # 人、公司、工具
|   +-- concepts/       # 概念、框架、综合
|   +-- projects/       # 项目页
|   +-- daily/          # 日报
|   +-- logs/           # 工作日志
|   +-- reviews/        # 周/月复盘
|   +-- tasks/          # 任务页
|   +-- decisions/      # ADR
+-- boards/             # 看板
+-- templates/          # 模板
```

<details>
<summary><strong>Obsidian 风格（可选）- 适合日常手动浏览</strong></summary>

```text
vault/
+-- Daily/, Projects/, People/, Ideas/, Knowledge/
+-- Dev Logs/, Tasks/, Reviews/, Boards/, Templates/
```

```bash
python bootstrap_vault.py --path ~/my-vault --name "Your Name" --style obsidian
```

</details>

---

## 安装

一行安装：

```bash
curl -fsSL https://raw.githubusercontent.com/eugeniughelbur/obsidian-second-brain/main/scripts/quick-install.sh | bash
```

或两步安装：

```bash
git clone https://github.com/eugeniughelbur/obsidian-second-brain ~/.claude/skills/obsidian-second-brain
bash ~/.claude/skills/obsidian-second-brain/scripts/setup.sh "/path/to/your/vault"
```

然后执行：`/obsidian-init`

### 研究工具箱（可选）

5 条研究命令需要 API Key。运行 `install.sh` 并在提示时输入 `y` 可自动配置 `~/.config/obsidian-second-brain/.env`；也可手动：

```bash
mkdir -p ~/.config/obsidian-second-brain
cp .env.example ~/.config/obsidian-second-brain/.env
chmod 600 ~/.config/obsidian-second-brain/.env
# 然后把密钥填进去
uv sync   # 安装 Python 依赖
```

所需密钥：

| Key | 获取地址 | 用于 | 费用 |
|---|---|---|---|
| `XAI_API_KEY` | [console.x.ai](https://console.x.ai) | `/x-read`、`/x-pulse`、`/research-deep` 的 X 检索、`/youtube` 摘要 | 按量计费，约 `$0.05/次` |
| `PERPLEXITY_API_KEY` | [perplexity.ai/settings/api](https://perplexity.ai/settings/api) | `/research`、`/research-deep` | 按量计费，约 `$0.02-$0.50/次` |
| `YOUTUBE_API_KEY` | [console.cloud.google.com](https://console.cloud.google.com) | `/youtube` 元数据与评论（可选） | 免费层 1 万单位/日 |

即使不配置这些 Key，其余 26 条 Vault 命令仍可正常使用。

---

## FAQ

### 什么是 Claude Code Skill？
Claude Code Skill 是可复用的行为包，供 Anthropic 的 Claude Code CLI 自动加载。它可以打包斜杠命令、脚本、参考资料和操作规则，让 Claude 在特定领域具备稳定能力。

### 这是 Obsidian 插件还是 Claude Code Skill？
这是 **Claude Code Skill**，不是 Obsidian 插件。插件运行在 Obsidian 内；Skill 运行在 Claude Code（终端 AI 代理）内，从 Obsidian 外部读写并推理你的 Vault。

### 与普通 Obsidian 插件有什么区别？
Obsidian 插件受限于 Obsidian API；Claude Skill 受限于 Claude 在 shell 中可执行的能力。因此它能做很多插件做不到的事，比如实时网页研究、定时代理、跨年笔记综合。

### 如何把这个技能加到 Claude Code？
运行上面的安装命令。它会把仓库克隆到 `~/.claude/skills/obsidian-second-brain`，并把命令软链接到 `~/.claude/commands/`。安装后重启 Claude Code。

### 支持 Obsidian Sync 吗？
支持。该技能只写标准 Markdown 文件，Obsidian Sync、iCloud、Syncthing、Git 同步都可兼容。

### 一定要 API Key 吗？
不需要。原有 26 条 Vault 命令无需 Key。只有 5 条研究命令（`/x-read`、`/x-pulse`、`/research`、`/research-deep`、`/youtube`）需要对应服务 Key。

### 和 Notion AI 或 Mem 有何不同？
Notion AI / Mem 是闭源 SaaS。此技能把数据保存在你本地 Obsidian Markdown 中，不锁定厂商，随时可迁移。

### 什么是 AI-first vault 规则？
笔记优先写给未来的 Claude 检索与推理，而不是优先给人阅读。包含机器可读结构、每条断言的时效标记、强制 `[[wikilinks]]`、原始 URL、置信度。规范见 [`references/ai-first-rules.md`](references/ai-first-rules.md)。

### 运行在现有 Vault 上安全吗？
安全。不会未经确认进行破坏性删除或覆盖。旧笔记保持原样，新笔记遵循 AI-first 规则。`/obsidian-health` 会标记旧格式笔记，便于你按计划渐进迁移。

### `/research-deep` 比 `/research` 多了什么？
`/research` 是单次查询并输出档案；`/research-deep` 先扫现有笔记，识别你已知内容，再做 3-5 个定向补缺查询，输出增量报告（新增、确认、冲突、更新建议）。

### 研究命令大概多少钱？
以 2026-04 为例：`/x-read` 约 `$0.05`，`/x-pulse` 约 `$0.13`，`/research` 约 `$0.04`，`/research-deep` 约 `$0.40-$0.80`，`/youtube` 约 `$0.04`。Grok 调用费用记录在 `~/.research-toolkit/usage.log`。

### Windows/Linux 可用吗？
核心 Vault 命令可在 Claude Code 支持的平台运行。研究工具当前主要按 macOS 路径与行为测试（`~/.config`、`open` 命令）。欢迎 PR 补齐 Windows/Linux 适配。

### 如何升级到最新版？

```bash
cd ~/.claude/skills/obsidian-second-brain && git pull
```

无需重新初始化，命令会自动使用新指令。版本细节见 [CHANGELOG.md](CHANGELOG.md)。

### 去哪里提 issue 或需求？
GitHub Issues：<https://github.com/eugeniughelbur/obsidian-second-brain/issues>  
欢迎 PR，见下方 Contributing。

---

## 理念

很多“第二大脑”工具把你变成了资料管理员。

这个技能反过来：你专注思考、工作、表达；Claude 负责记忆，并用这份记忆帮助你思考得更好，自动暴露盲区、挑战惯性、连接弱关联、提炼潜在模式。

知识库不是“变大”，而是“进化”。

**你的笔记，就是你的护城河。**

灵感来源：[Andrey Karpathy 的 LLM-Wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)。

---

## 贡献

欢迎 PR：

- 新的 thinking 工具
- 新笔记类型 schema（习惯、书籍、投资等）
- MCP 集成（Calendar、Linear、Slack）
- 替代性 Vault 结构
- VS Code / Cursor 配置指南

---

## 作者

Built by **Eugeniu Ghelbur**

[![X](https://img.shields.io/badge/X-@eugeniu__ghelbur-000000?style=flat-square&logo=x)](https://x.com/eugeniu_ghelbur)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-eugeniu--ghelbur-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/eugeniu-ghelbur/)
[![GitHub](https://img.shields.io/badge/GitHub-eugeniughelbur-181717?style=flat-square&logo=github)](https://github.com/eugeniughelbur/)
[![Substack](https://img.shields.io/badge/Substack-ghelburlabs-FF6719?style=flat-square&logo=substack)](https://ghelburlabs.substack.com/)

---

## 许可证

MIT


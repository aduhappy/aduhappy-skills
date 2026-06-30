# 🎯 aduhappy-skills — 我的 AI Agent Skill 备忘录

> 个人收藏的 ZCode / Claude Code / Codex 技能插件速查表。
> 新设备一键恢复：把下面的安装指令发给 AI Agent 即可批量部署。

---

## 🚀 快速安装指令（18 个可自动安装）

把以下内容发给你的 AI Agent 即可一键安装这些 Skill：

```
请帮我安装以下 GitHub 上的 AI Agent Skill：

1. 科研写作助手：https://github.com/Norman-bury/research-writing-skill
2. Nature级表达与绘图：https://github.com/Yuan1z0825/nature-skills
3. 学术全流程管理：https://github.com/Imbad0202/academic-research-skills
4. 科研PDF深度解析：https://github.com/Rimagination/scansci-pdf
5. 研究问题打磨：https://github.com/Rimagination/good-question
6. 科研叙事写作：https://github.com/Rimagination/good-story
7. 学术图表生成（仅限Codex）：https://github.com/keros68/abstract-fig
8. 学术论文MCP检索：https://github.com/Rimagination/instsci
9. 中文去AI痕迹：https://github.com/op7418/Humanizer-zh
10. 软件著作权自动生成：https://github.com/Fokkyp/SoftwareCopyright-Skill
11. 设计感PPT生成：https://github.com/op7418/guizang-ppt-skill
12. 中文PPT模板填充：https://github.com/GordenSun/GordenPPTSkill
13. HTML演示文稿：https://github.com/lewislulu/html-ppt-skill
14. 可编辑PPTX生成：https://github.com/hugohe3/ppt-master
15. 前端幻灯片预览：https://github.com/zarazhangrui/frontend-slides
16. HTML模板库：https://github.com/zarazhangrui/beautiful-html-templates
17. 多智能体协作文档：https://github.com/aduhappy/multi-agent-project-skill
18. GEE/geemap 工作流：https://github.com/sadassimov/geemu-skill

大礼包请安装：https://github.com/K-Dense-AI/scientific-agent-skills
```

> ⚠️ 以下两个 Skill 需要安装配套客户端/网关程序，**建议手动安装**，详见下方说明：
> - **ChatMem**（桌面客户端）→ 见 #18
> - **OneFind**（网关程序）→ 见 #20

## 🔄 检查本地已安装 Skill 是否有更新

把以下内容发给 AI Agent，它会逐个对比本地 SKILL.md 与远程仓库版本，列出有更新的 Skill：

```
请帮我检查以下已安装的 Skill 是否有远程更新（对比本地 SKILL.md 和 GitHub 最新版本）：

独立 Skill：
1. https://github.com/Norman-bury/research-writing-skill
2. https://github.com/Yuan1z0825/nature-skills
3. https://github.com/Imbad0202/academic-research-skills
4. https://github.com/Rimagination/scansci-pdf
5. https://github.com/Rimagination/good-question
6. https://github.com/Rimagination/good-story
7. https://github.com/keros68/abstract-fig
8. https://github.com/Rimagination/instsci
9. https://github.com/op7418/Humanizer-zh
10. https://github.com/Fokkyp/SoftwareCopyright-Skill
11. https://github.com/op7418/guizang-ppt-skill
12. https://github.com/GordenSun/GordenPPTSkill
13. https://github.com/lewislulu/html-ppt-skill
14. https://github.com/hugohe3/ppt-master
15. https://github.com/zarazhangrui/frontend-slides
16. https://github.com/zarazhangrui/beautiful-html-templates
17. https://github.com/aduhappy/multi-agent-project-skill
18. https://github.com/sadassimov/geemu-skill

大礼包：
19. https://github.com/K-Dense-AI/scientific-agent-skills

如果发现某个 Skill 有更新，显示具体差异（commit hash 或关键变更），并询问我是否要更新。
```

---

## 📦 一、独立 Skill

### 🎓 学术科研与论文写作

#### 1. scientific-writing — 科研写作助手

科研写作助手。规范 IMRAD 流程，支持解析 LaTeX 模板，拒绝 AI 盲目扩写和乱编参考文献。

> **⚠️ 注意**
> - 输出为 `.md` / `.tex` / `.py`，最终排版需在 Word 中完成
> - 严禁编造文献和数据，引用必须可溯源

```
请帮我安装 skill：https://github.com/Norman-bury/research-writing-skill
```

#### 2. nature-skills — Nature 级学术表达与绘图

Nature 级学术表达与绘图。润色为顶刊风格语言，辅助编写符合顶刊要求的科研图表代码。包含 scientific-visualization 和 scientific-schematics。

> **⚠️ 注意**
> - 必须复制整个 skill 目录（含 `references/`、`scripts/`、`static/`）和 `skills/_shared/`，否则子技能报错

```
请帮我安装 skill：https://github.com/Yuan1z0825/nature-skills
注意：安装时必须连同 skills/_shared/ 目录一起复制，不要只复制 SKILL.md
```

#### 3. academic-research-skills — 学术全流程管理

学术全流程管理。从梳理大纲到定稿一条龙，能学习你的写作风格，有防泄密保护。包含 literature-review、citation-management、peer-review。

> **⚠️ 注意**
> - **必需** `ANTHROPIC_API_KEY`（运行成本约 $4-6/篇 1.5 万字论文）
> - 许可证 CC-BY-NC 4.0（非商业用途）

```
请帮我安装 skill：https://github.com/Imbad0202/academic-research-skills
注意：需要配置 ANTHROPIC_API_KEY 环境变量
```

#### 4. scansci-pdf — 科研 PDF 深度解析

科研 PDF 深度解析。精准读取复杂论文（公式、双栏排版、图表数据）。包含 pdf。基于 PyPI 包 `scansci-pdf`，通过 MCP 协议工作。

> **⚠️ 注意**
> - 建议用 `pip install scansci-pdf` 安装编译版核心（性能更好），GitHub 克隆版为纯 Python 回退
> - 登录验证（WebVPN/CARSI）在你自己的浏览器中进行，密码不经过工具

```
请帮我安装 skill：https://github.com/Rimagination/scansci-pdf
注意：建议用 pip install scansci-pdf 安装以获取编译版核心（性能更好）
```

#### 5. good-question — 研究问题打磨

研究问题打磨。把一个模糊想法打磨成有杀伤力的研究问题，自动生成 Good Question Card（含关键假设、竞争假说、可行性实验、审稿人预判）。支持多种模式（mentor / reviewer / collaborator / grant）。

> **⚠️ 注意**
> - 无运行时依赖，纯 SKILL.md + 方法卡片工作流
> - 触发方式：`$good-question` + 你的想法/方向

```
请帮我安装 skill：https://github.com/Rimagination/good-question
```

#### 6. good-story — 科研叙事写作

科研叙事写作助手。将零散的研究结果转化为有说服力的论文叙事，自动识别最强主线、检测过度声明（如相关说成因果）、校准子领域证据标准。支持生成 cover letter 和审稿人预判回复。

> **⚠️ 注意**
> - 无运行时依赖，纯 SKILL.md + 方法卡片工作流
> - 触发方式：`$good-story` + 研究材料/草稿
> - 不会隐瞒阴性结果或虚构共识，故事必须忠实于证据

```
请帮我安装 skill：https://github.com/Rimagination/good-story
```

#### 7. abstract-fig — 学术图表 draw.io 生成 ⚠️ 仅限 Codex

基于 Codex 的 image2 图像生成能力，将论文内容转化为可编辑的 draw.io 学术图表（图形摘要、概念模型、机制示意图、工作流图等）。输出 `.drawio` 文件，可在 [app.diagrams.net](https://app.diagrams.net/) 中继续编辑。

> **⚠️ 注意**
> - **仅限 Codex**：依赖 Codex 内置 `image2`（OpenAI 图像生成模型），其他 Agent 无法完整运行
> - 如需在 Claude Code / ZCode 中使用，仅可参考 SKILL.md 流程手动实现

```
请帮我安装 skill：https://github.com/keros68/abstract-fig
注意：此 Skill 仅限 Codex 使用，需要 Codex 内置的 image2 图像生成能力
```

#### 8. instsci — 学术论文 MCP 检索

学术论文检索工具（MCP + CLI）。优先 Open Access（Unpaywall/arXiv/Semantic Scholar），付费论文自动弹出浏览器窗口走机构权限（Shibboleth/CARSI/WebVPN）。支持批量下载和多家出版社工作流。

> **⚠️ 注意**
> - 安装：`git clone` + `pip install -e .`
> - AI Agent 使用需运行 `instsci-mcp` 启动 MCP 服务器
> - 机构登录（SSO/2FA）在你的浏览器中手动完成，密码不经过工具

```
请帮我安装 skill：https://github.com/Rimagination/instsci
注意：需要 git clone 后 pip install -e . 安装 Python 包，AI 使用需启动 MCP 服务器（instsci-mcp）
```

### ✍️ 文本润色与去 AI 痕迹

#### 9. humanizer-zh — 中文去 AI 痕迹

中文 AI 写作去痕。识别并消除"AI 套话"，让表达更符合真实人类中文书写习惯。识别 4 大类 24 种 AI 写作模式。

> **⚠️ 注意**
> - 无任何依赖（不需要 Python、API Key 或系统软件），最轻量的 Skill

```
请帮我安装 skill：https://github.com/op7418/Humanizer-zh
```

### 🔧 开发辅助与知识产权

#### 10. software-copyright-materials — 软件著作权自动生成

软件著作权自动生成。一键抽取前后 30 页代码，生成软著申请说明书和操作手册。**完全免费**。

> **⚠️ 注意**
> - 必需 Python 3.10+ 和 `python-docx`；完整功能需 .NET SDK 8.0+
> - 提交网站：中国版权保护中心（ccopyright.com.cn）

```
请帮我安装 skill：https://github.com/Fokkyp/SoftwareCopyright-Skill
注意：需要先安装 python-docx（pip install python-docx），完整功能需要 .NET SDK 8.0+
```

### 📽️ PPT 制作与演示

#### 11. guizang-ppt-skill — 设计感网页 PPT

设计感网页 PPT 生成。提供 Editorial 杂志风（10 种版式）和瑞士国际主义（22 种版式）两种视觉系统，单文件 HTML 输出。支持多平台社交封面、可选图像生成（Codex 专属功能）。

> **⚠️ 注意**
> - 需要文件读写 + shell 执行权限的 AI Agent 环境（Claude Code / Codex / Cursor 等）
> - 许可证 AGPL-3.0

```
请帮我安装 skill：https://github.com/op7418/guizang-ppt-skill
```

#### 12. GordenPPTSkill — 中文 PPT 模板填充

中文 PPT 模板填充。内置 17 套精调中文商务 PPTX 模板，非破坏性文本编辑（布局不变）。支持 DeepSeek、Claude、GPT 等多种 LLM。

> **⚠️ 注意**
> - 必需 Python + `python-pptx 1.0+`
> - 依赖微软雅黑字体，非 Windows 系统需手动配置字体映射
> - **个人/研究用途，禁止商用，禁止转载模板**

```
请帮我安装 skill：https://github.com/GordenSun/GordenPPTSkill
注意：需要先安装 python-pptx（pip install python-pptx）
```

#### 13. html-ppt-skill — HTML 演示文稿工厂

HTML 演示文稿工厂。36 种主题、31 种页面版式、47 种动画效果，纯静态 HTML/CSS/JS（无构建步骤）。独创演讲者模式（Presenter Mode）：S 键打开双屏，含逐字稿和计时器。

```
请帮我安装 skill：https://github.com/lewislulu/html-ppt-skill
```

#### 14. ppt-master — 可编辑 PPTX 生成

可编辑 PPTX 生成。将 PDF/DOCX/Markdown 等源文档转为原生可编辑的 PPTX（DrawingML 格式，可在 PowerPoint 中直接修改）。支持动画、幻灯片备注、模板填充模式。

> **⚠️ 注意**
> - 必需 Python 3.10+，运行 `pip install -r requirements.txt`
> - 效果上限取决于 AI 模型能力，推荐 Claude + gpt-image-2
> - 免费工具，仅需支付 AI 模型调用费用

```
请帮我安装 skill：https://github.com/hugohe3/ppt-master
注意：需要 Python 3.10+ 并安装依赖（pip install -r requirements.txt）
```

#### 15. frontend-slides — 前端幻灯片预览

前端幻灯片预览。先看视觉预览再选择风格，降低设计决策门槛。支持从 PPTX 导入、12 种内置预设 + 34 种 Bold 模板包、Vercel 一键部署。

> **⚠️ 注意**
> - 适用于所有代码 Agent（Codex / Claude Code / Kimi Code / Gemini CLI 等）
> - PPTX 导入依赖 Python + python-pptx
> - PDF 导出依赖 Node.js + Playwright

```
请帮我安装 skill：https://github.com/zarazhangrui/frontend-slides
```

#### 16. beautiful-html-templates — HTML 模板库

高质量 HTML 幻灯片模板库。34 套成品 HTML 模板，附 screenshots 预览和 index.json 目录，Agent 可自动匹配用户需求并克隆改编。常与 frontend-slides 配合使用。

> **⚠️ 注意**
> - 纯 HTML + JS 模板，浏览器即可查看
> - 常作为 frontend-slides 的模板来源

```
请帮我安装 skill：https://github.com/zarazhangrui/beautiful-html-templates
```

### 🤖 多智能体协作与项目管理

#### 17. multi-agent-project-skill — 跨 Agent 协作文档脚手架

跨 Agent、跨工具的可恢复项目文档脚手架。基于 AGENTS.md 开放标准（agents.md），生成纯 Markdown 协作结构：AGENTS.md + 任务卡片 + 数据来源溯源 + 决策记录（ADR）+ 进度日志 + STATUS.md 状态移交。任何 Agent（Claude/Cursor/Gemini/ZCode/Codex）读取同一入口即可接力工作。

> **⚠️ 注意**
> - 无需运行时依赖，只需 AI Agent 的 Markdown 读取能力
> - 中文文件名（任务规划_模板.md、来源.txt）在某些工具链中可能有编码/路径问题，可重命名为 ASCII
> - 安装方式：直接告诉 Agent "把 aduhappy/multi-agent-project-skill 装成 skill"

```
请帮我安装 skill：https://github.com/aduhappy/multi-agent-project-skill
```

### 💾 对话增强与记忆 ⚠️ 建议手动安装

#### 18. chatmem — 智能体长短期记忆

智能体长短期记忆。结构化后台记忆库，解决超长项目和连贯工作中的上下文断层问题。

> **⚠️ 手动安装说明（不建议自动安装）**
> - **Tauri 桌面应用**，需下载安装包：[GitHub Releases](https://github.com/Rimagination/ChatMem/releases)
> - 安装后在桌面应用中：**Settings → Agent Integrations → "一键安装到全部"**
> - 会自动检测 Claude Code / Codex / Gemini CLI / OpenCode 配置，写入 MCP 服务器条目并备份原配置
> - 安装后需**完全退出并重新打开**目标 Agent

```
⚠️ 此 Skill 建议手动安装，不要自动安装：
1. 下载 ChatMem 桌面客户端：https://github.com/Rimagination/ChatMem/releases
2. 安装后在 Settings → Agent Integrations 中点击"一键安装到全部"
3. 完全退出并重新打开你的 AI Agent
```

### 🌍 地理与遥感

#### 19. geemu-skill — GEE / geemap 工作流

GEE / geemap 工作流。Google Earth Engine 遥感脚本、影像处理、数据导出。

> **⚠️ 注意**
> - 必须完整克隆整个仓库（含 `jsonl` 向量库数十 MB），不能选择性复制
> - 需配置 Google Earth Engine 凭证和 Google Cloud 项目 ID

```
请帮我安装 skill：https://github.com/sadassimov/geemu-skill
注意：必须完整克隆整个仓库（包含 jsonl 向量库），需先配置 Earth Engine 认证和 Google Cloud 项目 ID
```

### 🔍 本地知识库检索 ⚠️ 建议手动安装

#### 20. onefind — 本地知识库优先检索

本地知识库优先检索。支持 Obsidian / Zotero / EndNote / Notion / Mendeley / Citavi 多源统一检索。

> **⚠️ 手动安装说明（不建议自动安装）**
> - **Windows 专属闭源安装程序**：[GitHub Releases](https://github.com/iawnfoanaowt/OneFind/releases)
> - 安装时至少填写**一个知识库路径**（Zotero / Mendeley / Citavi / Obsidian / Notion / EndNote）
> - EndNote、本地文件夹接口、Office/CAJ 分析需发送机器码到 `zhtaogis@163.com` 获取免费授权
> - **Deep 模式**（GPU 深度检索）需约 10 GB 磁盘空间，推荐 NVIDIA GPU

```
⚠️ 此 Skill 建议手动安装，不要自动安装：
1. 下载 OneFind 安装程序：https://github.com/iawnfoanaowt/OneFind/releases
2. 运行安装包，填写至少一个知识库路径（如 Zotero 数据库位置）
3. 可选：导入授权文件（EndNote/文件夹/Office 分析需要）
4. 可选：选择 Deep 模式（需 10GB 空间 + 推荐 NVIDIA GPU）
5. 在 Codex 中用 $ 调用，授予完整权限
推荐同时安装 LibreOffice（解析 Office 文档）和 Zotero（文献检索）
```

---

## 🧬 二、科学智能体大礼包

> 来源：[K-Dense-AI/scientific-agent-skills](https://github.com/K-Dense-AI/scientific-agent-skills) ⭐ 25.8k
> 内置 130+ 技能，调用 70+ 权威科学数据库。以下为已安装的子 Skill：

### 🔬 科学方法论

| Skill | 说明 |
|-------|------|
| **scientific-brainstorming** | 创意研究头脑风暴，探索跨学科连接和研究空白 |
| **scientific-critical-thinking** | 科学论证质量评估，识别偏差和混杂因素，GRADE/Cochrane 分级 |
| **hypothesis-generation** | 从观察数据中生成可检验的假设 |
| **consciousness-council** | 多视角辩论委员会，模拟不同学术观点碰撞 |

### 📊 数据分析与可视化

| Skill | 说明 |
|-------|------|
| **scientific-visualization** | Nature/Science/Cell 级别出版图表，多面板布局，色盲安全色板 |
| **scientific-schematics** | AI 迭代生成出版级科学示意图（网络架构、流程图、通路图） |
| **matplotlib** | Matplotlib 绑定，通用绑图 |
| **seaborn** | Seaborn 统计可视化绑定 |
| **exploratory-data-analysis** | 探索性数据分析全流程 |
| **statistical-analysis** | 统计分析方法与报告 |
| **infographics** | 信息图表设计 |

### 🤖 机器学习与深度学习

| Skill | 说明 |
|-------|------|
| **scikit-learn** | Scikit-learn 绑定，经典机器学习 |
| **scikit-survival** | 生存分析绑定 |
| **pytorch-lightning** | PyTorch Lightning 训练流程 |
| **transformers** | HuggingFace Transformers 绑定 |
| **stable-baselines3** | 强化学习算法绑定 |
| **shap** | SHAP 可解释性分析 |
| **optimize-for-gpu** | GPU 性能优化建议 |
| **pufferlib** | 并行训练工具库 |

### 📐 数学与建模

| Skill | 说明 |
|-------|------|
| **sympy** | 符号计算绑定 |
| **pymc** | 贝叶斯建模绑定 |
| **pymoo** | 多目标优化绑定 |
| **simpy** | 离散事件仿真绑定 |
| **timesfm-forecasting** | 时序预测绑定 |
| **umap-learn** | UMAP 降维可视化 |
| **fluidsim** | 流体仿真绑定 |
| **networkx** | 图论与网络分析 |

### 📚 文献与学术工具

| Skill | 说明 |
|-------|------|
| **paper-lookup** | 论文查找 |
| **paperzilla** | 论文管理与解析 |
| **bgpt-paper-search** | BGP 论文搜索 |
| **peer-review** | 同行评审结构化写作 |
| **citation-management** | 文献引用管理 |
| **scholar-evaluation** | 学者评估与评分 |
| **research-grants** | 科研基金申请撰写 |
| **venue-templates** | 期刊/会议模板（Nature, Science 等） |
| **open-notebook** | 开放实验笔记 |
| **labarchive-integration** | LabArchive 实验室档案集成 |
| **iso-13485-certification** | ISO 13485 医疗器械认证文档 |

### 📑 文档与演示

| Skill | 说明 |
|-------|------|
| **scientific-writing** | 科研论文 IMRAD 结构写作 |
| **scientific-slides** | 科学演示幻灯片 |
| **latex-posters** | LaTeX 学术海报 |
| **pptx-posters** | PowerPoint 学术海报 |
| **markdown-mermaid-writing** | Markdown + Mermaid 图表文档 |
| **docx** | Word 文档生成与处理 |
| **pdf** | PDF 读取/合并/拆分/OCR |
| **pptx** | PowerPoint 生成与处理 |
| **xlsx** | Excel 电子表格处理 |
| **markitdown** | 文件转 Markdown（Word/PDF/Excel 等） |

### 🔍 搜索与数据获取

| Skill | 说明 |
|-------|------|
| **exa-search** | Exa AI 搜索引擎绑定 |
| **parallel-web** | 并行网页抓取 |
| **database-lookup** | 数据库查询绑定 |
| **get-available-resources** | 可用资源检测 |
| **what-if-oracle** | 假设分析推理引擎 |

### 🌍 地球科学与化学

| Skill | 说明 |
|-------|------|
| **geomaster** | 地球科学综合绑定 |
| **geopandas** | GeoPandas 空间数据分析 |
| **astropy** | 天文学绑定 |
| **datamol** | 分子化学/药物设计绑定 |
| **dhdna-profiler** | DNA 高通量数据分析 |

### 💻 大数据与计算

| Skill | 说明 |
|-------|------|
| **dask** | Dask 分布式计算绑定 |
| **polars** | Polars 高性能 DataFrame |
| **vaex** | Vaex 超大规模数据处理 |
| **zarr-python** | Zarr N 维数组存储 |
| **statsmodels** | 统计建模与假设检验 |
| **modal** | Modal 云计算绑定 |
| **hugging-science** | HuggingFace 科学模型 |

### 🎨 其他工具

| Skill | 说明 |
|-------|------|
| **matlab** | MATLAB 编程绑定 |
| **market-research-reports** | 市场调研报告生成 |
| **usfiscaldata** | 美国财政数据分析 |
| **generate-image** | AI 图像生成 |
| **autoskill** | 自动技能选择 |
| **gtars** | GTARS 工具绑定 |
| **adaptyv** | 自适应可视化绑定 |
| **aeon** | 时间序列分析绑定 |
| **pyzotero** | Zotero 编程接口绑定 |

---

## 📋 三、环境推荐

### Anaconda（推荐安装）

> **不加入系统 PATH**，始终通过完整路径调用，避免与系统 Python 冲突。

| 项目 | 路径（示例） |
|------|------|
| conda | `D:\Anaconda\condabin\conda.bat` |
| python | `D:\Anaconda\python.exe` |
| pip | `D:\Anaconda\Scripts\pip.exe` |

安装后建议按需创建独立环境，例如：

```
conda create -n gee python=3.10    # Google Earth Engine
conda create -n yolov python=3.10  # YOLO 目标检测
conda create -n swat python=3.11  # SWAT 水文模型
```

### 其他推荐软件

| 软件 | 用途 |
|------|------|
| [MinerU](https://github.com/opendatalab/MinerU) | 开源 PDF 解析工具，精准提取学术论文中的公式、表格、图片，转为 Markdown/LaTeX，适合配合科研 Skill 处理复杂版面论文 |

---

<p align="center">
  <sub>Built with ❤️ by <a href="https://github.com/aduhappy">aduhappy</a></sub>
</p>

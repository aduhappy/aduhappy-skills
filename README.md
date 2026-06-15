# 🎯 Happy — 我的 AI Agent Skill 备忘录

> 个人收藏的 ZCode / Claude Code / Codex 技能插件速查表。
> 新设备一键恢复：把下面的安装指令发给 AI Agent 即可批量部署。

---

## 🚀 快速安装指令（7 个可自动安装）

把以下内容发给你的 AI Agent 即可一键安装这些 Skill：

```
请帮我安装以下 GitHub 上的 AI Agent Skill：

1. 科研写作助手：https://github.com/Norman-bury/research-writing-skill
2. Nature级表达与绘图：https://github.com/Yuan1z0825/nature-skills
3. 学术全流程管理：https://github.com/Imbad0202/academic-research-skills
4. 科研PDF深度解析：https://github.com/Rimagination/scansci-pdf
5. 中文去AI痕迹：https://github.com/op7418/Humanizer-zh
6. 软件著作权自动生成：https://github.com/Fokkyp/SoftwareCopyright-Skill
7. GEE/geemap 工作流：https://github.com/sadassimov/geemu-skill

大礼包请安装：https://github.com/K-Dense-AI/scientific-agent-skills
```

> ⚠️ 以下两个 Skill 需要安装配套客户端/网关程序，**建议手动安装**，详见下方说明：
> - **ChatMem**（桌面客户端）→ 见 #8
> - **OneFind**（网关程序）→ 见 #9

## 🔄 检查本地已安装 Skill 是否有更新

把以下内容发给 AI Agent，它会逐个对比本地 SKILL.md 与远程仓库版本，列出有更新的 Skill：

```
请帮我检查以下已安装的 Skill 是否有远程更新（对比本地 SKILL.md 和 GitHub 最新版本）：

独立 Skill：
1. https://github.com/Norman-bury/research-writing-skill
2. https://github.com/Yuan1z0825/nature-skills
3. https://github.com/Imbad0202/academic-research-skills
4. https://github.com/Rimagination/scansci-pdf
5. https://github.com/op7418/Humanizer-zh
6. https://github.com/Fokkyp/SoftwareCopyright-Skill
7. https://github.com/sadassimov/geemu-skill

大礼包：
8. https://github.com/K-Dense-AI/scientific-agent-skills

如果发现某个 Skill 有更新，显示具体差异（commit hash 或关键变更），并询问我是否要更新。
```

---

## 📦 一、独立 Skill

### 🎓 学术科研与论文写作

#### 1. scientific-writing — 科研写作助手

科研写作助手。规范 IMRAD 流程，支持解析 LaTeX 模板，拒绝 AI 盲目扩写和乱编参考文献。

> **⚠️ 注意事项**
> - **不会直接生成 .docx**，输出为 `.md` / `.tex` / `.py` 项目文件，最终排版需在 Word 中完成
> - **严禁编造文献和数据**，引用必须可溯源；高风险结论需用户二次核实
> - 可选依赖：Python + Miniconda（可复现图表脚本）、Pandoc（Markdown→Word）、LaTeX（编译）

```
请帮我安装 skill：https://github.com/Norman-bury/research-writing-skill
```

#### 2. nature-skills — Nature 级学术表达与绘图

Nature 级学术表达与绘图。润色为顶刊风格语言，辅助编写符合顶刊要求的科研图表代码。包含 scientific-visualization 和 scientific-schematics。

> **⚠️ 注意事项**
> - **必须安装整个 skill 目录**，不能只复制 `SKILL.md`（依赖 `references/`、`scripts/`、`static/` 等资源）
> - **必须同时复制 `skills/_shared/` 目录**，否则 nature-reader、nature-writing 等子技能会报错
> - 绘图强制使用三组 rcParams：`font.family=sans-serif`、`font.sans-serif=['Arial',...]`、`svg.fonttype='none'`
> - 可选环境变量：`NCBI_API_KEY`（提高 PubMed 速率限制）

```
请帮我安装 skill：https://github.com/Yuan1z0825/nature-skills
注意：安装时必须连同 skills/_shared/ 目录一起复制，不要只复制 SKILL.md
```

#### 3. academic-research-skills — 学术全流程管理

学术全流程管理。从梳理大纲到定稿一条龙，能学习你的写作风格，有防泄密保护。包含 literature-review、citation-management、peer-review。

> **⚠️ 注意事项**
> - **必须有 `ANTHROPIC_API_KEY`**（必需），运行成本约 $4-6/篇 1.5 万字论文
> - **完整性检查门（Stage 2.5 / 4.5）不可跳过**，强制走完整流程
> - AI 是副驾驶不是主驾驶——只做苦力（文献、格式、验证），不替你写论文
> - 不用于隐藏 AI 使用痕迹，目标是真正提升写作质量
> - 可选：`S2_API_KEY`（Semantic Scholar 限流）、Pandoc（DOCX 输出）、tectonic（PDF 输出）
> - 许可证：CC-BY-NC 4.0（**非商业用途**）

```
请帮我安装 skill：https://github.com/Imbad0202/academic-research-skills
注意：需要配置 ANTHROPIC_API_KEY 环境变量
```

#### 4. scansci-pdf — 科研 PDF 深度解析

科研 PDF 深度解析。精准读取复杂论文（公式、双栏排版、图表数据）。包含 pdf。基于 PyPI 包 `scansci-pdf`，通过 MCP 协议工作。

> **⚠️ 注意事项**
> - **核心模块 `src/scansci_pdf/_core/*.pyx` 是专有的**（Cython 编译），GitHub 克隆版用纯 Python 回退（功能相同，性能略低）
> - 登录验证（WebVPN/CARSI/EZProxy）在**你自己的浏览器**中进行，密码不经过工具
> - 默认开启 Sci-Hub（`scihub_enabled=true`），受限地区请配置 Tor/FlareSolverr 或改用 `legal_only` 策略
> - 可选：Elsevier API Key（免费，加速 ScienceDirect 下载）
> - 配置项：`download_strategy`（fastest/oa_first/scihub_only/legal_only）、`output_dir`、`batch_workers`（默认 10）

```
请帮我安装 skill：https://github.com/Rimagination/scansci-pdf
注意：建议用 pip install scansci-pdf 安装以获取编译版核心（性能更好），GitHub 克隆版为纯 Python 回退
```

### ✍️ 文本润色与去 AI 痕迹

#### 5. humanizer-zh — 中文去 AI 痕迹

中文 AI 写作去痕。识别并消除"AI 套话"，让表达更符合真实人类中文书写习惯。识别 4 大类 24 种 AI 写作模式。

> **⚠️ 注意事项**
> - **无任何依赖**：不需要 Python、API Key 或系统软件，是最轻量的 Skill
> - 翻译自 `blader/humanizer`，核心规则基于维基百科"AI 写作特征"
> - 作者明确声明：**不是用于欺骗 AI 检测器**，而是真正提升写作质量；最好的"去 AI"方法是真实的人类思考

```
请帮我安装 skill：https://github.com/op7418/Humanizer-zh
```

### 🔧 开发辅助与知识产权

#### 6. software-copyright-materials — 软件著作权自动生成

软件著作权自动生成。一键抽取前后 30 页代码，生成软著申请说明书和操作手册。**完全免费**。

> **⚠️ 注意事项**
> - **必需依赖**：Python 3.10+ 和 `python-docx`（`pip install python-docx`）
> - 可选：.NET SDK 8.0+（完整 DOCX OpenXML 生成），无 .NET 时使用基础 DOCX 回退
> - **不生成也不编造源代码**，代码材料必须来自你的真实项目
> - 自动应用"前 30 页 + 后 30 页"规则；源码不足 60 页时生成全部
> - `.docx` 是本地可编辑草稿，官方提交前需**导出为 PDF**
> - 输出目录：`<项目>/软件著作权申请资料/正式资料/`
> - 提交网站：中国版权保护中心（ccopyright.com.cn）
> - 许可证：MIT

```
请帮我安装 skill：https://github.com/Fokkyp/SoftwareCopyright-Skill
注意：需要先安装 python-docx（pip install python-docx），完整功能需要 .NET SDK 8.0+
```

### 💾 对话增强与记忆 ⚠️ 建议手动安装

#### 7. chatmem — 智能体长短期记忆

智能体长短期记忆。结构化后台记忆库，解决超长项目和连贯工作中的上下文断层问题。

> **⚠️ 手动安装说明（不建议自动安装）**
> - 这是一个 **Tauri 桌面应用**，不是纯 Skill 文件，需要下载安装包
> - 下载地址：[GitHub Releases](https://github.com/Rimagination/ChatMem/releases)（Windows `.exe` / `.msi`，macOS `.dmg`）
> - 安装后在桌面应用中：**Settings → Agent Integration → "一键安装到全部"**
> - 会自动检测 Claude Code / Codex / Gemini CLI / OpenCode 配置，写入 MCP 服务器条目并备份原配置
> - 安装后需**完全退出并重新打开**目标 Agent
> - ChatMem 是 MCP 后端工具，不是 `@chatmem` 提及
> - macOS 包未做 Apple Developer ID 签名，首次打开需在系统设置中允许

```
⚠️ 此 Skill 建议手动安装，不要自动安装：
1. 下载 ChatMem 桌面客户端：https://github.com/Rimagination/ChatMem/releases
2. 安装后在 Settings → Agent Integrations 中点击"一键安装到全部"
3. 完全退出并重新打开你的 AI Agent
```

### 🌍 地理与遥感

#### 8. geemu-skill — GEE / geemap 工作流

GEE / geemap 工作流。Google Earth Engine 遥感脚本、影像处理、数据导出。

> **⚠️ 注意事项**
> - **必须安装完整文件夹**，不能选择性复制文件，尤其不能遗漏 `gee_vector_db/chunks.jsonl` 和 `documents.jsonl`（数十 MB），否则检索失败
> - **必须有 Google Earth Engine 凭证**和 Google Cloud Project ID
> - 受限网络需配置代理环境变量
> - 安装后运行 `scripts/check_local_environment.py` 检查环境（Python、geemap、EE 凭证、项目 ID）
> - 无需向量搜索服务器、嵌入模型下载或私有凭证，检索基于关键词评分

```
请帮我安装 skill：https://github.com/sadassimov/geemu-skill
注意：必须完整克隆整个仓库（包含 jsonl 向量库），安装前需配置好 Earth Engine 认证和 Google Cloud 项目 ID
```

### 🔍 本地知识库检索 ⚠️ 建议手动安装

#### 9. onefind — 本地知识库优先检索

本地知识库优先检索。支持 Obsidian / Zotero / EndNote / Notion / Mendeley / Citavi 多源统一检索。

> **⚠️ 手动安装说明（不建议自动安装）**
> - 这是一个 **Windows 专属的闭源安装程序**，不是纯 Skill 文件
> - 下载地址：[GitHub Releases](https://github.com/iawnfoanaowt/OneFind/releases)
> - 默认安装路径：`C:\Users\<用户>\.codex\Function\OneFind`
> - 安装时至少填写**一个知识库路径**（Zotero / Mendeley / Citavi / Obsidian / Notion / EndNote）
> - **部分数据源需要授权**：EndNote、本地文件夹接口、Office/CAJ 分析功能需发送机器码到 `zhtaogis@163.com` 获取免费个人授权
> - **Deep 模式**（GPU 深度检索）需约 **10 GB 磁盘空间**，推荐 NVIDIA GPU
> - 安装时推荐使用 VPN（下载速度依赖网络）
> - 许可证：个人学习/研究用途；商用需联系 `zhtaogis@163.com` 授权

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
| **multi-agent-project** | 多智能体协作项目管理 |
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
| [ZCode](https://zcode.ai) | AI 编程助手（本仓库 Skill 的运行平台） |
| [ChatMem](https://github.com/Rimagination/ChatMem) | 智能体长短期记忆 |
| [OneFind](https://github.com/iawnfoanaowt/OneFind) | 本地多源知识库统一检索 |
| [Zotero](https://www.zotero.org/) | 文献管理 |
| [LibreOffice](https://www.libreoffice.org/) | 开源办公套件（OneFind 需要） |
| [MinerU](https://github.com/opendatalab/MinerU) | PDF 学术公式/图表提取 |
| [Node.js](https://nodejs.org/) | ZCode 运行依赖 |

---

<p align="center">
  <sub>Built with ❤️ by <a href="https://github.com/aduhappy">aduhappy</a></sub>
</p>

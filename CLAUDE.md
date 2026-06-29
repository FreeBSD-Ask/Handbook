# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 仓库概览

这是 FreeBSD 官方手册（FreeBSD Handbook）的中文翻译项目。基于 GitBook 格式，发布在 <https://handbook.bsdcn.org>。

源内容为 Markdown 文件，由 GitBook 平台自动构建和部署，无需本地构建步骤。

**翻译基准：** 以 FreeBSD 最新 RELEASE 版本为准，翻译源为 <https://docs.freebsd.org/en/books/handbook/book/>。

## 内容架构

### 核心文件

- **`SUMMARY.md`** — 全书唯一数据源，定义完整目录结构和导航树。GitBook 用它来生成侧边栏。 **第一行 `# Table of contents` 绝对不能变更** ，否则 GitBook 同步失效。
- **`mu-lu.md`** — 由 `mulu.yml` CI 工作流从 `SUMMARY.md` 自动复制生成，**不要手动编辑** 。
- **`yi-zhe-shuo-ming.md`** — 术语翻译对照表，所有术语翻译以此为准。
- **`CHANGELOG.md`** — 编辑日志，记录翻译进度和同步上游的 commit。

### 目录结构

- 章节目录遵循 `di-X-zhang-<主题>/` 命名模式（拼音 slug）
- 每节为独立 `.md` 文件，如 `di-1-zhang-jian-jie/1.1.-gai-shu.md`
- 前言在 `qian-yan/`，附录在 `fu-lu-X/`
- 分部介绍页如 `di-yi-bu-fen-kuai-su-kai-shi.md`
- `.gitbook/assets/` — GitBook 静态资源（logo 等）
- 全书共 35 章（Ch1-Ch35），中文章号与英文原版 1:1 对应；Ch18 为「OCI 容器」，于 2026-06 由英文原版补译
- 章节结构对比脚本位于 `script/compare_structure_v2.py`，可检测中英文版本子章节级差异
- `en/` — 英文 AsciiDoc 原版归档（40 个子目录，每个含 `_index.adoc`），用于翻译对照参考；不要修改或翻译其中的内容

### 标题管理（关键约束）

`senc-headers.yml` 工作流会在每次 push 时自动将 `SUMMARY.md` 中的标题同步到对应 `.md` 文件的 H1。 **这意味着直接编辑 `.md` 文件的 `# 标题` 会被 CI 覆盖。** 修改章节标题时，只改 `SUMMARY.md` 中对应的 `* [标题](路径)` 条目即可。

## CI/CD 工作流

所有工作流位于 `.github/workflows/`：

| 工作流 | 触发条件 | 说明 |
| ------ | -------- | ---- |
| `sync-headers.yml` | push | 从 SUMMARY.md 同步一级标题到各 .md 文件 |
| `mulu.yml` | SUMMARY.md 变更时 push | 复制 SUMMARY.md → mu-lu.md |
| `markdown-lint2.yml` | workflow_dispatch | markdownlint 检查，规则见 `.github/.markdownlint.json` |
| `md-padding.yml` | workflow_dispatch | 自动在 CJK 与英文/数字间添加空格 |
| `AutoCorrect.yml` | --- | 自动修正常见中文笔误与格式问题 |
| `links.yml` | 定时 + workflow_dispatch | lychee 死链检查，配置见 `.github/lychee.toml` |
| `file-name-check.yml` | --- | 检查 SUMMARY.md 中引用的文件是否存在 |
| `create-pdf.yml` | --- | 导出 PDF |

## 编写规范

### 格式

- **命令行前缀：** `#` 表示 root 权限，`$` 表示普通用户。不要使用 `sudo`。
- **提示块：** tip/important/note/warning/caution 使用 `>` 缩进引用，关键词 **加粗**。
- **代码块：** 使用 ` ```sh ` 兜底，禁止使用 text 作为代码块标记
- **表格：** 一律居中。
- **禁止 HTML：** 本项目不支持任何 HTML 语法。
- **文件命名：** 使用拼音 slug，文件名中不得包含空格、中文字符或英文冒号 `:`，必须兼容 Windows 操作系统对文件名的要求。
- **路径与 IP：** 全书正文中的路径（带 `/` 或 `\` 的，如 `/etc/rc.conf`、`/usr/local/etc/`）和 IP 地址一律使用 **加粗**，不使用反引号 `` ` `` 包裹；不要混合使用 `*` 和 `` ` ``（如 `*`path`*` 是错误的）。
- **命令、选项、参数：** 命令、选项、可调选项、可调参数等格式使用 `行间代码`（反引号）包裹。
- **转义字符：** 含转义字符 `\` 的元素一律使用 `行间代码` 包裹整个元素，不在正文中直接使用转义字符（如写 `PROTO\_TYPE` 而非 `PROTO\_TYPE` 在正文里裸露）。逐个手动修改，禁止批量替换。
- **避免滥用"已"字：** 如"XX 已新增"应改为"新增 XX"；"已修复"应改为"修复完成"。
- **禁止篡改：** 不要篡改软件版本号、用户名、带圈数字（如 ①②③ 等），确保其位置、数量和英语原文一致。
- **避免章节交叉引用：** 正文不要出现具体的章节交叉引用（如"参见第 5 章"），改用语义化链接或省略。

### 术语

- `ports` 保持英文不翻译（注意区分真正的"端口"）
- "Jail" 保持英文（不翻译为"监狱"、"监牢"）
- "拷贝" → "复制"，"壳/外壳" → "shell"
- 第二人称一律使用"你"而非"您"
- 所有术语翻译见 `yi-zhe-shuo-ming.md` 对照表

### CJK 空格

中英文、中文与数字之间必须加半角空格。文件和命令名用 `` ` `` 括起来。`md-padding.yml` 和 `AutoCorrect.yml` 工作流会自动检测修复。

### 图片

在正文中插入图片，使用 markdown 格式。

### 翻译流程

1. 参考官方英文手册原文进行人工校对
2. 提交 PR 到 main 分支

### 翻译校对工作流程（Claude Code）

对已翻译章节进行质量审校时，参考以下步骤：

1. **获取原文**：通过 `WebFetch` 抓取对应章节的英文原版页面（`https://docs.freebsd.org/en/books/handbook/<chapter-slug>/`），获取完整的英文文本。

2. **逐句对照**：将中文翻译与英文原文逐句比对，重点检查以下问题类别：

   | 问题类型 | 示例 |
   | -------- | ---- |
   | 事实性错误 | "large parts" 误译为"三个文件" |
   | 漏译 | 英文原版有但中文缺失的句子 |
   | 机翻腔/表达生硬 | "在阅读本章后，你将会收获" → "通过阅读本章，你将了解" |
   | 用词不当 | "独家优势"应为"主要优势"（原文 "particular strengths"） |
   | 版本过时 | 15.0-CURRENT 未同步至 16.0-CURRENT |
   | 语法/文字错误 | 重复字词、"非常地"应为"非常" |

3. **提交修改**：
   - 基于 `main` 创建分支 `fix/chapter-X-translation`
   - 仅提交修改的 `.md` 文件，不要包含无关文件
   - 提交信息格式：`fix: 修正第 X 章翻译错误及同步英文原版更新`
   - 用 `gh pr create` 创建 PR，目标分支为 `main`
   - PR 描述中列出每处修改及原因

4. **注意事项**：
   - 不要修改 `# 标题`——会被 `sync-headers.yml` CI 覆盖
   - 保持术语一致性，参考 `yi-zhe-shuo-ming.md`
   - 英文原文可能比翻译版本更新，版本号差异（如 15.0 vs 16.0）应以英文原版为准
   - 添加新内容（如英文原版新增的段落）时，确保翻译风格与上下文一致
   - 禁止篡改带圈数字，如 ①②③ 等，确保其位置、数量和英语原文一致
   - 禁止篡改代码块（包括 shell 命令、配置文件内容、ini 段等），仅修改正文翻译
   - 禁止篡改用户名、邮箱、URL、IP 地址等技术参数
   - 禁止篡改软件版本号
   - 以英文原版 `docs.freebsd.org/en/books/handbook/` 为唯一权威源；禁止以中文版已有翻译作为修改依据，避免错误沿袭

5. **逐句校对递归工作流**（核心约束）：
   - **逐行逐句子**遍历内容，检查逻辑一致性，联网复核后修改
   - **三轮 + 一轮复查**：完整执行三轮逐句校对，然后严格、完整地复查一轮；若仍有问题，继续执行三轮，递归直至无问题
   - **逐个修改**：修改时禁止机械修改、禁止批量；必须逐个手动修改，禁止使用软件工具批量替换或批量逐个复核
   - **修改前后复核**：每次修改前确认问题真实存在、修改后确认改动准确且未引入新错误
   - **不复查旧错**：不得复查以前已经完成三轮的错误；每轮查询内容必须是新的（若与之前的复查重复则跳过、不改，只看是否有新增内容）
   - **联网复查**：对于不存在的实际访问查询（如失效链接、版本号、API 端点），需联网复查三次后修改
   - **禁止绕过审查**：不得以任何方式搜索、批量、绕过逐句子审查流程

## Lint 配置

- **markdownlint**（`.github/.markdownlint.json`）：本地已安装 `markdownlint-cli2 v0.22.1`（基于 `markdownlint v0.40.0`），可在本地直接运行检查与修复
  - **本地运行命令**（在仓库根目录执行）：

    ```sh
    # 检查全部中文 .md（排除 en/、.github/、.gitbook/、node_modules/、script/）
    markdownlint-cli2 "**/*.md" "!en/**" "!.github/**" "!.gitbook/**" "!node_modules/**" "!script/**" --config .github/.markdownlint.json

    # 自动修复可修复的问题（MD012 多余空行、MD047 末尾换行、MD034 裸 URL 等）
    markdownlint-cli2 "**/*.md" "!en/**" "!.github/**" "!.gitbook/**" "!node_modules/**" "!script/**" --config .github/.markdownlint.json --fix
    ```

  - **MD060 表格列风格规则（重要）**：配置为 `"style": "compact"` + `"aligned_delimiter": true`
    - **compact 风格**：管道符两侧各保留**单个空格**，例如 `| cell1 | cell2 |`；空单元格写作 `| |`（不是 `||` 或 `|  |`）
    - **aligned_delimiter**：分隔行 `|---|` 的管道符位置必须与表头行的管道符位置对齐
    - **CJK 显示宽度**：markdownlint 按**显示宽度**计算列位置，**每个中文字符按 2 宽度**计算（与英文 1 宽度不同）。因此含 CJK 的列宽 = CJK 字符数 × 2 + ASCII 字符数 × 1
    - **分隔行 dash 数量公式**：若某列内容显示宽度为 W，则分隔行该列总宽（含两侧空格）也应为 W，dash 数量 = W − 4（减去前后各 1 空格 + 前后各 1 冒号）。例如列内容 `FreeBSD 版本` 显示宽度 = 7+1+4 = 12，分隔行应为 ` :--------: `（8 个 dash）
    - **常见错误修复**：当 markdownlint 报 `MD060/table-column-style [Table pipe does not align with header for option "aligned_delimiter"]` 时，需手动扩展分隔行 dash 数量，使管道符位置与表头按显示宽度对齐；`--fix` 无法自动修复此类问题
  - **MD056 表格列数规则**：表头声明几列，所有数据行都必须有几列；末尾缺空单元格时需补 `| |`，而非省略管道符
- **textlint**（`.textlintrc`）：仅启用 `ja-space-between-half-and-full-width` 规则，用于 CJK/英文空格检查
- **lychee**（`.github/lychee.toml`）：6 线程、30 并发、30 秒超时、最多 3 次重试、Chrome UA、排除私有 IP 和 `ftp.freebsd.org`

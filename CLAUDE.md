# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 仓库概览

这是 FreeBSD 官方手册（FreeBSD Handbook）的中文翻译项目。基于 GitBook 格式，发布在 <https://handbook.bsdcn.org>。

源内容为 Markdown 文件，由 GitBook 平台自动构建和部署，无需本地构建步骤。

**翻译基准：** 以 FreeBSD 最新 RELEASE 版本为准，翻译源为 <https://docs.freebsd.org/en/books/handbook/>。

## 内容架构

### 核心文件

- **`SUMMARY.md`** — 全书唯一数据源，定义完整目录结构和导航树。GitBook 用它来生成侧边栏。**第一行 `# Table of contents` 绝对不能变更**，否则 GitBook 同步失效。
- **`mu-lu.md`** — 由 `mulu.yml` CI 工作流从 `SUMMARY.md` 自动复制生成，**不要手动编辑**。
- **`yi-zhe-shuo-ming.md`** — 术语翻译对照表，所有术语翻译以此为准。
- **`CHANGELOG.md`** — 编辑日志，记录翻译进度和同步上游的 commit。

### 目录结构

- 章节目录遵循 `di-X-zhang-<主题>/` 命名模式（拼音 slug）
- 每节为独立 `.md` 文件，如 `di-1-zhang-jian-jie/1.1.-gai-shu.md`
- 前言在 `qian-yan/`，附录在 `fu-lu-X/`
- 分部介绍页如 `di-yi-bu-fen-kuai-su-kai-shi.md`
- `.gitbook/assets/` — GitBook 静态资源（logo 等）

### 标题管理（关键约束）

`senc-headers.yml` 工作流会在每次 push 时自动将 `SUMMARY.md` 中的标题同步到对应 `.md` 文件的 H1。**这意味着直接编辑 `.md` 文件的 `# 标题` 会被 CI 覆盖。**修改章节标题时，只改 `SUMMARY.md` 中对应的 `* [标题](路径)` 条目即可。

## CI/CD 工作流

所有工作流位于 `.github/workflows/`：

| 工作流 | 触发条件 | 说明 |
|---|---|---|
| `sync-headers.yml` | push | 从 SUMMARY.md 同步一级标题到各 .md 文件 |
| `mulu.yml` | SUMMARY.md 变更时 push | 复制 SUMMARY.md → mu-lu.md |
| `markdown-lint2.yml` | workflow_dispatch | markdownlint 检查，规则见 `.github/.markdownlint.json` |
| `md-padding.yml` | workflow_dispatch | 自动在 CJK 与英文/数字间添加空格 |
| `AutoCorrect.yml` | - | 自动修正常见中文笔误与格式问题 |
| `links.yml` | 定时 + workflow_dispatch | lychee 死链检查，配置见 `.github/lychee.toml` |
| `file-name-check.yml` | - | 检查 SUMMARY.md 中引用的文件是否存在 |
| `create-pdf.yml` | - | 导出 PDF |

## 编写规范

### 格式

- **命令行前缀：** `#` 表示 root 权限，`$` 表示普通用户。不要使用 `sudo`。
- **提示块：** tip/important/note/warning/caution 使用 `>` 缩进引用，关键词**加粗**。
- **代码块：** 使用 ` ```shell-session `，**不要**添加多余标记如 ` ```bash `。
- **表格：** 一律居中。
- **禁止 HTML：** 本项目不支持任何 HTML 语法。
- **文件命名：** 使用拼音 slug，文件名中不得包含空格、中文字符或英文冒号 `:`。

### 术语

- `ports` 保持英文不翻译（注意区分真正的"端口"）
- "Jail" 保持英文（不翻译为"监狱"、"监牢"）
- "拷贝" → "复制"，"壳/外壳" → "shell"
- 第二人称一律使用"你"而非"您"
- 所有术语翻译见 `yi-zhe-shuo-ming.md` 对照表

### CJK 空格

中英文、中文与数字之间必须加半角空格。文件和命令名用 `` ` `` 括起来。`md-padding.yml` 和 `AutoCorrect.yml` 工作流会自动检测修复。

### 图片

翻译者不要在正文中插入图片，在需要插图的位置标记：

```
【——————————-此处需要插入图片­——————————————-】
```

并主动告知维护者哪一小节需要插图。

### 翻译流程

1. 使用 DeepL 机器翻译（<https://www.deepl.com/zh/translator>），严禁其他翻译网站
2. 参考官方英文手册原文进行人工校对
3. 提交 PR 到 main 分支

### 翻译校对工作流程（Claude Code）

对已翻译章节进行质量审校时，参考以下步骤：

1. **获取原文**：通过 `WebFetch` 抓取对应章节的英文原版页面（`https://docs.freebsd.org/en/books/handbook/<chapter-slug>/`），获取完整的英文文本。

2. **逐句对照**：将中文翻译与英文原文逐句比对，重点检查以下问题类别：

   | 问题类型 | 示例 |
   |---|---|
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

## Lint 配置

- **markdownlint**（`.github/.markdownlint.json`）：禁用了 MD013（行长度）、MD033（HTML）、MD010（tab）、MD036（无强调作标题）、MD040（围栏代码块语言）、MD045（无 alt 文本图片）等规则
- **textlint**（`.textlintrc`）：仅启用 `ja-space-between-half-and-full-width` 规则，用于 CJK/英文空格检查
- **lychee**（`.github/lychee.toml`）：6 线程、30 并发、30 秒超时、最多 3 次重试、Chrome UA、排除私有 IP 和 `ftp.freebsd.org`

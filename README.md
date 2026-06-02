# FreeBSD 中文手册

[![翻译进度](https://img.shields.io/badge/翻译进度-校对中-blue)](CHANGELOG.md)
[![GitHub stars](https://img.shields.io/github/stars/FreeBSD-Ask/Handbook)](https://github.com/FreeBSD-Ask/Handbook/stargazers)

FreeBSD 官方手册（FreeBSD Handbook）的中文翻译项目，基于 GitBook 格式，发布在 <https://handbook.bsdcn.org>。

## 项目状态

**翻译基准：** 以 FreeBSD 最新 RELEASE 版本为准，翻译源为 <https://docs.freebsd.org/en/books/handbook/book/>。

**校对进度：**
- ✅ 第 1-34 章已完成机器翻译
- ✅ 第 1-9 章已完成人工校对
- ✅ 第 10-34 章已完成人工校对（2026.6.2）

**当前状态：** 翻译校对工作已基本完成，持续进行质量改进和英文原版同步。

## 快速开始

### 本地预览

本项目基于 GitBook 格式，可通过 GitBook 平台或本地工具预览：

```bash
# 安装 GitBook CLI
npm install -g gitbook-cli

# 本地预览
gitbook serve
```

### 目录结构

```
Handbook/
├── SUMMARY.md          # 全书目录结构（GitBook 数据源）
├── CHANGELOG.md        # 编辑日志和翻译进度
├── yi-zhe-shuo-ming.md # 术语翻译对照表
├── qian-yan/           # 前言
├── di-1-zhang-*/       # 第 1 章
├── di-2-zhang-*/       # 第 2 章
├── ...
├── di-34-zhang-*/      # 第 34 章
└── fu-lu-*/            # 附录
```

## 贡献指南

欢迎社区通过 PR 贡献力量！请遵循以下规范：

### 翻译规范

1. **术语一致性**：参考 [术语翻译对照表](yi-zhe-shuo-ming.md)
2. **CJK 空格**：中英文、中文与数字之间必须加半角空格
3. **命令行前缀**：`#` 表示 root 权限，`$` 表示普通用户
4. **禁止 HTML**：本项目不支持任何 HTML 语法
5. **文件命名**：使用拼音 slug，禁止空格、中文字符或英文冒号

### 标题管理

**重要：** 章节标题必须通过 `SUMMARY.md` 修改，直接编辑 `.md` 文件的 `# 标题` 会被 CI 覆盖。

### 提交流程

1. Fork 本仓库
2. 创建特性分支：`git checkout -b fix/chapter-X-translation`
3. 提交修改：`git commit -m "fix: 修正第 X 章翻译错误"`
4. 推送分支：`git push origin fix/chapter-X-translation`
5. 创建 Pull Request

### 校对工作流程

参考 [CLAUDE.md](CLAUDE.md) 中的翻译校对工作流程：

1. 通过 WebFetch 获取英文原版
2. 逐句对照，检查翻译问题
3. 提交修改并创建 PR

## 相关链接

- **官方原址：** <https://docs.freebsd.org/en/books/handbook/>
- **中文发布：** <https://handbook.bsdcn.org>
- **编辑日志：** [CHANGELOG.md](CHANGELOG.md)
- **术语对照：** [yi-zhe-shuo-ming.md](yi-zhe-shuo-ming.md)
- **旧版存档：** <https://www.alipan.com/s/9rUaCHKauvC>

## 许可证

本项目遵循 [BSD 2-Clause 许可证](LICENSE)。

## 致谢

感谢所有为本项目贡献翻译和校对工作的社区成员！

# 贡献指南

感谢你愿意为本项目贡献代码。本文档说明参与协作时需要遵守的约定。

## 开始之前

- 提交 Issue 前请先搜索是否已有相同问题。
- 较大的改动建议先开 Issue 讨论方案，避免做无用功。
- 安全漏洞请不要公开提交 Issue，见 [SECURITY.md](SECURITY.md)。

## 环境准备

```bash
git clone <仓库地址>
cd <项目目录>
cp .env.example .env
# 安装依赖
```

## 分支规范

| 分支 | 用途 |
| --- | --- |
| `main` | 稳定分支，始终保持可发布状态 |
| `dev` | 开发分支，集成各功能分支 |
| `feat/<描述>` | 新功能 |
| `fix/<描述>` | 缺陷修复 |
| `docs/<描述>` | 文档变更 |
| `refactor/<描述>` | 重构 |
| `chore/<描述>` | 杂项 |

从 `dev`（若无则 `main`）切出分支，完成后向 `dev` 提交 PR。

## 提交信息规范

本项目采用 [Conventional Commits](https://www.conventionalcommits.org/zh-hans/) 规范：

```text
<type>(<scope>): <subject>
```

常用类型：

| 类型 | 含义 |
| --- | --- |
| `feat` | 新功能 |
| `fix` | 缺陷修复 |
| `docs` | 仅文档变更 |
| `style` | 不影响代码含义的格式调整 |
| `refactor` | 重构 |
| `perf` | 性能优化 |
| `test` | 测试相关 |
| `build` | 构建系统或依赖变更 |
| `ci` | CI 配置变更 |
| `chore` | 其他杂项 |
| `revert` | 回滚 |

启用提交信息模板：

```bash
git config commit.template .gitmessage
```

## 代码风格

- 缩进、换行、编码以 [.editorconfig](.editorconfig) 为准，请确认编辑器已启用 EditorConfig。
- 换行符统一为 LF，由 [.gitattributes](.gitattributes) 保证。
- 具体语言的格式化与 lint 工具由项目自行配置。

## 提交 PR

1. 确保本地自测通过，新增功能附带测试。
2. 更新受影响的文档与 `CHANGELOG.md`。
3. 按 [PR 模板](.github/PULL_REQUEST_TEMPLATE.md) 填写说明，关联对应 Issue。
4. 保持提交历史清晰，必要时先 rebase 整理。

## 许可证

贡献的代码将按本项目的 [LICENSE](LICENSE) 授权。

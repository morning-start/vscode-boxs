# Modern Python Pack

一个现代化的 Python 开发工具包，集成了 astral-sh 生态系统中的优秀工具，为 VS Code 提供完整的 Python 开发体验。

## 📦 包含的扩展

本扩展包包含以下精心挑选的扩展：

| 扩展                                                                                                     | 功能                                     |
| -------------------------------------------------------------------------------------------------------- | ---------------------------------------- |
| [charliermarsh.ruff](https://marketplace.visualstudio.com/items?itemName=charliermarsh.ruff)             | Ruff - 极速的 Python linter 和 formatter |
| [astral-sh.ty](https://marketplace.visualstudio.com/items?itemName=astral-sh.ty)                         | Ty - Python 类型检查器                   |
| [ms-python.python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)                 | Python 官方扩展                          |
| [ms-python.debugpy](https://marketplace.visualstudio.com/items?itemName=ms-python.debugpy)               | Python 调试器                            |
| [tamasfe.even-better-toml](https://marketplace.visualstudio.com/items?itemName=tamasfe.even-better-toml) | TOML 文件支持                            |
| [morningstart.ruff-helper](https://marketplace.visualstudio.com/items?itemName=morningstart.ruff-helper) | Ruff 辅助工具                            |

## ✨ 主要特性

### 🚀 极速开发体验
- **Ruff**: 用 Rust 编写的超快 Python linter，比传统工具快 10-100 倍
- **Ty**: 现代化的 Python 类型检查器，提供快速而准确的类型检查
- **uv**: 极速的 Python 包管理器和解析器

### 🔧 完整的工具链
- 代码格式化和 lint
- 类型检查
- 调试支持
- TOML 配置文件支持
- 包管理和依赖解析

### 🎯 astral-sh 生态系统
本扩展包专注于 astral-sh 提供的现代化 Python 工具：
- **uv**: 极速的 Python 包管理器和项目管理工具
- **Ruff**: 统一的 Python linter 和 formatter
- **Ty**: 类型检查器

## 📥 安装方法

### 通过 VS Code Marketplace 安装
1. 打开 VS Code
2. 进入扩展视图（`Ctrl+Shift+X`）
3. 搜索 "Modern Python Pack" 或 "astral-sh-py"
4. 点击安装

### 通过命令行安装
```bash
code --install-extension morningstart.astral-sh-py
```

## 🚀 快速开始

### 1. 安装扩展包后
安装完成后，VS Code 会自动安装所有包含的扩展。

### 2. 配置 Python 环境
```bash
# 使用 uv 创建新的 Python 项目
uv init my-project
cd my-project

# 安装依赖
uv add requests
```

### 3. 配置 Ruff
在项目根目录创建 `ruff.toml` 或 `pyproject.toml`：

```toml
[tool.ruff]
line-length = 88
target-version = "py311"

[tool.ruff.lint]
select = ["E", "F", "I", "N", "W"]
```

### 4. 配置 Ty
在 `pyproject.toml` 中添加：

```toml
[tool.ty]
target-version = "py311"
```

## 📖 使用指南

### Ruff 使用
Ruff 会自动在保存时格式化代码并检查问题。常用快捷键：
- `Ctrl+S` (Windows/Linux) 或 `Cmd+S` (Mac): 保存时自动格式化
- `Ctrl+Shift+P` -> "Ruff: Format Document": 手动格式化

### Ty 使用
Ty 会在编辑时提供实时的类型检查反馈：
- 类型错误会在编辑器中显示红色波浪线
- 鼠标悬停可查看详细的类型信息

### uv 使用
在终端中使用 uv 管理项目：
```bash
# 创建新项目
uv init project-name

# 添加依赖
uv add package-name

# 运行脚本
uv run python script.py

# 更新依赖
uv lock --upgrade
```

## 🛠️ 配置建议

### VS Code 设置 (settings.json)
```json
{
  "[python]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "charliermarsh.ruff",
    "editor.codeActionsOnSave": {
      "source.fixAll.ruff": "explicit",
      "source.organizeImports.ruff": "explicit"
    }
  },
  "ruff.lint.enable": true,
  "ruff.format.enable": true,
  "ty.enable": true
}
```

### 推荐的项目结构
```
my-project/
├── pyproject.toml
├── ruff.toml
├── src/
│   └── my_package/
│       └── __init__.py
├── tests/
│   └── test_example.py
└── uv.lock
```

## 🔄 更新日志

查看 [CHANGELOG.md](./CHANGELOG.md) 了解详细的更新记录。

## 🤝 贡献

欢迎贡献！请通过以下方式参与：

1. Fork 本项目
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

## 📄 许可证

本项目采用 [LICENSE](./LICENSE) 许可证。

## 🔗 相关链接

- [VS Code 扩展市场](https://marketplace.visualstudio.com/items?itemName=morningstart.astral-sh-py)
- [GitHub 仓库](https://github.com/morning-start/vscode-boxs/tree/main/astral-sh-py)
- [uv 文档](https://github.com/astral-sh/uv)
- [Ruff 文档](https://docs.astral.sh/ruff/)
- [Ty 文档](https://github.com/astral-sh/ty)

## 💡 常见问题

### Q: 为什么选择 astral-sh 的工具？
A: astral-sh 的工具都是用 Rust 编写的，具有极高的性能和现代化的设计理念，能够显著提升 Python 开发效率。

### Q: 本扩展包与单独安装各扩展有什么区别？
A: 本扩展包提供了一站式安装和配置，确保所有工具协同工作，避免配置冲突，并提供统一的开发体验。

### Q: 如何报告问题？
A: 请在 [GitHub Issues](https://github.com/morning-start/vscode-boxs/issues) 中报告问题。

## 📞 支持

如有问题或建议，请通过以下方式联系：
- 提交 [GitHub Issue](https://github.com/morning-start/vscode-boxs/issues)
- 发送邮件至项目维护者

---

**享受高效的 Python 开发体验！** 🎉

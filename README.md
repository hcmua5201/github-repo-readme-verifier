# GitHub 仓库 README 规范化验证项目

本项目旨在提供一个自动化的工具，用于验证 GitHub 仓库中 README 文件的规范化程度。

## 项目简介

README 文件是项目的门面，一个规范、完整的 README 对于项目的协作和维护至关重要。此脚本通过一系列预定义的规则，自动检查 README 文件是否满足基本要求。

## 使用方法

1.  **准备工作**:
    *   在本地创建一个 `.env` 文件，并填入您的 `GITHUB_TOKEN` 和 `GITHUB_ORG`。
    *   确保您已安装 Python 3.8+ 和所需的依赖包 (`pip install requests python-dotenv pyyaml`)。
2.  **运行验证**:
    *   将 `readme_verifier.py` 脚本下载到本地。
    *   在脚本所在目录打开终端，执行 `python readme_verifier.py`。
    *   脚本会自动从本仓库的 `main` 分支拉取 `readme_verify_config.yaml` 配置文件，并据此验证本仓库的 `README.md`。

## 验证规则说明

验证规则由仓库根目录下的 `readme_verify_config.yaml` 文件定义，主要包括：

-   **必填章节**: 检查 README 是否包含所有指定的标题。
-   **必需徽章**: 检查 README 是否包含所有指定的 Shields.io 徽章。
-   **内部链接**: 检查指向仓库内部文件的链接是否有效。
-   **外部链接**: 检查指向外部网站的链接是否可访问。
-   **内容合规**: 检查内容是否包含禁止的关键词（例如，用于标记待办或修复的词汇）。

---

**项目徽章：**

![License](https://img.shields.io/badge/license-MIT-green)
![Python Version](https://img.shields.io/badge/python-3.8+-blue.svg)

**相关链接：**

- [API 文档](docs/API.md)
- [贡献指南](CONTRIBUTING.md)
- [GitHub](https://github.com)
- [Python 官网](https://www.python.org)

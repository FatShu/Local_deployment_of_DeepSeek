# Ollama 文件分析工具

这是一个使用 Ollama API 分析多种文件类型的工具，可以处理 txt、xlsx、docx、doc、pptx 和 ppt 文件。

## 功能特点

- 交互式文件分析
- 支持多种文件格式
- 实时显示模型思考过程
- 动态配置 Ollama 服务端口
- 完整的错误处理和提示

## 安装步骤

1. 确保已安装 Python 3.8+
2. 安装 Poetry 包管理器：
   ```bash
   pip install poetry
   ```
3. 克隆本仓库：
   ```bash
   git clone https://github.com/yourusername/ollama-file-analysis.git
   cd ollama-file-analysis
   ```
4. 安装项目依赖：
   ```bash
   poetry install
   ```

## 使用方法

1. 启动 Ollama 服务：
   ```bash
   ollama serve
   ```
2. 激活 Poetry 虚拟环境：
   ```bash
   poetry shell
   ```
3. 运行程序：
   ```bash
   python -m ollama_file_analysis.main
   ```
4. 按照提示操作：
   - 程序会扫描 Database 文件夹中的文件
   - 对每个文件，你可以指定分析类型（总结、提取要点等）
   - 分析结果会实时显示

## 项目结构
ollama-file-analysis/
├── pyproject.toml         # Poetry配置文件
├── README.md              # 项目说明文档
├── src/
│   └── ollama_file_analysis/
│       └── __init__.py    # 包初始化文件
│       └── main.py        # 主程序文件
└── .gitignore             # Git忽略文件
## 贡献

如果你发现任何问题或有改进建议，请提交 Issue 或 Pull Request。

## 许可证

本项目采用 MIT 许可证。
    
# DeepSeek本地部署及应用
支持txt、xlsx、docx、doc、pptx、ppt格式内容识别并执行操作
## 功能特点
- 交互式文件分析
- 支持多种文件格式
- 实时显示模型思考过程
- 动态配置Ollama服务端口
- 完整的错误处理和提示
## 安装前准备
1. 确保已安装 Python 3.8+
2. 安装 Poetry 包管理器：
   ```bash
   pip install poetry
   ```
3. 克隆本仓库：
   ```bash
   git clone https://github.com/FatShu/Local_deployment_of_DeepSeek
   ```
4. 安装项目依赖：
   ```bash
   poetry install
   ```
### 安装ollama
访问ollama官网<br>
```bash
https://ollama.com/
```
选择对应自己系统的版本下载<br>
下载完成后可在命令提示符中输入ollama查看是否安装成功<br>
##### 修改Ollama安装目录
ollama默认安装在C:\Program Files\Ollama下<br>
可以通过用管理员身份打开命令提示符（CMD）输入
```bash
路径\0llamaSetUp.exe /DIR="需要安装的路径"
```
### 安装AI大模型
在Ollama官网中选择需要的模型后<br>
打开命令提示符输入ollama run 模型名进行使用，如果模型未安装会自动进行下载<br>
例如：
```bash
ollama run deepseek-r1:32b
```
推荐16G显存可以下载32b的版本，小显存的建议1.5b版本，7b版本需要6G左右的显存<br>
安装完成后可以用ollama list查看已下载的模型<br>
##### 修改模型安装位置
模型默认安装在C:\Users\用户名\.ollama\models下<br>
需要新建环境变量，变量名为OLLAMA_MODELS，变量值为需要存储的路径，例如D:\Ollama\models<br>

至此，你的电脑上就已经能够运行AI大模型了<br>
## 运行准备
查看ollama是否运行，输入ollama serve可以查看，ollama默认监听11434端口<br>
如果需要修改监听端口，新建环境变量，变量名为OLLAMA_PORT，变量值为需要监听的端口<br>
需要安装的python包有openpyxl python-docx textract pandas ollama six<br>
输入
```bash
pip install openpyxl python-docx textract pandas ollama six
```
即可进行安装<br>
安装完成后就可以运行Python代码使用AI了，如果你发现任何问题或有改进建议，请提交Issue或Pull Request。<br>

## 项目结构
ollama-file-analysis/<br>
├── pyproject.toml         # Poetry配置文件<br>
├── README.md              # 项目说明文档<br>
├── src/<br>
│   └── ollama_file_analysis/<br>
│       └── __init__.py    # 包初始化文件<br>
│       └── main.py        # 主程序文件<br>
└── .gitignore             # Git忽略文件<br>

## 许可证
本项目采用 MIT 许可证。
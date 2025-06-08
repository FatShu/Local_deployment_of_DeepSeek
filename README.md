# DeepSeek本地部署及应用
安装前准备
-
### 安装ollama
访问ollama官网https://ollama.com/，选择对应自己系统的版本下载
下载完成后可在命令提示符中输入ollama查看是否安装成功
#### 修改Ollama安装目录
ollama默认安装在C:\Program Files\Ollama下
可以通过用管理员身份打开命令提示符（CMD）输入 路径\0llamaSetUp.exe /DIR="需要安装的路径"
### 安装AI大模型
在Ollama官网中选择需要的模型后
打开命令提示符输入ollama run 模型名进行使用，如果模型未安装会自动进行下载
例如：ollama run deepseek-r1:32b
安装完成后可以用ollama list查看已下载的模型
#### 修改模型安装位置
模型默认安装在C:\Users\用户名\.ollama\models下
需要新建系统变量，变量名为OLLAMA_MODELS，变量值为需要存储的路径，例如D:\Ollama\models

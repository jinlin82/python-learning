# python-learning
## 环境配置(Windows系统)
1. 下载安装 Anaconda，网址：
   https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/Anaconda3-2019.10-Windows-x86_64.exe
   - 安装过程中注意要选择添加到Path中选项.
   - 安装在根目录下面，如 C:\Anaconda3 或 D:\Anaconda3 等.
2. 使用 Vscode 作为编程工具
   - 下载地址：链接：https://pan.baidu.com/s/1qf3rmdqk3COdGPA7D312PA 提取码： 5fq3
   - 解压到某文件夹（路径中不要出现中文，空格等）里面，运行里面的 code.exe 即可，
     如：C:\Worktools\VSCode-win32-x64-1.42.0\Code.exe
   - 添加右键快捷键: 记事本打开 `python-learning` 项目中(先使用下面方法克隆项目)的 `vsCode_addright.reg` 文件，把其中的
     `C:\\Worktools\\VSCode-win32-x64-1.42.0\\Code.exe` 全部替换为自己
     `Code.exe` 的位置（注意要用双斜杠），保存后双击运行`vsCode_addright.reg` 文件.
3. 安装并配置 git
   - 下载地址：链接：https://pan.baidu.com/s/1E2Z0cijp1x2PIxqn7oVn9A 提取码： qi9o
   - 解压到某文件夹（路径中不要出现中文，空格等）里面, 如 `C:\Worktools\git`
   - 设置 `PATH` 环境变量，增加如 `C:\Worktools\git\bin`,方法：
	 + 在解压后的 `git\bin` 文件夹里面，按住 shift 键， 右键点击空白处，选择 "`在此处打开命令`"
	 + 在打开的cmd窗口中输入(一行一行输入并运行）（注：如果打开的是 `Powershell`，
       先运行 `cmd` 命令，再一条一条运行以下语句）
```
for /f "usebackq tokens=2,*" %A in (`reg query HKCU\Environment /v PATH`) do set my_user_path=%B
setx PATH "%cd%;%my_user_path%"
```
   4. 配置 `.gitconfig`, 按下快捷键 `win+R` ，在弹出的窗口中输入 `CMD`，之后在弹出
      的窗口中输入：
```
git config --global user.email "jinlin82@qq.com"
git config --global user.name "Jin Lin"
```
（注：引号里改为**自己的邮箱和名字，名字用汉语拼音写**）

   5. 验证有没有配置好： 按下快捷键 `win+R` ，在弹出的窗口中输入 `CMD`，之后在弹出
      的窗口中输入： `git` 没有运行错误即表示安装好

## git 基本使用方法

### 如何克隆此项目中所有内容

1. 进入要拷贝到的目标文件夹
2. 按住 shift 键， 右键点击空白处，选择 "`在此处打开命令`"
3. 在打开的cmd窗口中输入 `git clone
   https://github.com/jinlin82/python-learning`, 等待完成即可.

### 如何更新项目中的内容
1. 方法 1:
   - 进入克隆后项目文件夹， 按住 shift 键， 右键点击空白处，选择 "`在此处打开命
     令`"
   - 在打开的cmd窗口中输入 `git pull`
2. 方法 2: 使用 vscode 的 git 功能

## Vscode 使用方法


### 如何使用 Vscode 打开项目
1. 可以右键点击该项目所在的文件夹，选择用“Open Folder as VS Code Project”打开；
2. 也可以先打开VSCode-win32-x64-1.42.0文件夹里面的code.exe,点击“文件”——“将文件夹添加到工作区”，然后选择要打开的项目即可（Vscode为中文版本情况下）。
   
### 如何使用 Vscode 打开和运行 python程序文件（.py 文件），jupyter notebook 文件 （.ipynb) 文件
1. 打开和运行 python程序文件（.py 文件）
   - 右键点击python程序文件（.py文件），选择'Open Folder as VS Code Project'打开,或者直接在Vscode打开的项目里点击.py文件
   - 光标放在代码所在行或者选中需要运行的代码，按‘Ctrl+Enter’或‘shift+enter’快捷键即可运行。
2. 打开和运行jupyter notebook 文件 （.ipynb) 文件
   - 右键点击jupyter notebook程序文件（.ipynb文件），选择'Open Folder as VS Code Project'打开,或者直接在Vscode打开的项目里点击.ipynb文件
   - 运行.ipynb文件,按‘Ctrl+Enter’或‘shift+enter’快捷键可以逐行的运行代码；运行单个代码块，直接点击该代码块左上方的三角符号图标运行;运行整个.ipynb文件，点击最上面左边的两个三角形组成的图标运行。




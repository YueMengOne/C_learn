# C 语言笔记
## 一、C 语言概述 | 环境配置

### 1.1 C 语言的应用领域

1. 操作系统的开发
2. 驱动开发
3. 数据库开发
4. 嵌入式开发
5. 游戏开发

### 1.2 C 语言常用开发环境

1. **VC++ 6.0  **(**过时**)
2. **Visual Studio**  (适合商业项目、**不适合初学者**)
3. **Clion**  (适合商业项目、**不适合初学者**)
4. **Dev C++**  (体积小、**代码补齐一般**。不适合商业项目，**适合初学者**)
5. Vim  (linux程序员必须。有一定难度，**不适合初学者**)
6. VS Code  (体积小，**商业初学者都适合**)

### 1.3 VS Code 环境配置

1. **下载 VS Code**

2. **安装 VS Code**

3. **安装中文插件**

4. **安装 Mingw64 编译器**

   > MinGW64 文件：[点击跳转](files/x86_64-14.2.0-release-posix-seh-ucrt-rt_v12-rev1.7z)

5. **放置 mingw64 文件**

   > 1. C 盘新建一个 Dev 文件夹
   > 2. 将解压后的 mingw64 文件 放置到 Dev 文件夹中

6. **设置环境变量**

    - Windows 11

      > 1. 复制 mingw64/bin 文件夹所在的文件夹链接
      > 2. 设置 > 系统 > 系统信息 > 高级系统设置 > 环境变量
      > 3. 找到**系统变量**中的 Path 双击
      > 4. 新建 > 粘贴文件路径 > 确定

7. **安装 C/C++ 插件**

8. <a id="section1">**安装 Code Runner 插件**</a>

   > 安装完成后，点击**设置**按钮
   >
   > 选中 `Code-runner:Run In Terminal` （运行在内部的终端）
   >
   > 选中`Code-runner:Save File Before Run` （保存文件再运行）

9. **编辑 C 代码并运行程序**

### 1.4 VS Code 常用配置

1. **文件编辑器设置字体大小**

   > 文件 > 首选项 > 设置 > `Editor:Font Size` > 18

2. **终端设置字体大小**

   > 文件 > 首选项 > 设置 > 功能 > 终端 > `Integrated:Font Size` > 18

3. **显示终端和隐藏终端**

   > Ctrl + ~

4. **运行前自动保存文件**

   > 已设置，参考 [安装 Code Runner 插件](#section1)

5. **将 Power Shell 改为 UTF-8 编码**（解决终端输出中文乱码）

   > 1. 管理员运行 Power Shell
   > 2. 执行 `New-Item $PROFILE  -ItemType File -Force`
   > 3. 执行成功后到 `Documents\WindowsPowerShell` 文件夹
   > 4. 编辑 `Microsoft.PowerShell_profile` 文件
   > 5. 文件中添加 `$OutputEncoding = [console]::InputEncoding = [console]::OutputEncoding = New-Object System.Text.UTF8Encoding` (输出编码 = 系统文本UTF-8编码)
   > 6. 右击 `Microsoft.PowerShell_profile` 文件 > 使用 Power Shell 运行
   > 7. Power Shell 管理员模式运行 `Set-ExecutionPolicy Unrestricted`
   > 8. 在 Power Shell 运行 `chcp` 检查输出结果是否为 65001

6. **不产生 tempCodeRunnerFiile.c**

   > 文件 > 首选项 > 设置 > 扩展 > `Run Code configuration` > `code-runner.ignoreSelection` > 选中 `ignore Selection` (忽略选择)

## 二、初识 C 语言

### 1. main 函数

**主函数**，程序的入口。所有程序都是从 main 函数开始执行的

```c
// main 函数程序
int main()
{
	return 0;
}
```

###  2. printf 和 库函数

### 3. 关键字

### 4. 字符和 ASCII 编码

### 5. 字符串和 \0


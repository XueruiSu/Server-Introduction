# Server-Introduction

服务器的使用可以分为两类：服务器的管理和基于服务器进行代码开发。前者有很多对应的软件可以使用，大家根据自己的习惯进行选择，如MobaXterm，XShell等，后者推荐大家使用VScode进行远程代码开发。

使用 VS Code 远程连接 Linux 服务器进行代码开发有两大优势：1. 更快的代码编辑和调试：通过远程连接，您可以在本地使用 VS Code，但是实际上您的代码是在远程服务器上运行的。这可以带来更快的代码编辑和调试速度，因为代码的执行是在远程服务器上进行的。2. 更高的可扩展性：通过远程连接，您可以轻松地扩展您的代码开发环境。您可以使用远程服务器上的更多资源，例如计算能力、存储空间等等，这可以让您更好地满足不同的开发需求。

## 一、可选用的远程终端管理工具：
MobaXterm、XShell、PuTTY、SecureCRT、Termius、iTerm2、Webmin...

下面提供MobaXterm的简要教程：

### 1. 下载和安装：从 MobaXterm 官网下载适合您的操作系统的版本，并按照安装向导进行安装。安装完成后，启动 MobaXterm。

### 2. 连接到远程服务器：在 MobaXterm 的主界面中，点击 "Session" 按钮，选择您要连接的协议（如 SSH、Telnet、FTP 等），并输入服务器 IP 地址和端口号，然后点击 "OK"。

### 3. 登录到远程服务器：在连接成功后，输入您的用户名和密码，然后点击 "OK"。如果您使用 SSH 协议连接，MobaXterm 还会提示您接受服务器的公钥。

### 4. 使用远程终端：连接成功后，您可以在 MobaXterm 的主界面中看到一个终端窗口，这是连接到远程服务器的终端。您可以在终端中输入命令执行操作，就像在本地终端一样。

### 5. 传输文件：MobaXterm 的界面还提供了一个文件传输窗口，可以让您在本地和远程服务器之间传输文件。您可以通过拖放文件到窗口中或使用传统的文件浏览器来传输文件。

### 6. 使用 X11 转发：如果您需要在远程服务器上打开 GUI 应用程序，可以使用 MobaXterm 的 X11 转发功能。首先，确保您在连接到远程服务器时启用了 X11 转发选项。连接后，在远程终端中输入命令打开 GUI 应用程序，它将在本地计算机上显示。

这是一个简要的 MobaXterm 使用教程，其中包含了连接到远程服务器、使用终端、传输文件和使用 X11 转发等基本功能。MobaXterm 还提供了许多其他功能，例如集成了常用的网络工具、支持多个会话、支持多种协议等等。如需了解更多详细信息，请查看 MobaXterm 的官方文档。

## 二、下面是连接 Linux 服务器的 VS Code 远程工作流程：
### 1. 在 Linux 服务器上安装 SSH（这一步已经帮你完成，即服务器已经安装好SSH）
确保您的 Linux 服务器上安装了 SSH。如果您使用的是 Ubuntu 或 Debian 等基于 apt 的发行版，则可以使用以下命令安装 SSH：

sudo apt-get update

sudo apt-get install openssh-server
### 2. 在 VS Code 中安装 Remote Development 扩展
在 VS Code 中搜索并安装 Remote Development 扩展。扩展名称为 "Remote Development"，由 Microsoft 提供。
### 3. 连接到 Linux 服务器
在 VS Code 中，按下 Ctrl + Shift + P（或 Cmd + Shift + P）打开命令面板，然后输入 "Remote-SSH: Connect to Host"。选择此选项后，将出现一个输入框，您需要在其中输入 Linux 服务器的 SSH 地址。

例如：

ssh xuerui@211.71.74.225

其中，"xuerui" 是您在 Linux 服务器上的用户名，"211.71.74.225" 是服务器的 IP 地址。确保您使用的是您的实际用户名和 IP 地址。
### 4. 输入密码并连接
连接到 Linux 服务器之后，您需要输入密码以验证您的身份。验证成功后，您将在 VS Code 中看到一个新的窗口，其中包含 Linux 服务器的文件系统。现在，您可以在 VS Code 中使用终端和文件编辑器与服务器进行交互。

## 三、辅助教程：
#### 校园网登录的问题解决办法（denoted by Chongchong Li）： https://github.com/XueruiSu/Login-out-Campus-Network.git
#### SSH免密登录教程（denoted by Xuerui Su）： https://github.com/XueruiSu/SSH-login-without-password.git
#### 使用tmux工具把程序挂载至后台教程（denoted by Xuerui Su）： https://github.com/XueruiSu/Tmux-tutorial.git

## 四、八卡服务器参数
![f0f6e30a690d23a85bd49a039b137ca](https://github.com/XueruiSu/Server-Introduction/assets/77718956/9ee10db4-12e4-4eef-9558-9a0c995a55d5)
![77544a1ff47ce3d0064122245fca330](https://github.com/XueruiSu/Server-Introduction/assets/77718956/0e1aa02b-e1cd-4d8b-879f-98696e0e979b)
![30def63dcb95145e15e7ecef1d7c6b2](https://github.com/XueruiSu/Server-Introduction/assets/77718956/4fd5e786-8f0e-4273-b157-ea7544252179)
![df38cb549b61874a35faefd0f6d526c](https://github.com/XueruiSu/Server-Introduction/assets/77718956/50f96a3b-4919-4369-b1b5-67907dbbaca8)



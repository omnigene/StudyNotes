## Git配置


- 查看配置：

  ```bash
  # 查看全部配置列表
  git config --list
  # 查看某项配置，<name>表示配置名称
  git config <name>
  ```

- 在配置文件中删除某项配置：

  ```bash
  # <name>表示某项配置的名称
  git config --global --unset <name>
  ```
  
- 设置默认文本编辑器：

  ```bash
  # <name>表示文本编辑器的名称，通常需要加引号
  git config --global core.editor <name>
  # 示例1：将Visual Studio Code设置为默认文本编辑器
  git config --global core.editor "code --wait"
  # 示例2：将Notepad++设置为默认文本编辑器
  git config --global core.editor "'C:/Program Files/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"
  ```
  
- 设置密码管理工具（Git Credential Manager for Windows）：

  ```bash
  # 配置密码管理工具，初次使用无需配置，默认调用Credential Manager管理账号密码
  git config --global credential.helper manager
  # 解除使用密码管理工具，解除后每次进行push等操作时都会要求输入GitHub账号密码
  git credential-manager uninstall
  ```

  - 在不解除密码管理工具的情况下切换Git用户，可通过Windows凭据管理器（搜索“管理网络密码“）删除GitHub凭据

  ![Windows凭据管理器](https://github.com/omnigene/StudyNotes/blob/master/Git/imgs/Windows凭据管理器.png?raw=true)

  - 删除凭据后，首次进行push等操作时，会弹出GitHub登录页面，一次登录后会储存新的凭据，无需再每次输入账号密码

  ![GitHub-Login](https://github.com/omnigene/StudyNotes/blob/master/Git/imgs/GitHub-Login.png?raw=true)



## Git基本操作

- 一次添加所有修改：

  ```bash
  git add .
  ```

- 添加及查看远程仓库：

  ```bash
  # <name>用于设置远程仓库在本地的名称，默认为origin
  # <url>用于设置需连接的github远程仓库地址，例：https://github.com/omnigene/StudyNotes
  git remote add <name> <url>
  # 查看远程仓库地址
  git remote -v
  ```

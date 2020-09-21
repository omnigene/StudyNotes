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
  # 清除密码管理工具中储存的凭证，清除后再进行push等操作时会要求输入GitHub账号密码
  git credential-manager uninstall
  ```

## Git基本操作

- 添加远程仓库：

  ```bash
  # <name>用于设置远程仓库在本地的名称，默认为origin
  # <url>用于设置需连接的github远程仓库地址，例：https://github.com/omnigene/StudyNotes
  git remote add <name> <url>
  ```

  
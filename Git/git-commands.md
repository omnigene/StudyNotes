## Git配置


- 查看配置列表：

  ```bash
  git config --list
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
  # 配置密码管理工具
  git config --global credential.helper manager
  # 卸载密码管理工具
  git crendential-manager uninstall
  ```



## Git基本操作

- 添加远程仓库：

  ```bash
  # <name>用于设置远程仓库在本地的名称，默认为origin
  # <url>用于设置需连接的github远程仓库地址，例：https://github.com/omnigene/StudyNotes
  git remote add <name> <url>
  ```

  
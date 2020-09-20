- 清除缓存在git中的用户名和密码：`git credential-manager uninstall`

- 添加远程仓库：

  ```bash
  # <name>用于设置远程仓库在本地的名称，默认为origin
  # <url>用于设置需连接的github远程仓库地址，例：https://github.com/omnigene/StudyNotes
  git remote add <name> <url>
  ````


- 查看配置列表：`git config --list`

- 设置默认文本编辑器：

  ```bash
  # <name>表示文本编辑器的名称，通常需要加引号
  git config --global core.editor <name>
  # 将默认文本编辑器设置为Visual Studio Code
  git config --global core.editor "code --wait"
  ```

  


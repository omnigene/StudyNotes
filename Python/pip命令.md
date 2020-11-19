## pip

```bash
# 查看已安装的包
pip list
# 检查需要更新的包
pip list --outdated
# 安装包
pip install <name>
# 升级包
pip install --upgrade <name>
# 强制重新安装包（解决无法升级包的问题）
pip install -U --force-reinstall <name>
# 生成项目依赖包列表文件
pip freeze>requirements.txt
```


# 1.1.常用配置

## 用户信息

1.查看配置信息

```bash
git config --list
```

2.常用配置

```bash
# 配置用户信息
git config --global user.name "jiuchou"
git config --global user.email "jiuchou@example.com"
# 记住用户密码
git config --global credential.helper store
# 配置ssh-keygen
# 生成秘钥文件，将~/.ssh/id_rsa.pub文件中内容保存到GitHub账号设置下的SSH keys中
ssh-keygen -t rsa -C "jiuchou@example.com"
```


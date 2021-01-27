# 设置身份验证

当从Git发起连接至GitHub时，需要通过HTTPS或者SSH进行身份验证。

{% hint style="info" %}
一般用SSH
{% endhint %}

## 生成SSH密钥

打开 Git Bash

```bash
$ ssh-keygen -t ed25519 -C "luanshixiao@gmail.com"
> Generating public/private ed25519 key pair.
> Enter a file in which to save the key (/c/Users/you/.ssh/id_ed25519):[Press enter]
```

密钥保存在默认位置，回车。

```bash
> Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again]
```

方便起见，不设置密码，连续两次回车。

## 将SSH公钥添加至GitHub

复制公钥

```bash
$ clip < ~/.ssh/id_ed25519.pub
```

在GitHub账户设置中的`SSH and GPG keys` `New SSH key`

将公钥粘贴至 `Key` 中

`Add SSH key`


# ssh clone

這裡記錄下使用 SSH, Git `clone` 的一些常用錯誤!

## ❓ 錯誤: Permission denied (publickey)

表示 SSH 沒有授權到:

1. 沒有把 public key 丟到你的 hosting service (GitHub, GitLab, etc)
2. `ssh-add -l` 沒有你的 ssh key

```sh
# 啟動 ssh-agent
$ ssh-agent bash

# 加入金鑰
$ ssh-add /path/to/your/ssh/key
```

備註: 這個方法只會在原本的 instance 有效. 在關閉過後就會失效. 所以每次都必須要重新用一次!

原網址: https://blog.csdn.net/qq_37866436/article/details/109456501

## ❓ 錯誤: Bad file descriptor

表示 ssh 無法讀入你的金鑰. 看看你的 `~/.gitconfig` 是否有指定 `ssh` 的軟體.

```
[core]
	sshCommand = 'C:\\Windows\\System32\\OpenSSH\\ssh.exe'
```

如果你使用 Git Bash, 那上面就是**錯誤**的. Git Bash 是自成一個 Linux 環境. 所以你只能使用 Linux's 底下的 ssh.
不過 Git Bash 本身就自帶 ssh 軟件. 所以**直接移除**這個設定即可!

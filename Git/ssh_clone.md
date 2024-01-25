# ssh clone

如果你在 `clone` 的時候遇到:

```
Permission denied (publickey)
```

試試以下方法:

```sh
$ ssh-agent bash
$ ssh-add /path/to/your/ssh/key
```

原網址: https://blog.csdn.net/qq_37866436/article/details/109456501

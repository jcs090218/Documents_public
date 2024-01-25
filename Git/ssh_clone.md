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

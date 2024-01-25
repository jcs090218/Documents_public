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

備註: 這個方法只會在原本的 instance 有效. 在關閉過後就會失效. 所以每次都必須要重新用一次!

原網址: https://blog.csdn.net/qq_37866436/article/details/109456501

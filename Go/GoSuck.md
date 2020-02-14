# Go Suck

This is the document if you FEEL hate from Go. Welcome you to complain about
this here.

這是個文檔當你對Go感受到恨意的時候, 歡迎你對這個文檔發洩一下你的情緒.

## 1. Docstring

Most of the languages use `/*` for their docstring yet Go use `//`.

大部分的語言都使用`/*`當做`doc`, 不過Go反其道而行使用`//`. (可惡)

Why not this? 為什不用這個?

```go
/**
 * Description over here.
 *
 * @param ... : ...
 * @return ...
 */
```

Use this? 用這個?

```go
// Description over here.
// @param ... : ...
// @return ...
```

## 2. Environment (環境)

Most programming languages are design under global automated environment variables
settings. Go designed that you would only allow to work under `GOPATH`, which
limited it usage and inconvenience.

大部分語言都是自動下全域的環境設置. Go還設置了你必須在`GOPATH`底下才能引進
專案的道理!

Now all functions have to go through `GOPATH`. (I started missing Java's environment)

所有內部函式必須通過`GOPATH`. (我已經開始懷念Java的環境設置了)

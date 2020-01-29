# Coding Standard

這裡先簡單紀錄一下大至的程式碼規範. 之後有要再細分在修改. :D


## 通用規範

1. 不要有無意義的空行.
2. 一律要有標頭檔案.
3. 任何可能有不清楚的`函式`和`變數`一律要註解.
4. [存取範圍層級](https://docs.microsoft.com/zh-tw/dotnet/csharp/language-reference/keywords/accessibility-levels)
一律要標示. (如果有)
5. 一律使用Space空格.
6. 每一行不超過80字母,超過一律斷行`\n`.
7. 全部`變數`一律都要有初始值. (如果可以)

*P.S. 之後Code Review會有更詳細的要求,規範總不會是完美的!~*

### 標頭檔注意事項

標頭檔可以自己設計, 只要有包含以下幾項紀錄即可.

- [ ] 檔案名稱
- [ ] 創建檔案的人名
- [ ] 創檔日期

例子:
```
# ========================================================================
# $File: SomeFile.txt $
# $Date: 2019-09-17 15:59:41 $
# $Revision: $
# $Creator: Jen-Chieh Shen $
# $Notice: See LICENSE.txt for modification and distribution information
#                   Copyright © 2019 by Shen, Jen-Chieh $
# ========================================================================
```


## 個語言規範

* [Unity C#](.unity_csharp.md)
* [C#](./csharp.md)
* [TypeScript](./typescript.md)
* [JavaScript](./javascript.md)

# Huge Issues (巨大的困難)
> 這裡記錄著這個專案的大大小小的困難.

這裡我主要先把問題分成下列兩大類.

  * 引擎理解與使用
  * 程式規範, 語言的理解

引擎使用的部分我打算先撇開, 下次一起補齊.

## 程式規範, 語言的理解

我看了幾個程式碼檔案. 裡面並沒有所謂的Coding Convention之類的東西.
沒有標頭, 沒有註解(合理的, 只有少數有做). 充滿著"魔術數字". 這些
都算是問題較小的程式問題. 只要有良好的習慣自然而然就能做好. 重要
必須先有一份Coding Standard, 不然維護性很難提升.

這裡有一份TypeScript的Coding Standard, 僅供參考.

* https://github.com/Platypi/style_typescript

懶的話, 可以使用Linter! :P

可以參考我寫的, [Code Coverage 維護性](./code_coverage.md).

### 過度的使用Lambda

程式碼裡面使用的過多的Lambda, 也就是所謂的function pointer.
在沒有程式規範的情況下, 我無法得知哪些是外部呼叫, 哪些是內部呼叫.
我只能默認所有程式碼都是外部呼叫. 也就是說要是我有O(n)要處理的`變數`.
每增加一個`變數`我就得要多關心一個`變數`的使用和變化. 在協同的情況下
是非常可怕的. 別人亂改你的程式碼的`變數`都會變得非常難查找; Debug的時間
就會是O(n). 如果有public或private支持起碼可以得到減少O(public) - O(private).
雖然還是O(n), 但起碼數量減少了.

*這裡不懂, 我事後再補範例解釋!*

### EventCenter 自由的代價

Event Center是介面面的事件呼叫實作機制. 底層使用簡易的`key, value`
的想法很創新. 也確實做到了`decoupling`和`自由性`. 同時也帶來查找上的困難.
加上同id可以被註冊的情況下事件管理將非常難以管理(跟public/private的原因一樣).
好一點的情況就是分一個`global`/`local`, 不然就是依照module辦事.
例如Network -> EventCenter. Game -> EventCenter. 這樣會比較清楚.

並提供一些必要函式搭配使用, 可以用來debug. 例如:

1. clean - 清除所有事件, 當事件不對稱的時候可以判斷.
2. show - 列出所有目前註冊的事件清單.

改進就是當override key的時候要列出來跟使用者說, 不要默認.

### Defense Programming (防禦式程式編碼)

每當一個程式碼可能出錯的時候使用`return`, 請一併告知使用者為何哪裡出錯?
不要默認. 傻傻地盯著電腦不傻嗎? :sweat:

### Release和Debug旗子

目前沒看到, 先記錄著.

### 過多的dot, dot, dot

這是我隨便截的一段程式碼, 這裡面有兩個`.`. 以人類行為學裡, 過多的下一個
代辦事項是不直觀的.

:x: Bad

```ts
node.getChildByName("new_s").active = true;  // 我們得到news設成true.
```

:heavy_check_mark: Good

```ts
let news : cc.Node = node.getChildByName("new_s");  // 我們得到news,
news.active = true;                                 // news被設成true了!
```

*以上例子短, 可能不夠明顯. 越來越多會越來越明顯.*

### 節點掌握

一樣是這一段代碼, 我們卻無法設置`中斷點`. 因為我不會知道哪個環節出錯了!
`TypeScript`/`JavaScript`可能沒這問題. 因為Browser的DevTool和VSCode越來越
強了... 不過一樣禁止比較好.

```
// 如果這裡有錯誤, 
// 我們不會知道node, getChildByName, active, 哪個是null.
node.getChildByName("new_s").active = true;
```

### 不超過80個字元

這個有越來越短的趨勢, 上網查查看吧! :joy:

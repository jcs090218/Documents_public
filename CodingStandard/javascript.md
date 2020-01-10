# JavaScript
> JavaScript的程式規範


* 創檔者: Shen, Jen-Chieh
* 註解: 這裡寫著JavaScript的一些程式規範.


## 檔案相關 (File Related)

* Tab or Space: `SPC`
* Tab Width: `2`


## 文件命名 (File Naming)

一律小寫,使用`-`當空格.

:heavy_check_mark: Good
```js
gameobject.js
game-object.js
```

:x: Bad
```js
gameObject.js
GameObject.js
```

## 註解 (Commenting)

* 基本上應該會跟Facebook代碼規範一樣.


### 函式

幾個重要的關鍵字.

* `@desc` - 函式功能標記.
* `@param` - 函式變量標記.
* `@return` - 回傳標記.
* `@attention` - 注意標記.
* `@source` - 來源標記.

範例如下.
```js
/**
 * @desc Load the animation by file path.
 * @source https://www.google.com/
 * @attention Important notice typed here...
 *
 * @param { string } prefixName Prefix name of the animation targeting.
 * @return { Animation } Loaded animation object.
 */
public function loadAnimation(prefixName) { }
```

### 變數

* 沒有特別規則, 乾淨就好.


## 變數命名 (Variable Naming)

### 全域變數 (Globla Variable)

一律大寫加底線.

:heavy_check_mark: Good

```js
var THIS_IS_VARIABLE = false;
```

:x: Bad
```js
var this_is_variable = false;  // Bad!
var ThIs_Is_VaRiAbLe = false;  // Very Bad!
var THIS_is_VARIABLE = false;  // Very Bad!
```

### 區域變數 (Scope Variable)

請用`let`,並且使用`camelCase`.


## 函式 (Function)

一律使用[camelCase](https://zh.wikipedia.org/wiki/%E9%A7%9D%E5%B3%B0%E5%BC%8F%E5%A4%A7%E5%B0%8F%E5%AF%AB).

:heavy_check_mark: Good
```js
public function add() { }
```

:x: Bad
```js
public function Add() { }
```

## 括號 (Curly Bracket)

一律在同一行.

:heavy_check_mark: Good
```js
public function Add() {
}
```

:x: Bad
```js
public function Add()
{ }
```

# TypeScript
> TypeScript的程式規範

* 創檔者: Shen, Jen-Chieh
* 註解: 這裡寫著TypeScript的一些程式規範.


## 檔案相關 (File Related)

* Tab or Space: `SPC`
* Tab Width: `4`


## 文件命名 (File Naming)

一律使用`upper camel case`.

:heavy_check_mark: Good
```ts
GameObject.ts
```

:x: Bad
```ts
gameObject.ts
```


## 註解 (Commenting)

* 基本上應該會跟Egret官方一樣.

### 函式

幾個重要的關鍵字.

* `@desc` - 函式功能標記.
* `@param` - 函式變量標記.
* `@return` - 回傳標記.
* `@attention` - 注意標記.
* `@source` - 來源標記.

範例如下.
```ts
/**
 * @desc Load the animation by file path.
 * @source https://www.google.com/
 * @attention Important notice typed here...
 *
 * @param { string } prefixName Prefix name of the animation targeting.
 * @return { Animation } Loaded animation object.
 */
public loadAnimation(prefixName : string) : Animation { }
```

### 變數

* 沒有特別規則, 乾淨就好.


## 變數命名 (Variable Naming)

### 全域變數 Static

* 沒有特別規則, 視同其他變數.

### 公用變數 Public

使用第一個字一律小寫的`lower camel case`.

:heavy_check_mark: Good
```ts
public int var1;
```

:x: Bad
```ts
public int Var1;   // Bad!
public int _var1;  // Very Bad!
```

### 私有變數 Private

前面一律加`_`底線,之後接著`lower camel case`.

:heavy_check_mark: Good
```ts
private int _var1;
```

:x: Bad
```ts
private int var1;   // Bad!
private int Var1;   // Bad!
private int _Var1;  // Very Bad!
```

### 繼承變數 Protected

* 跟Private一樣.

### Enum

* 全部大寫和底線.

:heavy_check_mark: Good
```ts
enum KeyCode {
    KEY_BACKSPACE,
    KEY_TAB
}
```

:x: Bad
```ts
enum KeyCode {
    key_backspace,
    key_tab
}
```


## 函式 (Function)

### 命名 (Naming)

一律使用[camelCase](https://zh.wikipedia.org/wiki/%E9%A7%9D%E5%B3%B0%E5%BC%8F%E5%A4%A7%E5%B0%8F%E5%AF%AB).

:heavy_check_mark: Good
```ts
public add() : void { }
```

:x: Bad
```ts
public Add() : void { }
```

## 括號 (Curly Bracket)

一律在同一行.

:heavy_check_mark: Good
```ts
public Add() : void {
}
```

:x: Bad
```ts
public Add() : void
{ }
```

## 類別 (Class, Enum, Struct)

命名一律`PascalCase`.


:heavy_check_mark: Good
```cs
enum EnumA { }
class ClassA { }
```

:x: Bad
```cs
enum enumA { }
class classA { }
```

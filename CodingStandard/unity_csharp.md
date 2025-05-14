# Unity CSharp

- 創檔者: Shen, Jen-Chieh
- 註解: 這裡寫著Unity C#的一些程式規範.

## 🔍 檔案相關 (File Related)

* Tab or Space: `SPC`
* Tab Width: `4`

## 🔍 文件命名 (File Naming)

一律使用 `upper camel case`.

✔️ Good

```cs
GameObject.cs
```

❌ Bad

```cs
gameObject.cs
```

## 🔍 註解 (Commenting)

- `函式`和`變數`就使用Visual Studio IDE自帶的, 其他隨意.
- 註解前面有`代碼`的話最少一定要兩格`空格`!

### 函式

```cs
///<summary>
/// Do addition, etc.
///</summary>
public void Add() { }
```

### 變數

```cs
///<summary>
/// Comment here...
///</summary>
public int var1;
```

or

```cs
public int var1;  // 前面最少兩格空格!
```

## 🔍 變數命名 (Variable Naming)

### 全域變數 Static

一律大寫,空格使用底線.

✔️ Good

```cs
public static int VAR1_NAME;
```

*P.S. 唯一一個不是全部大寫的就是使用獨體模式 (Singleton Pattern) 的 `instance`.*

### 公用變數 Public

使用第一個字一律小寫的 `lower camel case`.

✔️ Good

```cs
public int var1;
```

❌ Bad

```cs
public int Var1;   // Bad!
public int _var1;  // Very Bad!
```

### 私有變數 Private

前面一律加 `_` 底線,之後接著 `lower camel case`.

✔️ Good

```cs
private int m_var1;
```

❌ Bad

```cs
private int var1;   // Bad!
private int Var1;   // Bad!
private int _Var1;  // Very Bad!
```

### 繼承變數 Protected

- 跟 Private 一樣.

### Enum

- 全部大寫和底線.

✔️ Good

```cs
enum KeyCode {
    KEY_BACKSPACE,
    KEY_TAB
}
```

❌ Bad

```cs
enum KeyCode {
    key_backspace,
    key_tab
}
```


## 🔍 函式 (Function)

### 命名 (Naming)

一律使用[upper camel case](https://zh.wikipedia.org/wiki/%E9%A7%9D%E5%B3%B0%E5%BC%8F%E5%A4%A7%E5%B0%8F%E5%AF%AB).

✔️ Good

```cs
public void Add() { }
```

❌ Bad

```cs
public void add() { }
```

## 🔍 括號 (Curly Bracket)

一律在下一行.

✔️ Good

```cs
public void Add()
{ }
```

❌ Bad

```cs
public void Add() {
}
```

## 🔍 類別 (Class, Enum, Struct)

命名一律`upper camel case`.

✔️ Good

```cs
enum EnumA { }
class ClassA { }
struct StructA { }
```

❌ Bad

```cs
enum enumA { }
class classA { }
struct structA { }
```

## 🔍 命名空間 (Namespace)

排序從**內建**到**外建**.

✔️ Good

```cs
using System;
using System.Collections.Generic;
using UnityEngine;
using MyBox;  // 外部命名 (External)
```

❌ Bad

```cs
using MyBox;  // 外部命名 (External)
using System;
using UnityEngine;
using System.Collections.Generic;
```

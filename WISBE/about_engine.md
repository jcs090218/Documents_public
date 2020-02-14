# About Engine (關於引擎)
> 這是一個關於引擎基礎的文章.

### getChildByName, findGameObject

這類型的要少用, 這效能消耗是O(n). 直接拿取效能直接是O(1). 以下是小事例.

```ts
@property({
  tooltip: '我們直接從Cocos Creator裡面抓到這裡面.',
  type: cc.Sprite,
})
public sprite : cc.Sprite = undefined;
```

### 強制規定型態

如果設定什麼都是`cc.Node`那就如同全部都是`any`或者`Object`是一樣的道理.

:x: Bad

```ts
private ball : cc.Node = undefined;
```

:heavy_check_mark: Good

```ts
class Ball extends cc.Component { }
private ball : Ball = undefined;
```

### 做分工 和 property

多使用property來使程序介面化. 這是使用介面遊戲引擎的優勢. 
介面化的程序可以交接給設計師去調整. 否則真的累人.

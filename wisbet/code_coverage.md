# Code Coverage 維護性
> 這裡我把"維護性"和Code Coverage擺在一起講.

維護性可以簡單分為以下幾種來判斷`程式碼`或`專案`的可維護程度.

### 基礎

1. 是否遵循程式規範
2. 代碼註解是否清楚 (因人而異;溝通很重要)
3. 代碼質量與易讀性 (拜託Docstring)
4. 是否有文檔支持 (越大型的專案;通常一定需要)
5. 是否用外部插件, 外部插件的程式控管方案 (`信任`或`不被信任`)

### 額外

1. Over-engineer Architecture (禁止過度設計;適當的使用Design Pattern)
2. Premature Optimization (大型專案絕對禁止)
3. Unit Testing (是否有Unit Test或者Example)
  - Example歸類為這一類.
4. 適當的使用關鍵字, TODO, NOTE, SEE, ATTENTION, etc.

Code Coverage主要就是建立在這些基礎之上. Code Coverage越好的專案, 
就能夠越輕易的讓新進的人加入參與貢獻代碼. 也能夠輕易地轉手專案!

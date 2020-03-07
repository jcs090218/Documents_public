# Project Strucutre

## Current Status (2020-02-18)

```
* assets/
├─CommonScript  (Don't Touch)
│  └─Component
│      └─Model
├─resources     (Don't Touch)
│  └─Slot
│      ├─Dimaon_world  (self game res)
│      └─Share         (res config)
└─Slot
    ├─CommonScript
    │  ├─Component
    │  │  ├─BigWin     (Control fro Huge winning.)
    │  │  ├─Graphic    (GamePlay, line painter.)
    │  │  ├─Input      (Input Module)
    │  │  ├─Loader     (Progress Bar / Loading Page)
    │  │  ├─menu       (UI)
    │  │  ├─Model      (Calculation for the game.)
    │  │  ├─SlotWheel  (Core Game, just the wheel)
    │  │  ├─Sound      (BG)
    │  │  ├─Sprite     (Only for one script, slot sprite.)
    │  │  └─Text       (显示三个共用字体?)
    │  ├─Event         (只有一个Enum)
    │  ├─Loading       (Config Loader)
    │  ├─MainGame      (Loading BG, 要改名?)
    │  ├─net           (网路)  *
    │  └─utils         ()
    ├─GameScript       (游戏)
    │  └─Dimaon_world
    └─Scene            (场景)  *
```

## New Status (2020-02-18)

```
Slot
  - Scripts
    - net
  - Scenes
```

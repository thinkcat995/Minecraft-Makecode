# 作業-建造器-金字塔
## 說明
按下執行後，使用聊天指令 A 就會開始建造金字塔的外觀，完成後再自行美化內容。

可以自己嘗試修改 <br/>
1. 變數 level 決定金字塔的高度 <br/>
2. 金字塔的材質 <br/>
3. 建造器在重複4次的移動中，最後的 -2 也可以改成 -1 試試

```template
let level = 0
let _level = 0
player.onChat("A", function () {
    level = 5
    _level = level
    builder.teleportTo(pos(20, 0, 20))
    for (let index = 0; index < _level; index++) {
        builder.mark()
        for (let index = 0; index < 4; index++) {
            builder.move(FORWARD, level * 2 - 2)
            builder.turn(LEFT_TURN)
        }
        builder.tracePath(GOLD_BLOCK)
        builder.shift(1, 1, 1)
        level += -1
    }
})
```

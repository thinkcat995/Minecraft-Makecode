# 作業-建造器-房屋
## 說明
按下執行後，使用聊天指令 H 就會開始建造四方形房屋的外觀，完成後再自行美化內容。

可以自己嘗試修改 <br/>
1. 使用不同的方塊材質 <br/>
2. 平移的大小

n-house 是使用不同的方塊，讓房屋的地板、牆壁及屋頂，都能有不同的材料來組成。

```template
player.onChat("H", function () {
    builder.teleportTo(pos(1, -1, 1))
    builder.setOrigin()
    builder.mark()
    builder.shift(10, 7, 10)
    builder.fill(PLANKS_BIRCH)
    builder.teleportToOrigin()
    builder.shift(1, 1, 1)
    builder.mark()
    builder.shift(8, 5, 8)
    builder.fill(AIR)
})
player.onChat("n-house", function () {
    builder.teleportTo(pos(20, 0, 20))
    builder.setOrigin()
    builder.shift(0, -1, 0)
    builder.mark()
    builder.shift(10, 0, 10)
    builder.fill(BRICKS)
    builder.teleportToOrigin()
    builder.mark()
    for (let index = 0; index < 4; index++) {
        builder.move(FORWARD, 10)
        builder.raiseWall(PLANKS_BIRCH, 5)
        builder.turn(LEFT_TURN)
    }
    builder.teleportToOrigin()
    builder.shift(0, 5, 0)
    builder.mark()
    builder.shift(10, 0, 10)
    builder.fill(PLANKS_SPRUCE)
})
```

# 範例-彩虹塔
## 請聽老師說明
```template
player.onChat("beacon", function () {
    地點 = positions.add(
    player.position(),
    pos(2, 0, 0)
    )
    for (let index = 0; index < 4; index++) {
        for (let value of 彩虹) {
            blocks.place(value, 地點)
            地點 = positions.add(
            地點,
            pos(0, 1, 0)
            )
        }
    }
})
player.onChat("b4", function () {
    地點 = positions.add(
    player.position(),
    pos(2, 4, 2)
    )
    for (let value of 彩虹) {
        blocks.place(value, 地點)
        地點 = positions.add(
        地點,
        pos(1, 0, 0)
        )
    }
    for (let value of 彩虹) {
        blocks.place(value, 地點)
        地點 = positions.add(
        地點,
        pos(0, 0, 1)
        )
    }
    for (let value of 彩虹) {
        blocks.place(value, 地點)
        地點 = positions.add(
        地點,
        pos(-1, 0, 0)
        )
    }
    for (let value of 彩虹) {
        blocks.place(value, 地點)
        地點 = positions.add(
        地點,
        pos(0, 0, -1)
        )
    }
})
player.onChat("BLL", function () {
    地點 = positions.add(
    player.position(),
    pos(8, 0, 8)
    )
    for (let index = 0; index < 20; index++) {
        for (let value of 彩虹) {
            blocks.place(value, 地點)
            地點 = positions.add(
            地點,
            pos(-1, 0, 0)
            )
        }
        地點 = positions.add(
        地點,
        pos(彩虹.length, 1, 1)
        )
    }
})
player.onChat("B77", function () {
    地點 = positions.add(
    player.position(),
    pos(8, 0, 8)
    )
    for (let value of 彩虹) {
        for (let index = 0; index < 7; index++) {
            blocks.place(value, 地點)
            地點 = positions.add(
            地點,
            pos(-1, 0, 0)
            )
        }
        地點 = positions.add(
        地點,
        pos(7, 1, 1)
        )
    }
})
let 地點: Position = null
let 彩虹: number[] = []
彩虹 = [RED_CONCRETE]
```

# 作業-彩虹橋
## 說明
修正彩虹橋的程式內容，產生有7種顏色，橋面有8格寬度的一座彩虹橋。
```template
player.onChat("rainbow", function () {
    圓心 = positions.add(
    player.position(),
    pos(5, 0, 0)
    )
    for (let index = 0; index < 8; index++) {
        for (let value of 彩虹) {
            shapes.circle(
            value,
            圓心,
            20 - 彩虹.indexOf(value),
            Axis.X,
            ShapeOperation.Replace
            )
        }
        shapes.circle(
        AIR,
        圓心,
        20 - 彩虹.length,
        Axis.X,
        ShapeOperation.Replace
        )
        blocks.fill(
        GRASS,
        positions.add(
        圓心,
        pos(0, 0, 20)
        ),
        positions.add(
        圓心,
        pos(0, 0, -20)
        ),
        FillOperation.Replace
        )
        圓心 = positions.add(
        圓心,
        pos(0, 0, 1)
        )
    }
})
let 圓心: Position = null
let 彩虹: number[] = []
彩虹 = [RED_CONCRETE]
```

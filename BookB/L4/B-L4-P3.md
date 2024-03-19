# 範例-動物園
## 請聽老師說明
```template
let 動物: number[] = []
player.onChat("zoo", function () {
    動物 = [CHICKEN]
    for (let value of 動物) {
        mobs.spawn(value, randpos(
        pos(5, 0, 5),
        pos(-5, 0, -5)
        ))
    }
})
player.onChat("fence", function () {
    builder.teleportTo(pos(10, 0, 10))
    builder.mark()
    builder.face(WEST)
    for (let index = 0; index < 4; index++) {
        builder.move(FORWARD, 21)
        builder.turn(RIGHT_TURN)
    }
    builder.tracePath(OAK_FENCE)
})
```

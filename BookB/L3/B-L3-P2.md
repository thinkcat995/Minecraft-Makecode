# 範例-跳水大師
## 請聽老師說明
```template
player.onChat("fish", function () {
	
})
function 水池 (地點: Position, 大小: string) {
    if (大小 == "大") {
        blocks.fill(
        WATER,
        positions.add(
        地點,
        pos(1, -1, 1)
        ),
        positions.add(
        地點,
        pos(10, -3, 10)
        ),
        FillOperation.Replace
        )
    } else {
        blocks.fill(
        WATER,
        positions.add(
        地點,
        pos(1, -1, 1)
        ),
        positions.add(
        地點,
        pos(5, -3, 5)
        ),
        FillOperation.Replace
        )
    }
}
function 傳送 (地點: Position, 高度: number) {
    player.teleport(positions.add(
    地點,
    pos(1, 高度 + 1, 1)
    ))
    gameplay.setGameMode(
    SURVIVAL,
    mobs.target(LOCAL_PLAYER)
    )
}
function 跳台 (地點: Position, 高度: number) {
    blocks.fill(
    PLANKS_BIRCH,
    positions.add(
    地點,
    pos(0, 高度, 0)
    ),
    positions.add(
    地點,
    pos(2, 高度, 2)
    ),
    FillOperation.Replace
    )
    blocks.fill(
    PLANKS_SPRUCE,
    地點,
    positions.add(
    地點,
    pos(0, 高度, 0)
    ),
    FillOperation.Replace
    )
}
player.onChat("jump", function () {
	
})
```

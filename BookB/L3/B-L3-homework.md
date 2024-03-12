# 作業-美味漢堡
## 說明
修改美味漢堡程式，當輸入不同的聊天指令時，產生3種不同口味的漢堡。
```template
player.onChat("no", function (漢堡編號) {
    if (漢堡編號 == 1) {
        player.say("xx漢堡" + "做好囉")
    } else if (漢堡編號 == 2) {
        player.say("xx漢堡" + "做好囉")
    } else {
        player.say("xx漢堡" + "做好囉")
    }
})
function 頂層麵包 (位置: Position, 層: number) {
    shapes.circle(
    SMOOTH_SANDSTONE,
    positions.add(
    位置,
    pos(0, 層, 10)
    ),
    7,
    Axis.Y,
    ShapeOperation.Replace
    )
    shapes.circle(
    SMOOTH_SANDSTONE,
    positions.add(
    位置,
    pos(0, 層 + 1, 10)
    ),
    6,
    Axis.Y,
    ShapeOperation.Replace
    )
    shapes.circle(
    SMOOTH_SANDSTONE,
    positions.add(
    位置,
    pos(0, 層 + 2, 10)
    ),
    5,
    Axis.Y,
    ShapeOperation.Replace
    )
}
function 底層麵包 (位置: Position) {
    shapes.circle(
    SMOOTH_SANDSTONE,
    positions.add(
    位置,
    pos(0, 0, 10)
    ),
    7,
    Axis.Y,
    ShapeOperation.Replace
    )
}
function 生菜 (位置: Position, 層: number) {
    shapes.circle(
    EMERALD_BLOCK,
    positions.add(
    位置,
    pos(0, 層, 10)
    ),
    6,
    Axis.Y,
    ShapeOperation.Replace
    )
}
function 小黃瓜 (位置: Position, 層: number) {
    shapes.circle(
    MELON_BLOCK,
    positions.add(
    位置,
    pos(0, 層, 10)
    ),
    6,
    Axis.Y,
    ShapeOperation.Replace
    )
}
function 豬肉 (位置: Position, 層: number) {
    shapes.circle(
    RED_SANDSTONE,
    positions.add(
    位置,
    pos(0, 層, 10)
    ),
    5,
    Axis.Y,
    ShapeOperation.Replace
    )
}
function 魚肉 (位置: Position, 層: number) {
    shapes.circle(
    YELLOW_GLAZED_TERRACOTTA,
    positions.add(
    位置,
    pos(0, 層, 10)
    ),
    5,
    Axis.Y,
    ShapeOperation.Replace
    )
}
function 雞肉 (位置: Position, 層: number) {
    shapes.circle(
    ORANGE_CONCRETE,
    positions.add(
    位置,
    pos(0, 層, 10)
    ),
    5,
    Axis.Y,
    ShapeOperation.Replace
    )
}
function 牛肉 (位置: Position, 層: number) {
    shapes.circle(
    RED_GLAZED_TERRACOTTA,
    positions.add(
    位置,
    pos(0, 層, 10)
    ),
    5,
    Axis.Y,
    ShapeOperation.Replace
    )
}
function 蕃茄 (位置: Position, 層: number) {
    shapes.circle(
    REDSTONE_BLOCK,
    positions.add(
    位置,
    pos(0, 層, 10)
    ),
    6,
    Axis.Y,
    ShapeOperation.Replace
    )
}
function 太陽蛋 (位置: Position, 層: number) {
    shapes.circle(
    BLOCK_OF_QUARTZ,
    positions.add(
    位置,
    pos(0, 層, 10)
    ),
    6,
    Axis.Y,
    ShapeOperation.Replace
    )
    shapes.circle(
    GOLD_BLOCK,
    positions.add(
    位置,
    pos(0, 層, 10)
    ),
    3,
    Axis.Y,
    ShapeOperation.Replace
    )
}
```

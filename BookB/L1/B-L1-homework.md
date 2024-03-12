# 作業-超級挖洞人
## 說明
結合並修改挖洞人及一拳超人的程式，做出以下幾個功能
1. 玩家走路時，清除前方地面以上 3x2x2 的空間，
2. 玩家衝刺時，以自身為中心清除地面以上 5x3x5 的空間，
3. 玩家潛行時，則是向下挖1格，再向前清除地面以上 3x2x1 的空間，並在玩家的左右兩邊地上插上火把。

```template
player.onChat("do", function () {
    要挖洞嗎 = !(要挖洞嗎)
    player.say("要挖洞嗎? " + 要挖洞嗎)
})
player.onTravelled(WALK, function () {
    blocks.fill(
    AIR,
    pos(0, 0, 0),
    pos(0, 0, 0),
    FillOperation.Replace
    )
})
player.onTravelled(SPRINT, function () {
    blocks.fill(
    AIR,
    pos(0, 0, 0),
    pos(0, 0, 0),
    FillOperation.Replace
    )
})
player.onTravelled(SNEAK, function () {
    blocks.fill(
    AIR,
    pos(0, 0, 0),
    pos(0, 0, 0),
    FillOperation.Replace
    )
    blocks.place(TORCH, pos(0, 0, 0))
})
let 要挖洞嗎 = false
要挖洞嗎 = false
```

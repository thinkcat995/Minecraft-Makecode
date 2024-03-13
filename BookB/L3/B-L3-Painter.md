# 小畫家-函式版
## 說明
請在陣列中設定要使用的方塊。用走路或衝刺的方式都可以在地面作畫。<br/>
聊天指令 c 設定目前用哪一個方塊畫畫。<br/>
聊天指令 s 設定目前畫筆的大小。<br/>
聊天指令 p 設定目前要不要畫畫。<br/>

```template
player.onChat("c", function (num1) {
    if (num1 > 0 && num1 <= 顏料.length) {
        設定使用顏料(num1 - 1)
    }
})
player.onChat("s", function (num1) {
    if (num1 >= 1 && num1 <= 3) {
        設定畫筆大小(num1)
    }
})
player.onChat("p", function () {
    設定畫畫狀態()
})
function 設定畫筆大小 (尺寸: number) {
    畫筆大小 = 尺寸 - 1
    player.say("畫筆大小設為 " + 畫筆大小的文字[畫筆大小])
}
function 畫畫 () {
    if (畫畫中) {
        blocks.fill(
        顏料[目前的顏料],
        pos(畫筆大小 * -1, -1, 畫筆大小 * -1),
        pos(畫筆大小, -1, 畫筆大小),
        FillOperation.Replace
        )
    }
}
function 設定使用顏料 (顏料號碼: number) {
    目前的顏料 = 顏料號碼
    player.say("使用 " + blocks.nameOfBlock(顏料[目前的顏料]) + " 畫畫")
}
function 設定畫畫狀態 () {
    畫畫中 = !(畫畫中)
    player.say("是否要畫畫: " + 畫畫中)
}
player.onTravelled(WALK, function () {
    畫畫()
})
player.onTravelled(SPRINT, function () {
    畫畫()
})
let 畫畫中 = false
let 畫筆大小 = 0
let 目前的顏料 = 0
let 畫筆大小的文字: string[] = []
let 顏料: number[] = []
顏料 = [
WOOL,
ORANGE_WOOL,
MAGENTA_WOOL,
LIGHT_BLUE_WOOL,
YELLOW_WOOL,
LIME_WOOL,
PINK_WOOL,
GRAY_WOOL
]
畫筆大小的文字 = ["小", "中", "大"]
目前的顏料 = 0
畫筆大小 = 0
畫畫中 = false
```

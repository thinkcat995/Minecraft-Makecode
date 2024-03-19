# 範例-陣列教學
## 請聽老師說明
```template
player.onChat("score", function (num1) {
    player.say("" + 姓名[num1] + " 的分數是 " + 分數[num1])
})
player.onChat("get", function (num1) {
    player.say(姓名[num1])
})
player.onChat("info", function () {
    player.say(姓名)
    player.say(姓名.length)
})
player.onChat("random", function () {
    player.say(姓名[randint(0, 姓名.length - 1)])
})
let 分數: number[] = []
let 姓名: string[] = []
姓名 = [
"王小明",
"陳花花",
"李大頭",
"林小玉",
"童童"
]
分數 = [
60,
100,
70,
80,
90
]
```

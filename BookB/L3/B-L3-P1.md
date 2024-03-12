# 範例-開車
## 請聽老師說明
```template
player.onChat("S1", function () {
    player.say("我是駕駛，我要開車出門了")
})
player.onChat("S2", function () {
    player.say("我是乘客，我要搭車出門了")
})
player.onChat("S3", function () {
    player.say("我是駕駛，到目的地要停車下車了")
})
player.onChat("S4", function () {
    player.say("有東西忘在車裡，要拿出來")
})
function 上車 () {
    player.say("坐進車裡")
}
function 下車 () {
    player.say("下車出來")
}
function 開車門 () {
    player.say("打開車門")
}
function 關車門 () {
    player.say("關上車門")
}
function 開車 () {
    player.say("開車上路")
}
function 停車 () {
    player.say("停好車子")
}
function 發動 () {
    player.say("發動引擎")
}
function 熄火 () {
    player.say("引擎熄火")
}
function 放東西 () {
    player.say("放東西")
}
function 拿東西 () {
    player.say("找東西")
    if (找到東西) {
        player.say("拿東西")
    }
}
let 找到東西 = false
找到東西 = true
```

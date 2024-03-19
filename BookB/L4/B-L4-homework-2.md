# 作業-我是創世神
## 說明
完成創世神程式，讓誕生出的生物會顯示正確的名稱。
```template
player.onChat("god", function () {
    player.say("我是創世神，今天要來創造什麼生物呢...")
    基因１ = randint(0, 生物蛋.length - 1)
    player.say("基因１是" + 生物蛋[基因１])
    基因２ = randint(0, 生物蛋.length - 1)
    player.say("基因２是" + 生物蛋[基因２])
    if (基因１ == 基因２) {
        mobs.spawn(LIGHTNING_BOLT, posCamera(0, 0, 3))
        mobs.spawn(生物蛋[基因２], posCamera(0, 0, 3))
        player.say("成功了！誕生出" + 生物蛋[基因２])
    } else {
        mobs.spawn(SPLASH_POTION, posCamera(0, 0, 3))
        player.say("失敗了... 再試一次吧！")
    }
})
let 基因２ = 0
let 基因１ = 0
let 生物蛋: number[] = []
生物蛋 = [CHICKEN]
let 生物名稱 = ["雞"]
```

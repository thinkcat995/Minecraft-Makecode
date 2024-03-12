# 範例-打擊殭屍豬人
## 請聽老師說明
```template
player.onDied(function () {
    gameplay.timeSet(gameplay.time(MIDDAY))
    gameplay.setDifficulty(PEACEFUL)
})
player.onChat("play", function () {
	
})
function 遊戲設定 () {
    gameplay.timeSet(gameplay.time(MIDNIGHT))
    gameplay.setDifficulty(EASY)
    gameplay.setGameMode(
    SURVIVAL,
    mobs.target(LOCAL_PLAYER)
    )
    mobs.give(
    mobs.target(LOCAL_PLAYER),
    GOLDEN_SWORD,
    1
    )
    mobs.give(
    mobs.target(LOCAL_PLAYER),
    SHIELD,
    1
    )
    mobs.give(
    mobs.target(LOCAL_PLAYER),
    GOLDEN_HELMET,
    1
    )
    mobs.give(
    mobs.target(LOCAL_PLAYER),
    GOLDEN_CHESTPLATE,
    1
    )
    mobs.give(
    mobs.target(LOCAL_PLAYER),
    GOLDEN_LEGGINGS,
    1
    )
    mobs.give(
    mobs.target(LOCAL_PLAYER),
    GOLDEN_BOOTS,
    1
    )
}
function 產生殭屍豬人 () {
    mobs.spawn(PIG, pos(0, 0, 5))
    mobs.spawn(LIGHTNING_BOLT, pos(0, 0, 5))
}
mobs.onMobKilled(mobs.monster(PIG_ZOMBIE), function () {
    mobs.spawn(PIG, pos(0, 0, 5))
    mobs.spawn(LIGHTNING_BOLT, pos(0, 0, 5))
})
```

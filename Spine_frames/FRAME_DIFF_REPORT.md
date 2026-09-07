# Spine 动画帧差异分析报告

> 数据源：`D:\Documents\projects\ark-unpack\Spine_frames\`（505 角色，2002 骨架）
> BattleFront 1039 个骨架，BattleBack 959 个骨架

---

## 一、BattleFront vs BattleBack（同一皮肤，不同朝向）

**116 处事件帧差异，涉及 56 个角色。**

### 1.1 OnAttack 帧不同

| 角色 | 皮肤 | 动画 | BF | BB | 差值 |
|------|------|------|----|----|------|
| char_122_beagle | base / boc#1 | Attack.OnAttack | 15 | 14 | -1 |
| char_187_ccheal | base / epoque#2 | Attack.OnAttack | 12 | 14 | +2 |
| char_193_frostl | base / boc#4 | Attack.OnAttack | 15 | 17 | +2 |
| char_241_panda | base / marthe#1 / nian#7 | Attack.OnAttack | 14 | 12 | -2 |
| char_4042_lumen | base / sanrio#2 / ambienceSynesthesia#3 | Attack.OnAttack | 12 | 14 | +2 |
| char_1045_svash2 | base | Attack_A.OnAttack | 15 | 17 | +2 |
| char_1045_svash2 | base | Attack_B.OnAttack | 17 | 15 | -2 |
| char_4172_xingzh | base | Skill_1.OnAttack | 17 | 18 | +1 |
| char_4196_reckpr | base | Skill_Loop.OnAttack | 18 | 17 | -1 |

### 1.2 Skill 出伤帧不同

| 角色 | 皮肤 | 动画 | BF | BB | 差值 |
|------|------|------|----|----|------|
| char_134_ifrit | base / summer#1 / kfc#1 / rilakkuma#1 | Skill_2_Begin.OnAttack | 12 | 9 | -3 |
| char_219_meteo | base / sweep#1 / summer#22 | Skill.OnAttack | 12 | 8 | -4 |
| char_294_ayer | base / boc#3 | Skill_2_Loop.OnAttack | 15 | 14 | -1 |
| char_426_billro | snow#3 | Skill_2_Loop.OnAttack | 18 | 9 | **-9** |
| char_4055_bgsnow | base / yun#7 / wild#7 | Skill_1_Loop.OnAttack | 3 | 9 | +6 |
| char_173_slchan | base / wild#1 / wwf#1 | Skill_Start.OnAttack | 35 | 33 | -2 |
| char_1023_ghost2 | base / boc#6 | Skill_3_Attack.OnAttack | 24 | 21 | -3 |

### 1.3 事件仅在一侧存在

| 角色 | 皮肤 | 动画 | 存在侧 | 缺失侧 |
|------|------|------|--------|--------|
| char_017_huang | base / as#1 / witch#5 | Skill_2_Begin.OnAttack | BB=45 | BF=None |
| char_1020_reed2 | base / epoque#30 / snow#8 / summer#17 | Skill_2.OnAttack | BF=5 | BB=None |
| char_1044_hsgma2 | base | Skill_2_Idle.OnAttack | BB=0 | BF=None |
| char_1044_hsgma2 | base | Skill_2_End.OnAttack | BB=0 | BF=None |
| char_4212_nasti | base | Skill_3_Begin.OnAttack | BF=12 | BB=None |
| char_450_necras | base / summer#20 / ambienceSynesthesia#7 | Skill_2_Loop.OnAttack | BB=0 | BF=None |
| char_1023_ghost2 | base / boc#6 | Skill_1.OnAttack | BB=6 | BF=None |
| char_4025_aprot2 | base / whirlwind#5 | Skill_End.OnAttack | BB=0 | BF=None |
| char_512_aprot | base | Skill_End.OnAttack | BB=0 | BF=None |
| char_466_qanik | base / snow#6 | Skill_End.OnAttack | BB=0 | BF=None |

### 1.4 Start 事件差异（最常见）

涉及角色过多（30+），典型模式：BF 有 OnStart/OnAttack，BB 侧为 None，或反之。

| 角色 | 皮肤 | BF | BB |
|------|------|----|-----|
| char_123_fang | base | OnStart=5 | None |
| char_137_brownb | base / kitchen#1 | OnStart=5 | None |
| char_150_snakek | base / yun#7 | OnStart=6 | None |
| char_174_slbell | base | OnStart=6 | None |
| char_180_amgoat | base / summer#5 | OnStart=24 | None |
| char_236_rope | summer#2 | OnStart=6 | None |
| char_254_vodfox | witch#2 | OnStart=5 | None |
| char_261_sddrag | ambienceSynesthesia#2 | OnStart=5 | None |
| char_274_astesi | shining#1 | OnStart=18 | None |
| char_388_mint | base / epoque#30 / epoque#22 | OnStart=5 (BF) | OnAttack=5 (BB, 互换了事件名) |
| char_4009_irene | base / game#3 / ambienceSynesthesia#3 | None | OnStart=11 |
| char_4011_lessng | base / whirlwind#7 | OnStart=5 | None |
| char_4014_lunacu | base / yun#1 | OnStart=6 | OnStart=12 |
| char_4165_ctrail | base | OnStart=23 | OnStart=9 |
| char_4171_wulfen | base | OnStart=5 | None |
| char_4182_oblvns | base | OnStart=9 | None |
| char_4185_amoris | base / avemujica#1 | OnStart=6 | OnStart=5 |
| char_4198_christ | base / epoque#56 | OnStart=0 | OnStart=5 |
| char_4202_haruka | base / iteration#6 | OnStart=6 | None |
| char_436_whispr | base / witch#4 / nian#4 | OnStart=20 | None |
| char_485_pallas | base / epoque#19 | OnStart=5 | None |
| char_506_rmedic | base | OnStart=6 | None |
| char_605_cmedic | base | OnStart=6 | None |
| char_606_csuppo | base | OnStart=6 | OnStart=15 |
| char_616_pithst | base | OnStart=6 | OnStart=15 |
| char_1044_hsgma2 | base | OnStart=3 | OnStart=9 |
| char_1050_chen3 | base | Start_2.OnAttack=17 | Start_2.OnStart=15 (事件名互换) |
| char_112_siege | striker#2 | OnStart=6 | OnAttack=6 (事件名互换) |

### 1.5 特殊事件差异

| 角色 | 皮肤 | 动画 | 事件 | BF | BB |
|------|------|------|------|----|-----|
| char_1035_wisdel | base | Skill_3_Loop | skill_storage_w | 144 | 141 |
| char_1045_svash2 | base | Skill_3_Combat | OnActivateEffect | 15 | 36 |
| char_1045_svash2 | base | Skill_3_Combat | OnDeactivateEffect | 6 | 0 |
| char_1023_ghost2 | base / boc#6 | Start | OnStart | 3 | None |

---

## 二、同一朝向，不同皮肤

### 2.1 BattleFront

**86 处差异，涉及 43 个角色 + 8 个召唤物。**

#### OnAttack / Skill 出伤帧不同（⚠️ 影响 DPS 计算）

| 角色 | base | 皮肤 | 动画 | base帧 | 皮肤帧 | 差值 |
|------|------|------|------|--------|--------|------|
| **char_291_aglina** | base | summer#5 | Skill1_Loop.OnAttack | 6 | **48** | **+42** |
| **char_291_aglina** | base | summer#5 | Skill2_Loop.OnAttack | 6 | **48** | **+42** |
| char_343_tknogi | base | epoque#9 | Skill_1.OnAttack | 18 | 12 | -6 |
| char_426_billro | base | snow#3 | Skill_2_Loop.OnAttack | 9 | 18 | +9 |
| char_017_huang | base | as#1 | Skill_2_Down_Begin.OnAttack | None | 42 | 新增 |
| char_1035_wisdel | base | sale#14 | Skill_3_Loop.skill_storage_w | 144 | 141 | -3 |
| char_1035_wisdel | base | sale#14 | Skill_Down_3_Loop.skill_storage_w | 144 | 141 | -3 |

> **安洁莉娜(summer#5) 最严重**：技能出伤帧从 frame 6 变成 frame 48，差了 **1.4 秒**。

#### OnPlayAudio 不同（不影响伤害计算）

| 角色 | 皮肤 | 动画 | base | 皮肤 |
|------|------|------|------|------|
| char_197_poca | epoque#12 / rilakkuma#1 | Attack.OnPlayAudio | 39 | 56 |
| char_197_poca | epoque#12 / rilakkuma#1 | Skill_End.OnPlayAudio | 5 | 14 |
| char_2012_typhon | summer#17 | Attack_Loop/Down_Loop/Skill_2_1_Loop.OnPlayAudio | 51 | None（删除） |
| char_2012_typhon | summer#17 | Attack_Begin/Down_Begin/Skill_2_1_Begin.OnPlayAudio | 2 | None（删除） |
| char_214_kafka | snow#3 | Skill_2_Loop.OnPlayAudio | 12 | None |
| char_264_f12yin | marthe#13 | Attack_A/B.OnPlayAudio | None | 5（新增） |
| char_264_f12yin | marthe#13 | Skill.OnPlayAudio | None | 3（新增） |
| char_346_aosta | game#2 | Skill.OnPlayAudio | 60 | 51 |
| char_362_saga | sale#9 | Attack_Loop.OnPlayAudio | 15 | None |
| char_4148_philae | nian#12 | Skill_1.OnPlayAudio | 30 | None |
| char_486_takila | ambienceSynesthesia#2 / shining#2 | Skill_2_End.OnPlayAudio | None | 8（新增） |

#### Start.OnStart 不同

| 角色 | 皮肤 | base | 皮肤 |
|------|------|------|------|
| char_1037_amiya3 | sale#13 | 9 | 15 |
| char_147_shining | summer#1 | 6 | 18 |
| char_148_nearl | summer#2 | 6 | 11 |
| char_171_bldsk | summer#7 | 6 | 9 |
| char_171_bldsk | witch#1 | 6 | 24 |
| char_172_svrash | summer#4 | 3 | None |
| char_199_yak | summer#1 | 3 | 8 |
| char_235_jesica | sweep#1 | 8 | 12 |
| char_235_jesica | wild#2 | 8 | 9 |
| char_236_rope | summer#2 / witch#1 | 9 | 6 |
| char_237_gravel | winter#2 | 9 | None |
| char_290_vigna | as#1 / summer#1 | 9 | 15 |
| char_308_swire | nian#2 | 12 | 5 |
| char_333_sidero | summer#6 | 8 | None |
| char_337_utage | summer#4 | 6 | 9 |
| char_350_surtr | it#1 | 15 | 18 |
| char_400_weedy | snow#2 | None | 6 |
| char_4100_caper | summer#18 | 5 | 9 |
| char_440_pinecn | shining#1 | None | 5 |
| char_449_glider | epoque#17 | None | 20 |

#### 特殊事件增删

| 角色 | 皮肤 | 事件 | base | 皮肤 |
|------|------|------|------|------|
| char_101_sora | epoque#17 | Idle.beat | 318 | 320 |
| char_101_sora | epoque#17 | Die.beat | None | 0 |
| char_101_sora | epoque#17 | Default.beat | None | 0 |
| char_134_ifrit | rilakkuma#1 | Skill_Down_2_End.OnAttack | 0 | None（删除） |
| char_134_ifrit | rilakkuma#1 | Skill_Down_2_Loop.OnAttack | 12 | None（删除） |
| char_134_ifrit | kfc#1 / rilakkuma#1 / summer#1 | Start.OnStart/OnAttack | None | 6（新增） |
| char_4045_heidi | epoque#24 | Skill_1_Begin.OnActivateEffect | None | 14（新增） |
| char_4045_heidi | epoque#24 | Skill_2_Begin.OnActivateEffect | None | 12（新增） |
| char_4045_heidi | epoque#24 | Skill_2_End.OnDeactivateEffect | None | 24（新增） |
| char_172_svrash | summer#4 | Start.OnStrat | None | 12（新增） |

#### 召唤物差异

| 召唤物 | 皮肤 | 事件 | 旧帧 | 新帧 |
|--------|------|------|------|------|
| token_10002_kalts_mon3tr | boc#6→sale#14 | Start.OnStart | 15 | 12 |
| token_10003_cgbird_bird | sightseer#1→witch#1 | Start.OnStart | 6 | None |
| token_10007_phatom_twin | ghost#1→sale#4 | Start.OnStart | None | 3 |
| token_10009_weedy_cannon | sightseer#1→snow#2 | Start.OnStart | 5 | 3 |
| token_10011_beewax_oblisk | epoque#9→summer#11 | Start.OnStart | 5 | 3 |
| token_10018_robrta_mach | ambienceSynesthesia#3→summer#10 | Start/Default/End.OnStart | None | 0~5（新增） |

### 2.2 BattleBack

**72 处差异，涉及 46 个角色 + 2 个召唤物。** 模式与 BattleFront 基本对称。

#### OnAttack 帧不同

| 角色 | 皮肤 | 动画 | base | 皮肤 | 差值 |
|------|------|------|------|------|------|
| char_291_aglina | summer#5 | Skill1/2_Loop.OnAttack | 6 | 48 | +42 |
| char_343_tknogi | epoque#9 | Skill_1.OnAttack | 18 | 12 | -6 |
| char_426_billro | snow#3 | Skill_2_Loop.OnAttack | 9 | 18 | +9 |
| char_1011_lava2 | nian#6 | Skill_2_Begin.OnAttack | 9 | 0 | -9 |
| char_4172_xingzh | epoque#51 | Skill_1.OnAttack | 18 | 17 | -1 |
| char_1035_wisdel | game#9 | Skill_3_Loop.skill_storage_w | 141 | 144 | +3 |

其余 Start/OnPlayAudio/事件增删模式与 BattleFront 一致（同一个皮肤在 Front/Back 两侧同时变化），不再重复列举。

---

## 三、统计总结

| 维度 | BattleFront vs BattleBack | 同Forward不同皮肤 | 同Back不同皮肤 |
|------|--------------------------|-------------------|----------------|
| 总差异处 | 116 | 86 | 72 |
| 涉及角色数 | 56 | 43 | 46 |
| OnAttack 差异 | 9 角色 | 7 角色 | 6 角色 |
| Start 差异 | 30+ 角色 | 20+ 角色 | 20+ 角色 |
| 仅一侧有事件 | 10 角色 | 多个 | 多个 |

### 对 DES 引擎的影响

| 差异类型 | 影响 | 处理方式 |
|----------|------|----------|
| Start 事件 | 不影响战斗模拟 | 可忽略 |
| OnPlayAudio | 不影响伤害 | 可忽略 |
| OnAttack 帧不同(±1~2帧) | 轻微影响 DPS | 需要分朝向+分皮肤提取 |
| OnAttack 帧剧变(6→48) | **严重影响 DPS** | 必须分皮肤处理 |
| 事件在一侧缺失 | 影响战斗逻辑 | 以 BattleFront 为主 |

### 关键发现

1. **安洁莉娜(ch_291)** summer#5 皮肤是最大的异常，技能出伤帧从 6 跳到 48
2. **56 个角色** Front/Back 不一致，不能假设对称
3. **43 个角色**同朝向皮肤之间有差异，DES 必须支持多皮肤数据
4. 大部分差异是 Start/音效，OnAttack 差异约 10 个角色

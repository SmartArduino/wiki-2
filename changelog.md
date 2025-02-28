# Changelog

喵窝的更新记录。

!> **此页尚需完善。**因原Wiki记录遗失，且维护者精力有限，本页或未记录所有事件。

## 2019

### 2019-10【十月更新】
*相关[公告帖](https://bbs.nyaa.cat/d/1478-2019)*  
<span style="background-color: #333333; color: #333333;">一句话：不忘初心，返璞归真</span>

- **[游戏规则](wiki/rules.md)更新**
  + **建筑要求**简化：
    * 公共交通用建筑，须有底座、桥墩（对于桥梁）、照明、防护等合理结构。
    * 建筑（公共交通以外）的硬性要求，仅保留「禁止“擎天柱”、“豆腐块”存在」「禁止建设测试用建筑」。  
    其余要求将仅作建议/指导。
    * 自动化生产装置本身不限制，但应选择于「科技特区」、地下或专用建筑内部署。
    * 如聚落内有建筑规划及风格要求，应遵守。
- **城市规划更新**
  + 取消「主城」概念，各主城（除樱华町外）更名：
    * 东方主城 → **阿库亚斯**
    * 南方主城 → **浪花町**
    * 西方主城 → **柚子小镇**
    * 北方主城 → **北风城**
    * *（※各地相关标识将在随后陆续跟进修改。）*
    * *（注意： 将出生点设为以上主城者，需重新选择出生点，否则`/spawn`将回到位于`(0,0)`的密闭洞穴中。）*
    * <span style="background-color: #333333; color: #333333;">即便不叫“主城”，其作为经济、交通、文化中心，依旧堪称主城</span>
  + [樱华町](nyaa/realms/sakurakacho.md)扩建，设置自建区。
  + 建立村落（景观区）不再要求常驻人口及规划内容。新村落在[城镇村落列表](nyaa/realms.md)登记后，即视为有效。
- **经济规则调整**
  + ~变更出生点~ 村落间传送命令`/town select` 之费用，降至 45 节操/次。
- **维度功能调整**
  + 脑洞世界 `brainhole` 保留，作为像素画专用托管区域。其余内容转移至子服务器 `miu`（美羽实验室）。
- **内容调整**
  + RPGItem即将适配新版：
    * 大部分原基于RPGItem的**武器装备**不再恢复功能。
    * 然而，部分**实用道具**仍将恢复。
    * 后续将添加新型道具（如玩具、工具）。
    * NPC将随之恢复。

### 2019-9-20【Minecraft 1.14.4】
- 服务器主体升级至1.14.4版本。以下服务器除外：
  + 因相关插件有待跟进，子服务器`inf`暂时停留于1.13.2版本。
  + 子服务器`Freebuild`关闭。
- 主服务器三个非原版维度`EpicWorld` `EpicNether` `EpicEnd`同步重置。
- CE（CustomEnchantment）插件移除，相关附魔不再有效。
- RPGItem、Capcat（即传送牌）与NPC暂停服务。其中：
  + RPGItem相关插件仍在为升级准备；
  + NPC同上。  
  *（10月中旬已恢复，但升级前的NPC均未回归，疑似全部删除；商店NPC需重新放置。）*
  + 因原告示牌升级为“橡木告示牌”，Capcat需跟进更新相关逻辑。*9月21日修复*
- 高级玩家（Advanced）用户组取消，并入玩家（Player）组。
  + 原Advanced权限下放，如木牌商店空间额度。详见《经济设定》。
- HEH（HamsterEcoHelper）增加若干短命令，以便交易顺畅。
- 主服务器备份方式完全改为「增量备份」。  
因此，玩家不会再收到以下定时备份的消息：

```
[公告] Time now 2019/09/20 Sun 18:00 CST
[公告] 正在备份服务器喵~可能会有点卡喵~

[公告] 备份成功了喵~撒花~
```

### 2019-8-17 → 8-30【the *REAL* Aquatic Update】
- 主世界水域“升级”至1.13+版本风格。包括水底方块、冰山、生态群系等。
- 期间，建立一个与主世界使用相同种子的镜像世界；对比两个世界相应水域的海拔Y=63及以下方块，在主世界是水方块、水流的，替换为镜像世界对应的方块。
- 以下为令人惊喜的成果：
  + 东城海星城正下方、小鱼塘以西海面，猹湾以南海面，皆发现珊瑚群。
  + QQ村港湾以西，海面上冒出大量冰山。为已知距离樱华町最近的冰山群。
- 过程中出现了一些副作用：
  + 由于未采取“重生成”方式，除水以外的一切皆予保留。你可以在新海床下发现曾经遍布旧海底的砂砾层。
  + 海床下依靠水工作的人工装置（守卫者渔场、自动化瓜菜生产装置等）遭到大面积破坏。水几乎为岩石取代，鱼类、瓜果等无法输送。
  + 世界多地出现怪异海滩、沉船，其在Y=63以上本应出现的新方块被削去。
  + 所有新出现的海泡菜未自动“开灯”，需人工干预。

### 2019-07-17【NyaaWiki架构变更】
- 由 BookStackApp 迁移至 [Docsify](https://docsify.js.org)。
  + 因无任何迁移工具支持，所有文档均须以 Markdown 语言重写；
  + 现知识库基于[GitHub仓库](https://github.com/NyaaCat/wiki)；
  + 因此，编辑者需掌握基本的 Git 操作与 Markdown 语法。详见 [参与贡献Wiki](wiki/contribute.md)。
- 原BookStackApp知识库于7月21日下线，数据不再保留。

### 2019-05【服务器设定变更】
- [经济规则调整](https://bbs.nyaa.cat/d/1410-20190514)
  + **死亡惩罚取消。**但保留“死亡掉落”。
  + Capcat 传送木牌最低传送费用降低为 1 节。
  + 改变出生点 `/town select` 费用降低为 450 节每次。
  + 前后缀更改费用降低为 42 节
  + `/sethome` 的费用范围变为 45 - 450，每 100 格降低 20，其他不变。
  + `/home` 基础费用变为 9，单位 100 格增量改为 1，其他不变。
  + `/back` 基础费用变为 9，单位 100 格增量改为 1，其他不变。
- **维度调整**
  + 新增 资源末地`EpicEnd`；
  + 新增 资源下界`EpicNether`；
  + 同步恢复使用跨维度传送命令`/mvtp` `/goto`。
- NyaaUtils 经验存储瓶[更新](https://bbs.nyaa.cat/d/1408-20190514-nyaautils)
  + 现在有存储经验的*附魔之瓶* 被砸碎后，所存经验会分散到经验球中。
- 服务器登录地址[变更](https://bbs.nyaa.cat/d/1409)。

### 2019-3-4【出生点更新】
- 现在 `/espawn` 目的地重归大神殿。

### 2019-3-2【白名单申请方式变更】
- 即日起开放申请，不再要求是否有邀请人。
  + 不过，有邀请人可**增加**些许的过审可能性。
- 开放“迎新群”供申请人初步了解社区情况，并接受审视。
- 移除对Google+个人主页的要求（因其即将停止服务）。

### 2019-2-1【用户组改革】
- 现仅保留三个用户组（含“管理员”）。以下用户组撤销，不再保留相应权限：
  + 建筑师（Builder）
  + 创造组（Creator）
  + 城主（Moderator）
- 原隶属于上述用户组的玩家，按活跃度<sup>*（需要验证）*</sup>划归“高级玩家”或“玩家”组。

- - -
## 2018

### 2018-12-29 【服务器群组更新】
- 开放“无尽地狱”服务器`inf`。<sup>[（公告帖）](https://bbs.nyaa.cat/d/1373-infinity-infernal-bug)</sup>
  + 设定为轻 RPG 的 PVE 游戏服务器。承接原EpicWorld“黑化世界”功能，独立开服，装备与怪物强度将趋于合理。
  + 同时，主服务器启动“去RPG化”进程。
- 开放“自由创造服务器”`freebuild`。<sup>[（公告帖）](https://bbs.nyaa.cat/d/1375-freebuild)</sup>
  + 其目的是“共建世界”，因此并不同于地皮世界等专用建筑区，而是允许全体玩家释放想象力、发挥建筑特长的世界建筑工程。
  + 每期会有一个抽象主题，用于抛砖引玉，为玩家建筑提供各方面的思路方向。

### 2018-11-8 【Minecraft 1.13.2】
服务器已更新 1.13.2，目前带来如下变更：

- EpicWorld 已重置 - 使用 1.13 新地形生成
- 黑化和血月插件暂时移除 - 等待功能更新或移动到网内其他服务器使用
- 服务端由 Spigot 更改为 PaperSpigot
- 移除电梯插件，请使用游戏内机制建设电梯
- 暂时移除 Shopkeeper 插件，NPC 不会生成。待喵窝的 NPC 插件开发完成后，新的 NPC 会出现
- 网内其他服务器陆续升级中，可能需要很长一段时间完善/修复等。欢迎有兴趣帮忙的玩家报名。
- 部分插件仍没有完全兼容新版，因此可能会出错或不正常工作（例如飞行塔）。

玩家发现的一些变化<sup>[（讨论帖）](https://bbs.nyaa.cat/d/1362-minecraft-1-13-2-aquatic-update)</sup>：

- 依赖命令方块（需触碰按钮、踏板或陷阱箱）传送的装置全部失效。已知系新版不支持从命令方块执行由插件提供的命令所致。
- NyaaUtils现支持徒手点亮、熄灭红石灯，该权限下放至所有玩家。
- 部分树叶在旧版属性`decayable = true`时，若附近无树干，进入新版必消失。
- 大量RPGItem功能失效或异变。*后续基本修复大部分*
- 加载区块时，若有“无皮肤头颅”，会导致客户端卡顿。
- 新进玩家的`/espawn`目的地，不会随选择出生点而改变——即总是回到“新手密闭洞穴”中。<sup>（直至2019年3月4日）</sup>

### 2018-7-7 【黑化设定更新，掉落分布更新】
*相关[公告帖](https://bbs.nyaa.cat/d/1298-20180707)*

- 黑化怪血量大幅提升；伤害和部分技能则被削弱。
- 掉落分布完全重写。现在掉落物价值基本和黑化怪等级匹配。
- 现在作战需要更多技巧，乐趣更多。

### 2018-03 若干更新

*   NyaaWiki 由 DokuWiki 迁移到了 BookStackApp
    *   新版 Wiki 已经不再需要了解 Wiki 或者 markdown 语法，而是改为了所见即所得（WYSIWYG）编辑器。虽然这并不符合喵窝的极客风格，但是在一定程度上方便了更多非 IT 技术指向的玩家来协助编辑更美观、易用的知识库。
*   东方主城开放
    *   希望入居、前往经商等玩家现在可以准备前往
    *   之前在东城有住所、因东城重建而搬离的玩家现在可以免费领取一套住房或商铺，或继续选择自建区建造房屋。这些玩家移居东城的 spawn 点迁移费用可联系管理组补偿

### 2018-02 若干更新

*   PlayTimeTracker 的 AFK 判定调整，只要没有玩家操作则不再计时，即使玩家在挂机池等设施中
*   移除了玩家切换世界 `/mv tp [世界名称]` 的权限。玩家需要通过 `/spawn`、`/home` 等其它命令和世界内传送木牌、传送门前往其它世界
*   开设了喵窝历史服务器 （`/server archive`）
*   ~砍树以后，所砍树木的树叶不再掉落。玩家必须用剑自行清理~

- - -

## 2017

### 2017-12-18 NyaaUtils 等插件更新

*   NyaaUtils 掉落物保护现在有了新的选项，可单独设置不收取原版掉落物、按住 shift 时收取原版掉落物、默认收取原版掉落物。此举是为了解决开启掉落物保护的玩家攻击黑化时背包常常被低价值物品塞满，收获的高价值物品容易被怪物炸毁的问题。
*   在喵窝，经验修补时会自动挑选磨损程度最严重的物品维修，而非原版随机挑选物品维修，但需要玩家将 NyaaUtils 的掉落物保护打开。
*   InfernalMobs 在 RecursiveG 的努力下完成了重构，解决了黑化怪很多存在已久的 bug，提升了性能。
*   血月相关
    +   死亡重新加入的时候会自动传送到死亡箱旁边，而不是默认位置。
    +   血月用传送方式（比如 `/back`）到场地内会自动加入，不需要自己 `/bm join` 了。
        

### 2017-11-13 至 11-29 粒子效果等

*   NyaaUtils 新增 [粒子效果](https://wiki.nyaa.cat/books/%E7%8E%A9%E6%B3%95%E6%95%99%E7%A8%8B/page/nyaautils-%E7%B2%92%E5%AD%90%E6%95%88%E6%9E%9C) 设定功能
*   [NyaaUtils 新增经验胶囊功能](https://bbs.nyaa.cat/d/1182)，玩家拿着经验瓶即可将自身经验保存在此物品中，并从该物品恢复
*   EpicWorld 黑化掉落物品调整
    +   若干物品的掉落所需等级范围大幅调整   
    +   追加了 Lv.5 的强化水晶掉落
    +   追加了一系列奇怪的系统征购物品
    +   若干黑化掉落小吃也被追加到系统征购列表中
        

### 2017-07-28 申请方式变更

*   恢复了以前的邀请加入制
*   但与以往不同，申请人的申请将通过邀请人发送到 NyaaCat 的群组内，**所有社区成员将可以看到申请内容**
    

### 2017-06-25 Minecraft 1.12

*   服务端版本升级到 1.12
*   SignShop 和 SignChestShop 正式下线
*   [Capitalized NyaaCat](https://wiki.nyaa.cat/books/%E7%8E%A9%E6%B3%95%E6%95%99%E7%A8%8B/page/capcat) 的传送牌功能正式上线
    

### 2017-05-03 出生点更新

*   由传统的单一出生点改为多出生点
    +   [论坛讨论](https://bbs.nyaa.cat/d/985)
    +   进入服务器后，如果没有确定的出生点，将自动打开提示，选择一个出生点后即可传送到对应坐标。
    + 首次进服的玩家，将首先被安置到“新人密闭洞穴”中，并立即被要求指定出生点。选择后方可继续游戏。
      - 如未选择（按E退出菜单），虽可通过`/espawn`离开该洞穴，但`/spawn`会回到该洞穴。并且此后每次登录皆会被重新要求选择。
    +   老玩家可以暂时不指定出生点（即大神殿）。
    +   选择后，使用 `/spawn` 命令将返回之前选择的出生点。
    +   首次设置出生点免费，但如果修改需要支付 12450 节操。
    +   执行 `/home`、`/back` 等命令时，按照玩家设置的出生点距离计费。   
*   主世界**启用死亡掉落**
*   下界 [重新开放玩家建设](https://bbs.nyaa.cat/d/987)
*   重置了 EpicWorld
*   现在喵窝玩家可以使用 `/server kedama` 命令便捷的前往 [毛玉線圈物語](https://craft.moe) 服务器

关于“新人密闭洞穴”的描述<sup>（原载于《新人指南》）</sup>：

> 这里是一个废弃矿井的临时休息室。矿洞因过度开采已经坍塌，只有这间休息室靠着特殊的保护支架免于塌方。前后的通路都已经被封锁，你必须选择一个出生点才能离开这里。
    
### 2017-04-07 至 04-15 春季更新
    
*[论坛讨论](https://bbs.nyaa.cat/d/963)*
    
*   明确「不允许利用漏洞等方式生产或获取资源」
*   不再禁止刷怪塔、村民交易、各类自动化生产设施
*   恢复玩家自主规划建设工程的补贴
*   经济设定若干调整
    +   天喵木牌商店
        -   普通玩家组可创建 10 个木牌，高级玩家组 12 个
        -   普通玩家组可使用 42 个物品槽，高级玩家组可使用 45 个
    +   天喵商城
        -   普通玩家组可上架 6 个物品，高级玩家组可上架 12 个
        -   广告的展示次数范围从 20-200 更改为 10-400。
    +   重命名命令由 /rename 改为 /nu rename。如果需要包含空格，请将物品名称使用反引号（`` ` ``）括起来。该命令的价格与之前一致。
    +   现在可以申请规划领域提示，玩家进入设置的领域后将展示名称和管理玩家。费用为每个方块 1 节操。
    +   建立银行的最低冻结资本降低到 100 万节操。        
*   动力燃料的速度和时间提升
*   `/spawn` 恢复使用
*   `minigame` 世界启用死亡节操惩罚
*   地区设定，玩家进入地区后将有名称、地区类型、管理者等提醒，使用`/nu realm info` 可查看当前所处地区详情。
*   RPGItems 削弱远程玩法，大部分武器将不可通过副手弓远程打出伤害。
*   可通过 `/heh search` 查询物品在木牌商店的销售情况和分布，详见 [天喵商城·木牌商店](space/plugins/hamsterecohelper.md)
    

### 2017-03-08 三八经济改革·二

*[论坛讨论](https://bbs.nyaa.cat/d/938)*
    
*   系统服务调整
    +   `/home` 和 `/back` 改为按出生点距离递增计费，最低 42 节操，最高 198 节操。
    +   `/sethome` 改为按出生点距离递减计费，最低 99 节操，最高 998 节操。
    +   前缀设置价下调至 198 节操 + 100 经验 / 次。
    +   后缀设置价下调至 99 节操 + 100 经验 / 次。
    +   支持颜色和样式的物品重命名价格下调至 45 节操 / 次 / 个。
*   新增 [广告服务](https://bbs.nyaa.cat/d/935)。
*   商店调整
    +   公共交易使用的木牌，必须设置在店面中。
    +   店面原则上必须设置在主世界的商业区或 EpicWorld。
    +   玩家允许自由入驻商业区中的空店面，占用店面须尽快部署商店。
    +   店面必须保持活跃。
    +   普通玩家组可以创建 4 个木牌，高级玩家组可以创建 6 个。
    +   普通玩家组可以使用 32 个物品槽（slot），高级玩家可以使用 42 个。
    +   交易消费税 2%。
    +   天喵商城交易消费税上调到 5%。
*   公共工程所需建材由生存玩家有偿供应。

### 2017-02-28 商店更新

*   天喵木牌商店将用于替代长时间不更新且性能较差的 SignShop 和 SignChestShop。
*   **这两个插件将在 capcat 上线之前被移除**，因此请尽快将使用这些插件的商店转移到天喵木牌商店。
*   具体操作方法请见 [这里](space/plugins/hamsterecohelper.md)。
    

### 2017-01-28 至 02-05 服务器架构和设定更新

*   在 BungeeCord 的帮助下开始向群组型服务器转变。
    +   原有的 M 世界现在在新的 NyaaCat Wasteland 服务器（代号 `tsuki`）下运行。
    +   原有的 S 世界移动到主服务器的 EpicWorld 世界，并增大世界半径。
    +   原有的 EpicWorld 世界直接关闭。
    +   原有的 M 世界仍将在主服务器保留至 2017 年 2 月 15 日，请在此日期之前取回自己的遗留物品。已经于 2 月 9 日提前关闭。
    +   使用 `/server [服务器代号]` 命令在不同服务器间切换。
    +   关于各服务器的设定和规则等信息详见 [server](wiki/server-network.md)        
*   世界设定更新
    +   主世界中，建筑师玩家不再能使用创造模式，但可以付费使用 `/fly` 命令。创造组玩家不受此影响，但不能再使用 `/give` 命令。
*   死亡惩罚现在最低扣除 100 节操，最高依然是 10000 节操，按死亡玩家的现金计算。    
*   在线奖励的每日、周、月奖励将按照系统 balance 的值发放，有最低值和最高值的限制。  
*   死亡惩罚、交易的税现在都会保存到系统 balance。也就是，现在天喵的活跃度将会直接影响在线奖励的额度。
*   随着 Librazy 为 RPGitem 增加若干新特性，未来将推出各种新型 bug 玩具。
*   [新增兑换物「月芒符卡」](https://bbs.nyaa.cat/d/876)，分为 6 个等级，不同的符卡或符卡组合可以兑换不同的物品。
*   西方主城市政厅增加沙子与一些美丽方块的兑换，以弥补缺少使用原生生成器的 M 世界造成的部分类型资源短缺。
*   白名单申请要求变更
    +   邀请玩家 ID **不再是加入喵窝的必须要求**，但仍然作为申请加分项。
    +   不再要求在 NyaaBBS 拥有至少 20 篇帖子。
        

### 2017-01-10 喵窝三周年将至

*   Minecraft 服务端版本更新到 1.11.2
*   银行系统上线
    +   与其他服务器不同，我们的银行插件仅用于提供通用银行系统，也就是，没有所谓的「系统银行」或「官方银行」，所有的银行业务、资金调度都将由个人玩家运营，并通过插件提供服务。
    +   详细了解及申请开设银行的说明，请移步 [喵窝联合银行](nyaa/economic/nyaabank.md)。
*   血月的判定方案调整
    +   新的判定方案将按照普通怪物的击杀、黑化不同等级的击杀和助攻计分。
    +   额外增加了摸鱼的判定和团队奖励，以此提升普通玩家的参与度并平衡奖励。        
*   如果错过了高级玩家的领取，或长时间不上线被降级为普通玩家，现在将可以通过 `/ptt recur advanced` 重新申请积累，积累到足够的时间后即可再次获取奖励，不再需要重置累计在线时间。
*   为庆祝喵窝三周年的到来，即日起至 **2017 年 1 月 16 日**，每日在线奖励**三倍**。三周年当日的额外奖励及其他活动另行通知。

- - -

## 更早年份的更新

* [2016](changelogs/2016.md) :cat:
* [2015](changelogs/2015.md) :heart:
* [2014](changelogs/2014.md) :cyclone:

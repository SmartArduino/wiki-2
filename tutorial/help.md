# 常用命令速查表

!> **查询前请注意**

- 本表格仅包含对喵窝 Minecraft 服务器常见命令的介绍，具体的命令说明、操作方法等请查阅 NyaaWiki 的其它相关页面。
- 如无特殊说明，如果需要手持物品，均为**主手持有**。
- 部分命令收费或征税，备注为 **“收费”**。收费明细请参考 [世界经济设定](nyaa/economic.md)。
- 对于某些命名类命令，如果名称中含有空格，需要使用反引号 **\`** 将全部内容包围。  
示例：```/nu suffix `&f宝 生 永 梦` ```

## 传送类

| 命令| 说明| 备注 |
| ------------ | ------------ | ------------ |
| `/espawn`  | 返回喵窝默认出生点      |当前为大神殿|
| `/spawn`   | 返回玩家设定的出生点    |   |
| `/mv list`  |查看世界列表   |   |
| `/mvtp [维度代号]`<br />`goto [维度代号]`  |前往指定[维度](nyaa/worlds.md "也称世界")的默认出生点   |   |
| `/back`  | 返回上一次传送前所在位置  |收费   |
| `/home`  | 传送回家  | 收费  |
| `/home [家的名称]`  | 传送回指定名称的家  | 收费  |
| `/sethome`  |  设置家 | 收费  |
| `/sethome [家的名称]`  | 设置一个家  |  	收费 |
| `/delhome [家的名称]`  |  删除一个家 | |
| `/town select` | 变更出生点，村落间传送  | 初次免费，此后每次均收费  |
| `/server [服务器代号]` |前往指定的[服务器](wiki/server-network.md "查看服务器列表") | |


## 经济 / 市场类

| 命令| 说明| 备注 |
| ------------ | ------------ | ------------ |
|`/balance`<br />`/bal`	|查看现金余额	 ||
|`/nb my` | 查看银行存款及贷款总额 ||
|`/pay [玩家 ID] [金额]`	|转账给指定玩家	|执行后**立即转账**，请慎用|
|`/ptt ac`	|领取刚刚提示的PTT奖励	 ||
|`/heh market view`<br />`/hm`	|打开世界商店	 ||
|`/heh market offer [单价]`<br />`/hm [单价]`	|将手中的物品上架到世界商店|	收费|
|`/heh requisition req [物品ID] [单价] [数量]`<br />`/hreq [物品ID] [单价] [数量]`	|发起征购	 |物品ID为“hand”时，征购手中的物品|
|`/heh requisition sell [数量（可选）]`<br />`/hsell [数量（可选）]`	|手持征购中物品，响应征购	 ||
|`/heh auction auc [起步价] [步进价] [保留价（可选）]`<br />`/hauc [起步价] [步进价] [保留价（可选）]`	|发起拍卖，拍卖手中的物品	 ||
|`/heh auction bid [价格]`<br />`/hbid [价格]`	|在拍卖中出价	|价格**留空**或为“min”时，跟进可允许的最低价格|
|`/heh retrieve [confirm]`	|取回购买后，暂存于系统的物品|	执行前，需腾退背包/末影箱空间|
|`/heh shop sell [单价]`	|上架商品到你的木牌商店|	执行前，对准自己的商店“SELL”木牌|
|`/heh shop storage set`	|设置收购存储箱	 ||
|`/heh shop storage info`	|查询收购存储箱位置	 ||
|`/heh shop buy [单价]`	|将手中的物品添加到收购列表	|执行前，对准自己的商店“BUY”木牌|
|`/heh shop lotto set`	|设置抽奖奖池存储箱	 ||
|`/heh shop lotto info`	|查询抽奖奖池存储箱位置	 ||
|`/heh search [关键词] [选项:值]`	|搜索世界木牌商店中的商品	 ||
|`/heh searchpage [页码]`	|搜索结果页翻页	 ||
|`/heh transaction sellto [玩家 ID] [单价]`<br />`/hsellto [玩家 ID] [单价]`	|向指定玩家出售手中物品，并发送账单	 ||
|`/heh transaction pay [账单 ID]`<br />`/hpay [账单 ID]` |支付指定账单，并收货	|收费|
|`/heh transaction cancel [账单 ID]`	|取消指定账单	 ||
|`/npc hehshop`	|创建一个NPC，替代自己售货	|与自己样貌相同|
|`/npc hehshop remove`	|移除自己创建的NPC	 ||

### 木牌商店搜索选项

*   `i` 或 `item`：物品名称或 ID，仅搜索指定物品
*   `p` 或 `player`：玩家 ID，仅搜索指定玩家
*   `r` 或 `range`：搜索范围，仅搜索指定距离内有木牌的商店
*   `a` 或 `advanced`：高级搜索选项：
    *   `ench`：搜索包括附魔
        *   `enchonly`：仅搜索附魔
        *   `lore`：搜索包括描述
        *   `loreonly`：仅包括描述 选项间用 `|` 并列，如 `ench|lore`

?> :v: **以上参数组合范例**  
在所有木牌商店中，查找带有『经验修补』附魔的附魔书：  
`/heh search MENDING i:enchanted_book a:ench`


## 物品类


| 命令| 说明| 备注 |
| ------------ | ------------ | ------------ |
|`/nu rename [名称]`	|重命名物品	|可使用样式代码；收费|
|`/nu repair info`	|查看手中物品修复信息	||
|`/nu repair hand`	|修复主手上的工具、武器	|消耗副手上的一个修复用材料|
|`/nu repair full`	|修复主手上的工具、武器	|副手持修复用材料，尽最大可能修复|
|`/nu enchant info`	|查询副手中附魔源详情	 ||
|`/nu enchant [附魔名称] [附魔等级]`	|对主手的物品附魔	|牺牲副手上的附魔源|


## 辅助类

| 命令| 说明| 备注 |
| ------------ | ------------ | ------------ |
|`/nu lp`	|切换战利品保护开关	|| 
|`/nu lp ignorevanilla`<br />`/nu lp ig` |开启战利品保护|忽略原版物品|
|`/nu lp rejectvanilla`<br />`/nu lp re` |开启战利品保护|拒绝原版物品，但按住 Shift 键仍可捡起|
|`/nu lp includevanilla`<br />`/nu lp ac`|开启战利品保护|包括原版物品|
|`/nu el`	|切换飞行动力开关	| |
|`/nu mailbox create`	创建邮箱	|执行后，右键点击要用作收件箱的箱子||
|`/nu mailbox remove`	|删除自己的邮箱	 ||
|`/nu mailbox info`	|查看自己的邮箱信息	 ||
|`/nu mailbox send` [玩家 ID]	|发送手中的物品	|收费|
|`/nu mailbox sendchest [玩家 ID]`	|发送一箱物品	|执行后，右键点击此箱子；收费|
|`/nu prefix [前缀]`	|设置名称前缀	|可使用样式代码；收费|
|`/nu resetprefix	`|删除名称前缀	|| 
|`/nu suffix [后缀]`	|设置名称后缀	|可使用样式代码；收费|
|`/nu resetsuffix`	|删除名称后缀	 ||
|`/nu format`	|查看可用的样式代码	 ||
|`/nu show`	|展示手中的物品	 ||
|`/nu exhibition set`	|设置物品展示框保护	 ||
|`/nu exhibition unset`	|取消物品展示框保护	 ||
|`/nu expcap store [经验值]`	|将指定数量的经验存储到附魔瓶里	|经验值为“all”时，存储身上所有经验|
|`/nu expcap restore [经验值]`	|从附魔瓶提取指定数量的经验	|经验值为“all”时，提取所有经验|
|`/nu sit`	|开启或关闭“席地而坐”	|仅支持半砖、楼梯、毛毯、床（在白天）|
|`/nu se sign [行数] [内容]` | 预编辑手中的告示牌 |编辑后放置，直接点击“完成”|
|`/mail send [玩家 ID] [正文]`	|向指定玩家发送私信	 |正文加玩家ID字数限制**244字**|
|`/mail read`	|阅读新私信	 ||
|`/mail clear`	|清空私信箱	 ||

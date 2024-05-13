#自己写一些关于游戏中可能出现的算法，或者说脚本
## drop.lua
模拟击杀怪物后装备的掉落程序：
首先，击杀怪物后50%概率掉落对应的套装部位，但达到某个掉落次数后，触发保底机制，即下一次一定掉落之前未掉落的套装部位，当集齐套装所有部位后，保底机制重置。

这个脚本运行后是循环击杀怪物，直到集齐所有套装。

### 运行示例
击杀火焰怪后有50%概率掉落随机的火焰套装部位，火焰套装为：{"火焰剑", "火焰甲", "火焰盔", "火焰靴"}，当连续掉落4次还未集齐套装，则下一次触发保底，直到集齐套装退出循环。
![连续4次火焰甲的情况](https://github.com/manun2nd/game-algorithm/assets/101537160/1998190b-ae79-421c-aaa2-ef7e7b4130b8)

## match.lua
这是一个1v1随机匹配算法，初始有10名玩家。
1. 将10名玩家分为5组，分组如下：第一组（玩家1，玩家2）、第一组（玩家3，玩家4）、第一组（玩家5，玩家6）、第一组（玩家7，玩家8）、第一组（玩家9，玩家10）
2. 不同组的玩家会被随机匹配到一起进行1v1对战。
3. 拥有自检脚本，循环100000次，证明：（1、匹配玩家双方非同组；2、无玩家轮空；3、无死循环）

### 运行示例
![随便跑100000次没有出错](https://github.com/manun2nd/game-algorithm/assets/101537160/7556192c-0f3a-4e0d-859f-83e4de289283)

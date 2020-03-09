# CSGOTacticSimulator
CSGO战术模拟器
## 示例
https://www.iaders.com/upload/2020/0305/CTSDemo.gif
## 提示
- 可以通过点击图片获得坐标. 
- 坐标与图片在窗口内的缩放程度无关, 可以任意改变窗口大小而不用修改脚本. 
- 将鼠标移到人物点上, 可以看到该角色信息 (编号, 物品, 坐标). 
## 脚本
### 提示
- 每行脚本代表某个角色进行了某个动作, 例如购买 (瞬间), 移动 (耗时), 等待. 
- 脚本中角色之间的顺序并不影响最终效果, 例如可以把某个角色的动作集中在一起写出, 也可多个角色一起按时间顺序编写脚本. 
### 查询表
|语法|解释|实现与否|
|----|----|----|
|set camp [t, ct]|设置当前队伍|√|
|create team [ct, t] [pistol, eco, forcebuy, quasibuy]|生成队伍在出生点, 并自动配备武器与投掷物|×|
|create character [t, ct] {坐标}|在指定的坐标生成一名角色|√|
|delete character {角色编号}|删除一个角色|×|
|give character {角色编号} weapon {武器}|为某个角色配备指定武器|√|
|give character {角色编号} grenade {投掷物} <{投掷物} ...... {投掷物}>|为某个角色配备指定投掷物|√|
|give character {角色编号} props [bomb / defusekit]|为某个角色配备炸弹 / 拆弹器|√|
|set character {角色编号} status [alive / dead]|设定某个角色的存活状态|√|
|set character {角色编号} vertical position [upper / lower]|设定显示某个角色处于三维地图的上方或下方|√|
|action character {角色编号} move [run / walk / squat / teleport] {坐标}|将角色移动到某一地点|√ (除了teleport)|
|action character {角色编号} throw [smoke / grenade / flashbang / firebomb / decoy] {坐标} <{坐标} ...... {坐标}>|让角色投掷投掷物到某一坐标 |√|
|action character {角色编号} shoot [{坐标} / {目标编号} [die / live]]|让角色向某坐标或某目标射击|√|
|action character {角色编号} do [plant, defuse]|让角色下 / 拆包|√|
|action character {角色编号} wait until {秒数}|让角色原地等待到指定秒数|√|
|action character {角色编号} wait for {秒数}|让角色原地等待指定秒数|√|
|create comment {秒数} {坐标} {内容}|在指定时间地点创建一个标注|×|
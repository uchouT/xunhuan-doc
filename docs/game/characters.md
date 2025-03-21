# 角色设定

example: (gcd 你看着修改)

## 属性

### 基础属性

- 等级 ：玩家阵营单位会根据等级提升，获取相应的分配点数，分为数值点和技能点数。数值点由玩家自行分配给血量与蓝量，技能点数则是在学习一个新技能之后消耗。

- 血量：战斗内外都会使用的数值，怪的血量是会随等级提升的，可能拟定一个函数或者干脆留空手动填写。

- 蓝量：玩家用于释放各种技能的，怪物本身是没有蓝量的，无限火力来的。

- 防御力：物理，魔法，元素的对应防御力，单纯留出数值空间，计算时也只需要直接伤害-防御即可。

- 抗性：由一些装备/生物被动提供的百分比抗性。

- 敏捷：决定战斗中行动顺序的属性。

- 暴击伤害：游戏中的暴击是修正伤害，为+25％一类乘区。

- 移动力：一次移动时能够位移的格数。为敏捷/x+修正。

- 种族:不一定在战斗中会用到，但确实是所有个体都能有的。

  以上为目前能想到的所有在战斗中，几乎全单位共有的属性。以下为主角/主角团在战斗外可能用到的属性数值。

- 技能点：学习技能时的消耗。

- 幸运：**仅玩家拥有**，主要用于开宝箱，掉落，一些判定。

- 体力：**仅主角团拥有**，在**探索地图**中采集资源时会消耗的属性，不同的角色有不同的体力值。会在某些情况下增加。

- ？？：**仅玩家拥有**，暂时没想名字，总之是一个考量玩家具体游玩状态的一个数值，类似于什么灵魂坚韧程度或是别的什么。

- 正义值:**仅玩家拥有**，(未确定是否要实装)给玩家能够抢劫作恶的自由度，主要作用是售价变动，决定一个npc的加入与否。

- 好感：**仅主角团与一些常见重要npc拥有**,触发特定剧情的参考数值。

- 疲劳度：**仅玩家拥有**，由于游戏中有时间设定，且睡觉与否由玩家决定，用于催促玩家睡觉的数值。

- 熟练度：(考虑实装与否)，各项生产类技能不光需要学习，还需要熟练度才能进行等级的提升。

  

#### 伤害属性

- 伤害计算：游戏的伤害区间设计打算做成两部分，做基础与结果的区分为2个乘区—增幅与增伤。简单的说就是提升20％和造成伤害增加20％这两种情况，前者更加高贵。一方面是其结算在防御力之前，另一方面是其占用了稀少乘区。举个栗子。玩家这次伤害为100点，拥有20的伤害提升与武器的30造成伤害提升，怪物拥有25的易伤与30点防御力。这次伤害最终为（100x1.2）-30)x(1+0.3+0.25)=139.5,而暴击的区间放在前一个乘区，比如+50爆伤则1.2变为1.7。

- 物理：简单的物理伤害，数值由武器与技能提供，如一个战技是造成相当于武器攻击力/2+x点物理伤害，这里要注意一些点。任何物理伤害都吃造成收益但是不一定吃增幅收益。由物理方式如普攻，战技所造成的伤害吃物理伤害提升，而如过一个法术造成物理伤害，其所吃的增幅为法术伤害增幅。如果是全类增幅那么正常吃。
  （这么设计的想法是，法师应该有基础的应对方式面对一个极高法抗的怪，需要有造成物理伤害的手段，而法师武器本身没有攻击力，无法平a，就变成物理伤害法术，但是法师堆一堆物理buff又感觉有点神经，结果是类似于，一个冲击波法术，造成物理伤害，你法强越高这个波越痛）

- 魔法：法术类的技能的伤害会直接写明在法术上。玩家可以通过装备，前缀等方式增幅这个法术的伤害。尤其是多样化的前缀。

- 元素：本质上是魔法伤害，但是区分于魔法存在。设定类似于魔法伤害是纯粹的魔力冲击，而元素就是更实体化的攻击。元素伤害分为：火，水，木，土，风，雷，光，暗。
  （这里要指出，光暗的特殊性，首先是暗，除暗之外的7种元素为基础元素，暗本身在概念上就是一个异类，其更类似于湮灭的概念。然后是元素一般是吃0.5x的魔抗与1x的元素抗，比如10点火伤打10法抗0火抗就是5点伤害，而光，暗本身不吃任何抗性，以真实伤害存在。）

  元素伤害的设计理念是，让玩家对抗怪物的元素伤害，以及控制数值。比如我现在打一个怪，怪有500点单体法伤。而前排的坦克位堆了500点的法抗。那就会形成一个完全刮不动前排的情况，如果简单提升怪的伤害至1000点，则对于后排而言是毁灭性的打击。但是对前排还是不怎么痛。如果使用元素这种，类法穿的机制，只需要750点元素伤害就能打出1000点法术伤害的效果，同时，后排角色可以根据经验选择相对应的抗性来增加收益。你出等量的元素抗和法抗的难度可以认为是一样的，在这种情况下可以让抗性收益加倍来增加配队的操作感。

#### 某某类属性

- ...

### 特定属性？
根据剧情设计来，可以在这里打上 `#todo`，描述你的设计，以后我们看着来，一起设计。

## 角色列表
（以后再说）
example: 

| 角色名  | 职业  | 等级 | 描述 |
|---------|------|------| --- |
| 阿尔托莉雅 | 剑士 | 100  |可以通过`<br>` 来换行 |
| 艾米莉娅 | 魔法师 | 90  | 效果 <br> 如下 |
| 库洛米 | 盗贼 | 85  | 可以在此多行描述：<br> 属性1: ... <br> 属性2: |

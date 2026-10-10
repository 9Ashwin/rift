# 教学项目：信标回收

## 一句话

做一款 3D 低多边形单人潜行小品：玩家进入一座断电的观测站，回收三枚信标，躲开巡逻的“回声体”，再从电梯撤离。

这是教学垂直切片，不是商业游戏企划。它借鉴短流程恐怖游戏的压力设计，但不复刻任何现有游戏的题材、美术、规则或关卡。[1][4]

## 为什么选它

- Godot 负责角色、状态机、交互、敌人 AI、UI 和导出。
- Blender 负责场景 blockout、低多边形道具、简单动画与碰撞体。
- 一张地图、一个敌人、三件目标物，能跑通完整循环，不需要多人服务、程序生成或一堆素材。
- 资产导入先走 Godot 官方 glTF/GLB 流程，工具链可验证，也能解释每一步发生了什么。[25]

## 核心循环

```text
进入设施 → 搜索信标 → 听见/看见巡逻者 → 躲避或用诱饵转移注意
→ 拿齐信标 → 回到电梯 → 成功撤离
```

首版只做一条 3 到 5 分钟的路线。巡逻者只有三个状态：巡逻、调查声源、追逐。玩家不能战斗，失败后回到入口重来。

## 学习目标

1. 用 `CharacterBody3D` 做第一人称或越肩移动和碰撞。
2. 用 `Area3D`、信号和可交互接口实现拾取、开门、撤离。
3. 用明确的游戏状态管理 `探索 / 被发现 / 成功 / 失败`，避免把状态散落在各个脚本里。
4. 用 `NavigationAgent3D` 做巡逻、调查和追逐。
5. 在 Blender 制作一组风格统一的道具，导出 glTF/GLB，检查尺度、朝向、材质和碰撞体。
6. 做一个能导出、能重开、能结束的完整 build。

## 里程碑

### 0. 灰盒

Godot 里先用方块搭一条走廊、两间房和电梯。完成移动、镜头、碰撞、交互提示。

**验收**：新玩家从入口走到电梯，能拾取一个占位物并触发提示。

### 1. 完整玩法

加入三枚信标、出口条件、失败和重开。先不碰 Blender，所有资产继续用灰盒。

**验收**：集齐三枚信标才能撤离；被发现后能进入追逐并产生失败结果；重开不会残留旧状态。

### 2. Blender 资产

把灰盒逐步替换成 5 到 8 个低多边形资产：控制台、信标、门、灯、储物柜、诱饵设备。资产按类别管理，原始 `.blend` 与导出 `.glb` 分开存放。

**验收**：改动 Blender 源文件后能重新导出；Godot 场景里比例、方向、材质和碰撞均正确。资产走 glTF/GLB 工作流。[13][25]

### 3. 巡逻者与声音

加一个敌人、三个巡逻点和一个可投掷诱饵。声音与灯光负责提示危险，不加复杂战斗系统。

**验收**：敌人能巡逻、响应声源、追逐玩家；玩家能看懂自己为什么被发现。

### 4. 收尾

加标题页、设置、音量、胜败界面和导出说明。找没看过项目的人试玩一轮，记录卡住的位置。

**验收**：从启动到胜利/失败再到重开，全程没有编辑器操作；一局不超过 5 分钟。

## 先不做

- 联机、排行榜、账号系统。
- 随机地图、复杂背包和技能树。
- 大量敌人、武器系统、剧情分支。
- 必须购买 API 额度的 3D 生成步骤。Rodin/Tripo 只当可选工具，先用 Blender 自制或占位模型把玩法跑通。Rodin MCP 的账户/工作区授权和 Tripo API 的独立积分都要单独核对。[18][19][20]

## 推荐学习顺序

1. GDQuest 的 3D Arena FPS 入门项目，先熟悉 Godot 的移动、场景、射击和导出概念。[12]
2. 阅读 Packt 配套仓库，补 Blender 建模、动画和导入 Godot 的完整步骤；书籍正文是否可用按出版社许可处理。[13]
3. 对照 Godot 官方 3D 场景导入文档，把自己的 `.blend` 资产导成 glTF/GLB。[25]
4. 以本 brief 为范围做一款完整小品，再考虑接 MCP 或生成式 3D 工具。

## 项目边界

所有玩法、角色、关卡和素材都做原创。参考作品只用来拆机制，不复制名称、外观、音效、地图或文本。第三方教程、插件与素材按各自许可证使用。

## Sources

[1] https://steamdb.info/app/1304930/charts
[4] https://godotengine.org/article/godot-showcase-buckshot-roulette
[12] https://github.com/gdquest-demos/getting-started-with-godot-4
[13] https://github.com/PacktPublishing/Game-Development-with-Blender-and-Godot
[18] https://hyper3d.ai/features/mcp
[19] https://www.tripo3d.ai/help/credit/how-do-credits-work
[20] https://www.tripo3d.ai/help/api-plugins/tripo-studiotripo-api
[25] https://docs.godotengine.org/en/stable/tutorials/assets_pipeline/importing_3d_scenes/index.html

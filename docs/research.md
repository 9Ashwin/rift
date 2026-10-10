# 游戏案例、工具与教程

**检索快照：2026-10-10**。这不是一份“全网最火榜”，而是按 Godot + Blender 教学价值筛出的候选。GitHub 星数、Steam 并发和 X 页面都会变化，复用时请再核一次。

## 游戏案例

| 案例 | 可核对的热度信号 | 值得拆的部分 | 对教学项目的用法 |
|---|---|---|---|
| The Outlast Trials | SteamDB 记录 2026-10-08 历史峰值 147,955。[1] | 目标驱动的恐怖流程、追逐节奏、风险与撤离。 | 学它怎么把“做目标”变成压力，不照搬多人规模。 |
| WARDOGS | SteamDB 记录 2026-09-13 历史峰值 428,666。[2] | 大规模战场的可读性、队伍协作和武器反馈。 | 当作系统设计观察材料，不适合第一个项目照着做。 |
| Slay the Spire 2 | SteamDB 记录 2026-03-08 历史峰值 574,638。[3] | 卡牌构筑、路线选择、可组合的内容数据。 | 适合研究“少量规则如何长出很多局面”，但它不是 Godot/Blender 技术样板。 |
| Buckshot Roulette | Godot 官方把它列为 2024 年独立游戏成功案例，并在 2026 年访谈开发者；开发者谈到 Godot 的使用经验。[4][5] | 小空间、短回合、信息揭示和风险升级。 | 作为 Godot 小体量游戏的案例，不复制其题材、规则或美术。 |
| Bongo Cat | 媒体报道指出它的在线人数与桌面挂件/按键计数玩法有关。[26] | 桌面常驻、低干扰互动、装饰收集。 | 提醒我们别把 Steam 并发数直接当成“核心玩法很强”的证据。 |

这些峰值的时间跨度不一样。Outlast Trials 是这里最新的短期峰值；WARDOGS 和 Slay the Spire 2 更适合当玩法和规模案例，不该说成 10 月正在霸榜。

## GitHub 工具与工作流

星数和推送时间是本次 GitHub API 快照，不是质量分。

| 项目 | 快照与许可证 | 适合做什么 | 采用时注意 |
|---|---|---|---|
| [awesome-gamedev-agent-skills](https://github.com/gamedev-skills/awesome-gamedev-agent-skills) | 1,396★，Apache-2.0，README 列出 74 个跨引擎技能，2026-10-09 有更新。[8] | 给 Codex、Claude Code、Cursor 等 Agent 装游戏开发技能，覆盖 Godot、Unity、Unreal 等。 | 先挑 Godot 与美术资产相关技能，不要整包塞进上下文。 |
| [godot-agent](https://github.com/aigengame/godot-agent) | 48★，MIT，2026-10-10 有更新；项目标注 pre-1.0，支持 Godot 4.4+，需要 Python 3.13+。[9] | CLI、Agent Skill、MCP；可做 headless 检查，也能控制运行中的游戏并读日志/截图。 | 很新，先在空白 demo 验证，再接正式项目。 |
| [MCP for Blender](https://github.com/ahujasid/mcp-for-blender) | 30,384★，MIT，2026-10-06 有推送；社区项目，不是 Blender 官方插件。[27] | 通过 MCP 让 Agent 创建和操作 Blender 场景、对象与模型。 | 先在副本里试，限制它能改的目录和操作范围。 |
| [Blender Skills](https://github.com/arjun988/blender-skills) | 283★，MIT；README 列出 94 个 Blender 技能，支持 Codex、Claude Code、Cursor、Kiro。[28] | 细分建模、材质、场景和导出步骤，配合 Blender MCP 做执行。 | 先挑课程用得到的技能；README 的兼容性和数量属于作者自述。 |
| [GodotMaker](https://github.com/RandallLiuXin/GodotMaker) | 550★，README 标注 BUSL-1.1，2026-09-17 更新。[10] | 把想法自动化成 Godot 原型，支持 Claude Code、Codex、OpenCode。 | 代码可见不等于宽松开源；商业使用前读清 BUSL 条款。 |
| [Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios) | 26,062★，MIT，2026-10-08 更新；仓库描述为 49 个 Agent、72 个工作流技能。[6] | 参考游戏团队的 Agent 分工、协调和研发流程。 | 主要为 Claude Code 设计；想用 Codex 得适配，不是装上就通用。 |
| [game-ui-design-workflow](https://github.com/guiguiyan930-source/game-ui-design-workflow) | 226★，MIT，2026-08-05 更新。[7] | 游戏 UI 原型、风格延展、页面一致性和资源交付流程。 | 偏 Cursor Agent；用前先检查当前 CI 与示例是否仍能跑通。 |
| [Impeccable](https://github.com/pbakaus/impeccable) | 79,259★，Apache-2.0，2026-10-09 更新。[24] | 通用界面设计与评审工作流，可借鉴视觉方向和 critique/polish 流程。 | 它主要面向 Web UI，不是 Godot 控件或游戏 UI 的现成插件。 |

## Godot 与 Blender 学习资料

| 资料 | 内容与状态 | 建议 |
|---|---|---|
| [Godot 官方 demo projects](https://github.com/godotengine/godot-demo-projects) | 官方示例与模板仓库，9,634★、MIT，2026-10-08 更新。[11] | 看具体场景、渲染和脚本写法时优先查它。 |
| [GDQuest：Godot 4 入门项目](https://github.com/gdquest-demos/getting-started-with-godot-4) | 仓库含完整的 2D Vampire Survivors 风格与 3D Arena FPS 入门项目，108★，2026-05-16 更新。[12] | 先照着做一个完整小作品，再开始自己的教学项目。仓库 API 没识别出 SPDX 许可证，复用代码前先看仓库内 LICENSE。 |
| [Game Development with Blender and Godot](https://github.com/PacktPublishing/Game-Development-with-Blender-and-Godot) | Packt 图书配套代码，MIT，2023-01-18 更新；内容覆盖低多边形建模、动画、GLTF 导出和 Godot 场景。[13] | 这是配套代码仓库，不代表书籍正文免费。适合补 Blender 到 Godot 的完整手把手路径。 |
| [Godot 3D 场景导入文档](https://docs.godotengine.org/en/stable/tutorials/assets_pipeline/importing_3d_scenes/index.html) | Godot 官方说明 3D 场景与资产导入流程。[25] | 课程先采用 Blender 导出 glTF/GLB 的原生流程，稳定后再试自动化插件。 |
| [blender_godot_io](https://github.com/melvspacestudio/blender_godot_io) | Blender→Godot glTF 导出/链接工具；README 明确标注 WIP，当前仓库未声明 SPDX 许可证。[14] | 作为实验项目观察，不要把它设成课程的必需依赖。 |
| [blender-godot-pipeline](https://github.com/indiedevcasts/blender-godot-pipeline) | MIT；README 说明仍在开发，只支持有限的 mesh 导出流程，不能批量导出；2024-10-20 有推送。[15] | 可读它怎么处理重置变换和碰撞体命名，不建议依赖它承担整个资产管线。 |

## AI 生成 3D 资产与 MCP

| 工具 | 查到的事实 | 结论 |
|---|---|---|
| [Hyper3D Rodin MCP](https://hyper3d.ai/features/mcp) | 官方 MCP 说明通过浏览器登录并选择 Hyper3D workspace；MCP 连接不要求把 API key 填进客户端。[18] | “不用填 API key”不等于“免费无限用”。提交生成前确认当前 workspace、套餐和计费。 |
| [Tripo MCP](https://github.com/VAST-AI-Research/tripo-mcp) | Tripo 官方 GitHub 仓库，MIT；最后推送时间为 2025-04-14。[16] | 能接入 MCP，但版本较旧，接入前核对 API、依赖和模型版本。 |
| [Tripo Blender 插件](https://github.com/VAST-AI-Research/tripo-3d-for-blender) | Tripo 官方 Blender 扩展，MIT；最后推送时间为 2025-11-06。[17] | 可作为 Blender 内生成资产的入口，先在独立文件里试。 |
| Tripo 计费 | 官方帮助中心明确说明 Studio 网页积分与 API 积分分开；Studio 会员不自动附送 API 积分。[19][20] | MCP/API 调用前单独确认额度，别从网页会员状态推断 API 可免费用。 |

### 短视频截图里的工作流建议

截图账号为 @八郎AI，原帖链接和发布日期无法从截图确认。作者的建议是：Codex 做 3D 游戏时，简单、重复的资产可以用 Rodin MCP 批量生成；复杂资产再到网页端细调。作者也提到 Tripo 有 MCP 调用，但 API 费用与网页会员不共享。

这段是作者的使用建议，不是已验证的通用最佳实践。官方资料确认 Rodin MCP 通过浏览器授权并选择 workspace，不需要把 API key 填进客户端，但这不代表生成免费或不限量。[18] Tripo 官方帮助中心确认网页 Studio 积分与 API 积分分开。[19][20]

仓库只记下截图里的要点，没有上传截图文件；原帖链接和时间待补。

## X 上的公开线索

这几条是公开索引能找到的帖子，不是 X 全站趋势榜，也没有可靠的互动量排序。

- [Alex Prompter 的帖子](https://x.com/alex_prompter/status/2101609043077042547)展示了 Codex 通过 MCP 调用 Hyper3D Rodin 生成 3D 资产的工作流。[21]
- [Tripo 官方账号](https://x.com/tripoai)在 2026-10-08 发布了 Tripo P2.0 生成环境、再放进 Blender 拆分的演示。[22]
- [Godot 官方账号](https://x.com/godotengine/status/2021906412537069630)提到 Buckshot Roulette 开发者加入 Godot Development Fund，可作为引擎生态动态，不是游戏热度排名。[23]

## 我会怎么选

- **先学会做完一款**：GDQuest 的 3D 入门项目 → Blender/Godot 配套教程 → 自己做一张小关卡。[12][13]
- **让 Agent 帮忙改 Godot 工程**：先试 `godot-agent` 的一个 headless 检查流程；它还在 pre-1.0，别让它直接接管整个项目。[9]
- **需要美术流程**：先看 `awesome-gamedev-agent-skills` 的资产制作技能；生成模型只做可选加速，最终要检查拓扑、尺度、材质、碰撞体和许可。[8]
- **想让 Agent 操作 Blender**：先看 `MCP for Blender`，再用 Blender Skills 把步骤拆成可复用指令；两者都先在项目副本里试。[27][28]
- **要学习 AI 团队编排**：看 CCGS 的工作流结构；若目标是 Godot UI，则把 `game-ui-design-workflow` 的阶段拆解改成 Godot 资源和场景交付。[6][7]

## Sources

[1] https://steamdb.info/app/1304930/charts
[2] https://steamdb.info/app/1867240/charts
[3] https://steamdb.info/app/2868840/charts
[4] https://godotengine.org/article/godot-showcase-buckshot-roulette
[5] https://80.lv/articles/buckshot-roulette-developer-on-making-the-game-solo-feedback-success
[6] https://github.com/Donchitos/Claude-Code-Game-Studios
[7] https://github.com/guiguiyan930-source/game-ui-design-workflow
[8] https://github.com/gamedev-skills/awesome-gamedev-agent-skills
[9] https://github.com/aigengame/godot-agent
[10] https://github.com/RandallLiuXin/GodotMaker
[11] https://github.com/godotengine/godot-demo-projects
[12] https://github.com/gdquest-demos/getting-started-with-godot-4
[13] https://github.com/PacktPublishing/Game-Development-with-Blender-and-Godot
[14] https://github.com/melvspacestudio/blender_godot_io
[15] https://github.com/indiedevcasts/blender-godot-pipeline
[16] https://github.com/VAST-AI-Research/tripo-mcp
[17] https://github.com/VAST-AI-Research/tripo-3d-for-blender
[18] https://hyper3d.ai/features/mcp
[19] https://www.tripo3d.ai/help/credit/how-do-credits-work
[20] https://www.tripo3d.ai/help/api-plugins/tripo-studiotripo-api
[21] https://x.com/alex_prompter/status/2101609043077042547
[22] https://x.com/tripoai
[23] https://x.com/godotengine/status/2021906412537069630
[24] https://github.com/pbakaus/impeccable
[25] https://docs.godotengine.org/en/stable/tutorials/assets_pipeline/importing_3d_scenes/index.html
[26] https://www.eurogamer.net/steams-fourth-most-played-game-doesnt-really-make-any-money-and-its-developer-says-its-better-off-that-way
[27] https://github.com/ahujasid/mcp-for-blender
[28] https://github.com/arjun988/blender-skills

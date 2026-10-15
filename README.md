# AI 模型可视化生成测试汇总 · AI Visual Bench

收集不同 AI 模型在同一可视化生成任务上的作品，按测试分组，提供纯静态展示站。
*A collection of visual-generation tests comparing AI models, with a static, build-free gallery site.*

**展示站 / Live site:** https://hephaestusgame.github.io/ai-visual-bench/

## 测试列表 / Tests

### 1. 蒸汽朋克机械蜜蜂 / Steampunk Mechanical Bee

要求模型用**单个 HTML 文件**实现可交互的蒸汽朋克机械蜜蜂。测试灵感来自 [@NovaXCode 的帖子](https://x.com/NovaXCode/status/2110223641111888338)；本仓库所有作品均使用下面这段提示词生成（亦见 [PROMPT.md](tests/steampunk-bee/PROMPT.md)）：

```text
Build a complete, self-contained HTML app using Three.js r160+, OrbitControls, and lil-gui to create a highly detailed, animated 3D steampunk mechanical bee.

Design: Articulated brass head, amber compound eyes, spring antennae, exposed clockwork gears, four iridescent mechanical wings, six segmented legs, and a five-part abdomen with glowing power core and spiral stinger.
Materials: Realistic PBR brass, oxidized copper, blued steel, amber glass, and translucent wings with entirely procedural textures and details.
Animation: High-frequency wing flapping, correctly synchronized interlocking gears, moving antennae, and subtle body motion.
Exploded View: Smooth 0–1 slider separating components along radial or axial axes, with cyan leader lines.
GUI: Exploded View, Flap Frequency (0–60 Hz), Flight/Idle, Gear Speed (0.1×–5×), Wireframe, and Explode Axis controls.
Rendering: Responsive full-screen WebGL, ACES tone mapping, cinematic studio lighting, soft shadows, and smooth delta-time-based animation.

Generate all geometry and textures procedurally. Use no external models or image assets. Return complete, executable HTML from <!DOCTYPE html> to </html>, with functional controls, clean code, no placeholders, and no TODOs. Prioritize visual fidelity, mechanical detail, and performance.
```

按模型综合能力排序（参考 Artificial Analysis 智能指数与 LMArena，2026-10），非本测试结果。

| 模型 | 耗时 | 链接 |
|---|---|---|
| Claude Opus 5.5 | 150 分钟 | [运行](https://hephaestusgame.github.io/ai-visual-bench/tests/steampunk-bee/claude-opus-5.5/) · [源码](tests/steampunk-bee/claude-opus-5.5/index.html) |
| GPT 6 Astra | 18 分钟 | [运行](https://hephaestusgame.github.io/ai-visual-bench/tests/steampunk-bee/gpt-6-astra/) · [源码](tests/steampunk-bee/gpt-6-astra/index.html) |
| Gemini 4 Argon | 10 分钟 | [运行](https://hephaestusgame.github.io/ai-visual-bench/tests/steampunk-bee/gemini-4-argon/) · [源码](tests/steampunk-bee/gemini-4-argon/index.html) |
| Grok 4.7 | 40 分钟 | [运行](https://hephaestusgame.github.io/ai-visual-bench/tests/steampunk-bee/grok-4.7/) · [源码](tests/steampunk-bee/grok-4.7/index.html) |
| GLM 5.3 | 15 分钟 | [运行](https://hephaestusgame.github.io/ai-visual-bench/tests/steampunk-bee/glm-5.3/) · [源码](tests/steampunk-bee/glm-5.3/index.html) |
| GLM 5.3 Flash | 38 分钟 | [运行](https://hephaestusgame.github.io/ai-visual-bench/tests/steampunk-bee/glm-5.3-flash/) · [源码](tests/steampunk-bee/glm-5.3-flash/index.html) |
| DeepSeek V4.1 Flash | 12 分钟 | [运行](https://hephaestusgame.github.io/ai-visual-bench/tests/steampunk-bee/v41-flash/) · [源码](tests/steampunk-bee/v41-flash/index.html) · [README](tests/steampunk-bee/v41-flash/README.txt) |


### 2. 蒸汽朋克独眼巨人 / Steampunk Cyclops

要求模型用**单个 HTML 文件**实现带完整游戏动作套件的 3D 蒸汽朋克独眼巨人角色。提示词由本仓库作者编写，本类别所有作品均使用下面这段提示词生成（亦见 [PROMPT.md](tests/steampunk-cyclops/PROMPT.md)）：

```text
使用 Three.js r160+、OrbitControls 和 lil-gui 构建一个完整的、自包含的 HTML 应用，创建一个高度精细、带动画的 3D 蒸汽朋克独眼巨人角色，并具备完整的游戏动作套件。
设计：
粗壮的岩石质躯干、巨大的独眼眼球、厚重的肌肉束、皮革护腕与腰带、锈蚀金属肩甲、背负的巨型蒸汽锤，以及分段式五指巨掌与柱状双腿。头部为铰接式黄铜头骨，中央嵌有巨大的琥珀色独眼，眼眶环绕黄铜环，头顶覆盖锈蚀装甲板。胸腔是外露的锅炉结构，表面散布啮合齿轮、压力表、铜制液压管和发光的能量核心。背部有双烟囱锅炉背包，侧面挂着铜罐与排气管。肩、肘、膝、髋等关节处均有外露齿轮与液压活塞。右手持一把巨型蒸汽锤，锤头带有发光核心。
材质：
逼真的 PBR 黄铜、氧化铜、发蓝钢、锈蚀铁、裂纹皮革、岩石皮肤、琥珀玻璃眼球，以及带有完全程序化纹理和细节的金属磨损、锈迹、铜绿和皮革纹理。所有纹理必须通过 canvas 程序化生成，不使用任何外部图片或模型。
动画：
完整的游戏动作套件，包括待机呼吸、行走、奔跑、跳跃、落地、重锤砸击、横扫、投掷、受击、眩晕、嘲讽、咆哮、施法、死亡，以及技能施放全套状态机。动作应基于骨骼关节旋转实时计算，支持平滑过渡、循环动作与非循环动作，非循环动作结束后自动回到待机。独眼眼球应有微动和脉动发光，胸口能量核心与锤头核心应随时间闪烁。
爆炸视图：
平滑的 0–1 滑块，沿径向或轴向（X/Y/Z）分离装备与骨骼组件，并带有青色引导线，从原始位置连接到分离后的位置。爆炸轴可在径向、X 轴、Y 轴、Z 轴之间切换。
GUI：
爆炸视图滑块、爆炸轴选择、动作状态切换（待机/行走/奔跑/跳跃/重锤砸击/横扫/投掷/受击/眩晕/嘲讽/咆哮/施法/死亡）、动画速度（0.1×–5×）、齿轮转速（0.1×–5×）、线框模式、显示骨骼、自动旋转。
渲染：
响应式全屏 WebGL、ACES 色调映射、电影级工作室灯光（主光、补光、轮廓光、眼部点光源）、柔和阴影、基于 delta-time 的平滑动画、PMREM 程序化环境贴图、程序化雾效与地面。
技术要求：
完全以程序化方式生成所有几何体和纹理。不使用任何外部模型或图像资源。返回从 <!DOCTYPE html> 到 </html> 的完整、可执行 HTML，具有可正常使用的控件、干净的代码，无占位符，无 TODO。优先考虑视觉保真度、机械细节和性能。
```

| 模型 | 耗时 | 链接 |
|---|---|---|
| GPT 6 Astra | 32 分钟 | [运行](https://hephaestusgame.github.io/ai-visual-bench/tests/steampunk-cyclops/gpt-6-astra/) · [源码](tests/steampunk-cyclops/gpt-6-astra/index.html) |

## 目录结构 / Layout

- `index.html` — 展示站（纯前端，无构建）
- `tests/index.json` — 类别列表（展示页按此顺序渲染）
- `tests/<test>/models.json` — 每个测试的元数据（模型、耗时、文件路径、来源）
- `tests/steampunk-bee/<model>/index.html` — 原样保存的作品；`thumb.png` 为无头 Chromium 截取的封面

## 署名与许可 / Credits & License

- 蒸汽朋克蜜蜂灵感：[@NovaXCode](https://x.com/NovaXCode/status/2110223641111888338)。
- 代码：[MIT](LICENSE)。

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

| 模型 | 耗时 | 链接 |
|---|---|---|
| Gemini 4 Argon | 10 分钟 | [运行](https://hephaestusgame.github.io/ai-visual-bench/tests/steampunk-bee/gemini-4-argon/) · [源码](tests/steampunk-bee/gemini-4-argon/index.html) |
| Claude Opus 5.5 | 150 分钟 | [运行](https://hephaestusgame.github.io/ai-visual-bench/tests/steampunk-bee/claude-opus-5.5/) · [源码](tests/steampunk-bee/claude-opus-5.5/index.html) |
| GLM 5.3 Flash | 38 分钟 | [运行](https://hephaestusgame.github.io/ai-visual-bench/tests/steampunk-bee/glm-5.3-flash/) · [源码](tests/steampunk-bee/glm-5.3-flash/index.html) |
| Grok 4.7 | 40 分钟 | [运行](https://hephaestusgame.github.io/ai-visual-bench/tests/steampunk-bee/grok-4.7/) · [源码](tests/steampunk-bee/grok-4.7/index.html) |
| DeepSeek V41 Flash | 12 分钟 | [运行](https://hephaestusgame.github.io/ai-visual-bench/tests/steampunk-bee/v41-flash/) · [源码](tests/steampunk-bee/v41-flash/index.html) · [README](tests/steampunk-bee/v41-flash/README.txt) |
| GPT 6 Astra | 18 分钟 | [运行](https://hephaestusgame.github.io/ai-visual-bench/tests/steampunk-bee/gpt-6-astra/) · [源码](tests/steampunk-bee/gpt-6-astra/index.html) |


## 目录结构 / Layout

- `index.html` — 展示站（纯前端，无构建）
- `tests/<test>/models.json` — 每个测试的元数据（模型、耗时、文件路径、来源）
- `tests/steampunk-bee/<model>/index.html` — 原样保存的作品；`thumb.png` 为无头 Chromium 截取的封面

## 署名与许可 / Credits & License

- 蒸汽朋克蜜蜂灵感：[@NovaXCode](https://x.com/NovaXCode/status/2110223641111888338)。
- 代码：[MIT](LICENSE)。

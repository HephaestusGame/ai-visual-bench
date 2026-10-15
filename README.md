# AI 模型可视化生成测试汇总 · AI Visual Bench

收集不同 AI 模型在同一可视化生成任务上的作品，按测试分组，提供纯静态展示站。
*A collection of visual-generation tests comparing AI models, with a static, build-free gallery site.*

**展示站 / Live site:** https://hephaestusgame.github.io/ai-visual-bench/

## 测试列表 / Tests

### 1. 蒸汽朋克机械蜜蜂 / Steampunk Mechanical Bee

要求模型用**单个 HTML 文件**实现可交互的蒸汽朋克机械蜜蜂。灵感来源：[@NovaXCode 的帖子](https://x.com/NovaXCode/status/2110223641111888338)（2026-10-14，Gemini / argon 4 用单个 html 做出机械蜜蜂）。**原帖的原始提示词未公开**，因此本测试的提示词与原帖不一定一致。

| 模型 | 耗时 | 链接 |
|---|---|---|
| Gemini 4 Argon | 10 分钟 | [运行](https://hephaestusgame.github.io/ai-visual-bench/tests/steampunk-bee/gemini-4-argon/) · [源码](tests/steampunk-bee/gemini-4-argon/index.html) |
| Claude Opus 5.5 | 180 分钟 | [运行](https://hephaestusgame.github.io/ai-visual-bench/tests/steampunk-bee/claude-opus-5.5/) · [源码](tests/steampunk-bee/claude-opus-5.5/index.html) |
| GLM 5.3 Flash | 38 分钟 | [运行](https://hephaestusgame.github.io/ai-visual-bench/tests/steampunk-bee/glm-5.3-flash/) · [源码](tests/steampunk-bee/glm-5.3-flash/index.html) |
| Grok | 40 分钟 | [运行](https://hephaestusgame.github.io/ai-visual-bench/tests/steampunk-bee/grok/) · [源码](tests/steampunk-bee/grok/index.html) |
| V41 Flash | 12 分钟 | [运行](https://hephaestusgame.github.io/ai-visual-bench/tests/steampunk-bee/v41-flash/) · [源码](tests/steampunk-bee/v41-flash/index.html) · [README](tests/steampunk-bee/v41-flash/README.txt) |

### 2. 鹈鹕骑自行车 / Pelican Riding a Bicycle

经典 SVG 生成测试。作品来自 [scosman/pelicans_riding_bicycles](https://github.com/scosman/pelicans_riding_bicycles)，源仓库**未标注**各 SVG 对应的生成模型与耗时。

| 模型 | 耗时 | 链接 |
|---|---|---|
| 未标注 (Plate 1) | 未标注 | [SVG](tests/pelican-bicycle/pelican_riding_bicycle.svg) |
| 未标注 (Plate 2) | 未标注 | [SVG](tests/pelican-bicycle/pelican_riding_bicycle_2.svg) |
| 未标注 (Plate 3) | 未标注 | [SVG](tests/pelican-bicycle/pelican_riding_bicycle_3.svg) |
| 未标注 (Plate 4) | 未标注 | [SVG](tests/pelican-bicycle/pelican_riding_bicycle_4.svg) |
| 未标注 (Plate 5) | 未标注 | [SVG](tests/pelican-bicycle/pelican_riding_bicycle_5.svg) |
| 未标注 (Plate 6) | 未标注 | [SVG](tests/pelican-bicycle/pelican_riding_bicycle_6.svg) |
| 未标注 (Plate 7) | 未标注 | [SVG](tests/pelican-bicycle/pelican_riding_bicycle_7.svg) |

## 目录结构 / Layout

- `index.html` — 展示站（纯前端，无构建）
- `tests/<test>/models.json` — 每个测试的元数据（模型、耗时、文件路径、来源）
- `tests/steampunk-bee/<model>/index.html` — 原样保存的作品；`thumb.png` 为无头 Chromium 截取的封面

## 署名与许可 / Credits & License

- 鹈鹕作品 © 2024–present The Pelicans Riding Bicycles Enthusiasts Club (**PRBEC**) and contributors，来源 [scosman/pelicans_riding_bicycles](https://github.com/scosman/pelicans_riding_bicycles)，依 **PRBEC Permissive Pelican License v1.0** 使用，许可全文见 [tests/pelican-bicycle/LICENSE.md](tests/pelican-bicycle/LICENSE.md)。该目录不适用本仓库 MIT 许可。
- 蒸汽朋克蜜蜂灵感：[@NovaXCode](https://x.com/NovaXCode/status/2110223641111888338)。
- 其余代码：[MIT](LICENSE)。

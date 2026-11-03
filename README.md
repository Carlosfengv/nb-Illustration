# NB Illustration

![模型路由插画的深色与亮色对照](assets/nb-illustration-cover.svg)

把产品功能画成一个正在发生的界面动作。这个 Codex Skill 适合官网功能卡、Bento 网格、技术流程图和界面状态，也可以用来重绘现有插画。

每张图默认交付两份可编辑 SVG。深色版用炭灰底和近白高光，亮色版用纯白底和深石墨色线条。两版共用构图，保留低对比辅助轮廓，并用细边、内沿反光和双层软阴影突出交互焦点。

## 安装到 Codex

将此仓库的 `SKILL.md`、`agents/` 和 `assets/` 放进 Codex 的 `skills/nb-illustration/` 目录。macOS 或 Linux 可在仓库根目录执行以下命令。

```bash
nb_skill_dir="${CODEX_HOME:-$HOME/.codex}/skills/nb-illustration"
mkdir -p "$nb_skill_dir"
cp -R SKILL.md agents assets "$nb_skill_dir/"
```

## 用法

在 Codex 对话中调用 `$nb-illustration`，给出主题即可。也可以指定画幅、用途，或附上一份要重绘的 SVG。

> 用 $nb-illustration 画一张「模型灰度发布」的官网功能卡，横版 16:9。突出 5% 的流量进入新版本。

默认输出同一构图的 `*-dark.svg` 和 `*-light.svg`。批量生成时每张图各有一对。可以在请求中明确指定只输出一个主题。

## 仓库内容

- [`SKILL.md`](SKILL.md) 保存绘制规则、主题配色和交付检查。
- [`agents/openai.yaml`](agents/openai.yaml) 定义 Codex 中的显示名和示例提示词。
- [`assets/`](assets/) 保存 Figma 原稿参考和深浅主题样图。

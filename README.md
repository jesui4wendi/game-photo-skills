# Game Photo Mode

把拍过的地方，换成另一个游戏世界。

一个照片编辑 Skill。它先读懂照片里的主体、构图和物体，再重建材质、形状与光线。首版支持《我的世界》的方块像素风格，以及《赛博朋克2077》的场景材质与灯光。

[English](README.en.md) · [下载 Skill](packages/game-photo-mode-v1.0.0.zip) · [验收记录](evals/README.md) · [互动对照页](docs/index.html)

## 同一张照片，两种世界

| 原图 | Minecraft | Cyberpunk 2077 |
| --- | --- | --- |
| ![院落原图](docs/examples/courtyard-before.jpg) | ![方块院落](docs/examples/courtyard-minecraft.jpg) | ![工业材质院落](docs/examples/courtyard-cyberpunk.jpg) |
| ![街景人像原图](docs/examples/street-before.jpg) | ![方块街景人像](docs/examples/street-minecraft.jpg) | ![夜之城质感街景人像](docs/examples/street-cyberpunk.jpg) |

输入照片和输出均为 AI 生成的公开测试素材，不是私人照片，也不是游戏实际截图。输出确实以对应原图作为编辑输入；展示图经过缩小和 JPEG 压缩。完整提示与失败尝试见[验收记录](evals/README.md)。

下载仓库后可直接打开 `docs/index.html`，切换两种场景与预设，用分界线比较原图和编辑图，无需联网。

## 安装与使用

解压安装包，把 `game-photo-mode` 文件夹放入宿主的 Skills 目录。Codex 可放在 `~/.codex/skills/`，设置了 `CODEX_HOME` 时使用其 `skills/` 目录。重新加载 Skills 后上传照片，或提供本地图片路径：

```text
$game-photo-mode 把这张照片变成《我的世界》里的场景，保留人物位置和构图。
```

```text
$game-photo-mode 调整成《赛博朋克2077》的游戏画面质感，保留人脸、衣服颜色和原来的时间。
```

需要能接收原图的图片编辑工具。在 Codex 中优先使用内置图片工具，无需为这个 Skill 配置 API Key。Skill 本身只有说明和参考资料；其他宿主需要提供自己的图片编辑能力，模型费用和可用性由宿主决定。只有文字能力的宿主会返回可用提示，不能实际改图。

## 两种预设怎么工作

**Minecraft**：按粗方块尺度重建建筑，使用像素化的块面材质、方块树和玩家形人物。默认是熟悉的原版贴图与简洁光照风格，避免自动变成写实光影包。人物通过发型、肤色、衣服颜色和姿势保留辨识度，方块脸不能保证精确人脸相似。自行车等原版没有的物体会变成保留轮廓的方块道具，并不声称它们是原版物品。

**Cyberpunk 2077**：根据照片选择设计语言。普通院落保留白天，重建成粗粝的混凝土、维修金属和管线；雨后街景用实际灯源控制冷暖色和地面反射。首版样例覆盖 Entropism 和少量 Kitsch 元素，其他设计语言仅提供选择指导。它不会为了“赛博朋克”把每张照片都改成紫色霓虹夜景。

两种预设都会保留原图，生成新文件，并检查构图、主体、几何、材质和光线。遇到明显偏差会针对问题修正，而不是只重复游戏名称。[编辑流程](skills/game-photo-mode/SKILL.md)与[检查条件](skills/game-photo-mode/references/review.md)都可以直接阅读。

## 这次验证了什么

两类输入：静物院落、包含人物的雨后街景。共七次实际图像输入编辑，保留四张最终图和三张未采用尝试。Minecraft 修正了建筑尺度及反射光影混入；Cyberpunk 修正了院落材质与照明的方向。Skill 格式、内部引用、独立安装包均做了检查。

这是有限样例上的目测验证，不是自动相似度认证，也不保证下一次生成与游戏画面完全相同。照片内容与模型都会影响结果；很复杂的手部、文字、细小道具、多人和近距离人脸尚未覆盖。本项目不导出地图、模型、材质包或可玩场景。

## 扩展

已有的 [Source Engine Photo](https://github.com/jesui4wendi/source-engine-photo-skill) 保持独立。[后续游戏方向](docs/research/next-games.md)列出了下一批候选；它们没有被算作已支持功能。

新增预设应带有官方视觉依据、至少两类真实图像输入编辑、失败记录与结果图。欢迎提交能公开使用的失败样例：原图、结果、想保留的内容、实际偏差。不要只增加一段“某游戏风格”的提示就宣布支持。

## 许可证

Skill、文档和本项目生成的示例采用 [MIT](LICENSE)。游戏名称用于说明目标视觉语言；本项目不隶属 Mojang、Microsoft 或 CD PROJEKT RED，不包含提取的游戏资源。第三方游戏素材与商标权不由本许可证授予。

# ReelCast · 复刻原视频

给 Codex 一段短片，它可以找出角色抬头、伸手或碰到对方的那一帧，并告诉你在第几秒。再给它一张角色设定图，就可以生成对应的角色关键帧，左边看原片，右边看自己的角色。

## 安装到一个 Codex 项目

解压下载包，把整个 `skills/character-reel` 文件夹复制到你项目里的 `.agents/skills/` 下。完成后应能看到 `.agents/skills/character-reel/SKILL.md`。在这个项目里打开新的 Codex 聊天。

拆帧需要 Python 3.9+、Pillow 和支持 `-fps_mode` 的 FFmpeg（含 ffprobe）。在运行脚本的 Python 环境中用 `python3 -m pip install Pillow` 安装 Pillow。角色生图还需要当前聊天可以使用支持参考图的生图工具。

## 第一次试用

上传一段短片，输入：

```text
$character-reel 帮我拆一下这段视频。找出几个关键动作，给我原帧和时间码。
```

再附上你的角色图，输入：

```text
用我的角色画出这些动作。表情跟着剧情变化，外形按设定图。把每张图和对应的原帧放在一起给我看。
```

也可以只改一张，例如“第三张伸手太早，应该刚刚碰到对方，重画这张”。满意后可以要一段即梦提示词。是否上传即梦、何时开始生成，由你决定。

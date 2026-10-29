<div align="center">

# Suno Songwriting

### 从一句灵感，到一首歌的歌词与声音方向。

为 AI 助手准备的歌词与配置创作技能：把故事、情绪和音乐要求，整理成可复制的歌词、Styles 与 Suno 设置建议。<br />
以中文创作为重点，支持其他歌词语言；完整写歌、局部改词和纯器乐规划均可独立开始。

![Format](https://img.shields.io/badge/entry-SKILL.md-6366F1?style=flat-square)
![Output](https://img.shields.io/badge/output-lyrics_%26_styles-F59E0B?style=flat-square)
![Workflow](https://img.shields.io/badge/workflow-text_only-334155?style=flat-square)

**[下载技能](https://github.com/Eileenes/suno-songwriting/archive/refs/heads/main.zip)** · **[快速开始](#quick-start)** · **[使用示例](#examples)** · **[创作流程](SKILL.md)** · **[编曲指南](references/arrangement.md)**

</div>

---

## 能做什么

| 歌词与故事 | 声音与编曲 | Suno 文本与配置 |
| --- | --- | --- |
| 从灵感、生活经历或旧歌词创作新歌 | 按目标时长、BPM 和小节数分配段落 | 分别输出 Title、Lyrics、Styles、Exclude |
| 检查副歌韵脚、自然语义与换气空间 | 为前奏、器乐 solo 和渐弱尾奏留出空间 | 根据实际界面给出设置建议与试听起点 |
| 保留已认可部分，只修改指定段落 | 为主旋律、对答、和声、节奏与低音分配职责 | 区分界面控件、条件选项与音乐目标 |

这是一个由 AI 助手读取执行的文本技能，**不内置音频模型，不登录 Suno，也不自动生成或发布歌曲**。实际音频生成需要自行在 Suno 中操作；账号功能与额度由 Suno 提供。

<a id="quick-start"></a>

## 快速开始

### 1. 下载并读取技能

下载上方 ZIP 并解压，或者克隆仓库：

```bash
git clone https://github.com/Eileenes/suno-songwriting.git
cd suno-songwriting
```

无需安装即可让能读取本地文件的助手执行：

> 请读取这个仓库的 `SKILL.md`，写一首下班独自回家的中文歌，疲惫但温暖，偏独立流行。给我完整歌词、Styles 和 Suno 配置建议。

### 2. 长期使用时，安装整个技能目录

以 Codex 的默认用户技能目录为例，在仓库根目录执行：

```bash
mkdir -p "$HOME/.codex/skills"
if [ -e "$HOME/.codex/skills/suno-songwriting" ]; then
  echo "已有 suno-songwriting，请先备份并比较版本"
else
  mkdir "$HOME/.codex/skills/suno-songwriting"
  cp SKILL.md "$HOME/.codex/skills/suno-songwriting/"
  cp -R agents references "$HOME/.codex/skills/suno-songwriting/"
fi
```

如果设置了自定义 `CODEX_HOME`，请使用其下的 `skills` 目录。其他宿主按各自的技能目录规则安装。保留 `SKILL.md`、`agents/` 与 `references/` 的相对位置；未识别新技能时，可以重新打开会话或直接提供入口文件路径。

### 3. 说清目标，分别复制输出字段

在支持技能调用的会话中输入 `$suno-songwriting`，再说明主题、语言、风格、人声或目标时长。不必一次填满所有条件，技能也可以从一句灵感开始。

将交付中的歌词、Styles 和 Exclude 分别复制到对应输入框；**不要把整份技能说明或配置解释贴进歌词框**。纯音乐任务省略演唱歌词。

<a id="examples"></a>

## 使用示例

### 完整写歌

```text
使用 $suno-songwriting，写一首中文流行歌曲，约 2 分 30 秒。
女声有穿透力、节奏较快，主题是离开熟悉的城市重新开始。
歌词要押韵，开头渐进进入，结尾渐弱，中间安排弦乐 solo，
让小提琴、中提琴和大提琴有不同声部的呼应。
```

### 只改副歌

```text
使用 $suno-songwriting，保留现有主歌和音乐风格，只改副歌。
副歌主要押 ang 韵，不要为了押韵改变意思，核心句保留“绿灯亮了”。
下面是当前版本：……
```

### 规划纯器乐

```text
使用 $suno-songwriting，做一个约 60 秒的纯器乐片段，以大提琴为主。
不要演唱和哼唱，前半段克制，后半段展开，给我 Styles 与设置建议。
```

延续旧作时，请同时提供当前歌词、已认可的风格和可用参考素材。无法读取或试听的素材不会被视为已分析。

## 从灵感到试听

**创作需求 → 段落与编曲预算 → 歌词与 Styles → 配置建议 → 自行生成 → 根据试听局部调整**

| 交付 | 包含什么 |
| --- | --- |
| 创作方向与 Title | 简短的主题、情绪、声音方向及推荐歌名 |
| Lyrics | 写全重复段落的歌词；必要的简短结构标签 |
| Styles 与 Exclude | 默认英文风格词及中文解释；无需排除时留空 |
| 配置建议 | 字段、建议值和理由；未核实或不适用的选项单独标注 |
| 编曲预算 | 有时长、过渡或 solo 要求时提供段落、小节或秒数规划 |
| 试听调整 | 最多三条具体调整建议；优先一次改变一个变量 |

每个待复制字段单独成块。局部修改只返回受影响部分，保留已经认可的内容。[查看完整交付规则 →](SKILL.md)

## 使用条件与当前限制

| 场景 | 需要什么 | 当前边界 |
| --- | --- | --- |
| 创作歌词与风格 | 能读取 Markdown 的 AI 助手 | 仓库提供工作流与参考资料，没有独立应用或音频引擎 |
| 核实 Suno 控件 | 实际账号界面；必要时访问官方文档 | 控件随版本变化；无法核实时标注条件，不假设付费权限 |
| 延续旧作风格 | 已有歌词、风格描述或宿主可读取的素材 | 文字提示不能保证锁定同一声音或保留原旋律 |
| 精确时长与音频效果 | 生成结果与后续音频编辑工具 | BPM、时长、solo、渐弱和标签都是引导，不保证逐秒执行 |

- **时长先规划再写词**：例如 128 BPM、4/4 下，80 小节约 150 秒；这是预算，不是生成时长保证。
- **人声和配器服从需求**：女声、快节奏与弦乐不是每首歌的默认选择。
- **设置值是试听起点**：不将滑块数值说成官方最佳设置，不把 BPM、调性和乐器当成必有的独立按钮。
- **生成质量需要试听检查**：仓库不附带自动测试或已验证的 Suno 音频成品，不能据此保证押韵、演唱或生成效果。

## 文档与维护

| 文档 | 内容 |
| --- | --- |
| [技能入口](SKILL.md) | 需求提取、歌词创作、声音方向与交付检查 |
| [时长、押韵与配器](references/arrangement.md) | 小节预算、前奏尾奏、器乐职责与中文韵脚 |
| [Suno 字段与核实方法](references/suno-fields.md) | 字段映射、版本边界与官方查证入口 |
| [技能展示配置](agents/openai.yaml) | 展示名称、短介绍与默认调用提示 |

<details>
<summary><b>目录结构</b></summary>

```text
suno-songwriting/
├── README.md                 # 介绍、安装与使用示例
├── SKILL.md                  # 创作工作流入口
├── agents/openai.yaml        # 展示与调用配置
└── references/
    ├── arrangement.md        # 编曲预算与押韵
    └── suno-fields.md        # 字段映射与官方查证入口
```

</details>

遇到问题可[提交 Issue](https://github.com/Eileenes/suno-songwriting/issues)，说明宿主环境、使用目标与实际结果；提交示例前请移除私人歌词或未公开素材。

## 来源与授权

本项目与 Suno 无隶属关系；Suno 的名称、产品功能和使用条款以其官方说明为准。仓库通过字段指南链接相关官方资料，不提供账号、API 额度或音乐素材授权。

**仓库当前未提供 LICENSE 文件**，不应据此宣称采用 MIT 等开源许可证；使用和再分发权限需向作者确认。参考作品与输入素材的权利由其各自权利人保留。

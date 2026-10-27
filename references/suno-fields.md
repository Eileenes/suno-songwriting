# Suno 字段与核实方法

输出完整配置时读取。实际账号界面决定哪些字段可用；以下是字段含义与建议方法，不是所有版本都有的固定 UI。

## 当前事实与创作建议分开

- 用户给出截图、模型或参数时，优先使用已知界面信息，不为了套模板改用其他版本。
- 需要判断当前模型、功能、费用或控件可用性时，查阅相关官方文档。当前会话已经查证且没有变化疑点的信息可以复用，不必每次重新研究。
- 官方页面互相冲突时，结合实际界面与更新时间说明不确定性。无法联网也应继续完成创作，未核实项标“若界面提供”。
- 不以第三方 Suno API 的参数、枚举或数值范围冒充官网控件。不要凭记忆宣称字段字符上限。
- 给参数数值时明确是本曲的试听起点，不是官方推荐或结果保证。

| 字段 | 建议方式 |
| --- | --- |
| Mode | 能粘贴完整歌词的 Custom / Advanced，以实际名称为准。 |
| Model | 按账号实际可选模型及稳定/探索目标选择；未知时给原则。不要把某个版本写死。 |
| Lyrics 输入 | 自填完整歌词；若有 Manual 则选用。生成用的指令本身不粘进歌词框。 |
| Instrumental | 有演唱则关闭；纯音乐开启。中间有 solo 仍保持关闭。 |
| Vocal Gender | 按用户要求选择实际选项，与 Styles 一致。未知偏好可保留默认。 |
| Weirdness | 在实际范围内给具体起点：表示更稳妥还是更不可预测，不表示音质高低。 |
| Style Influence | 给具体起点，表示希望多贴近 Styles；不是音频相似度。 |
| Exclude / Exclude Styles | 只排除确实不需要的声音，无需求留空；不得排除正向风格要求。 |
| Audio Influence | 存在相关参考素材且界面出现时才推荐；否则“不适用”。 |
| Voices / Style Persona | 需要延续旧作声音或风格时，可选择用户已有素材；没有素材则跳过。文字描述不能保证锁定同一声音。 |
| Variety | 若提供，按是否允许调整风格提示词决定；希望保留 Styles 时可建议 0。不是 Weirdness 的另一个名字。 |
| Max Mode | 若提供，根据长度、连贯性与额外消耗推荐；先试方向时不必默认开启。 |
| Duration | 只有实际存在时才作为设置项；否则明确为创作目标，靠篇幅与编曲引导。 |
| Title | 一个推荐歌名，可附两个备选。 |

BPM、调性、拍号与乐器编排通常是写入 Styles 的音乐目标；没有界面证据时，不把它们列为独立按钮。

## 官方查证入口

- [自填歌词 / Custom](https://help.suno.com/en/articles/2415873)
- [Creative Sliders](https://help.suno.com/en/articles/6141377)
- [Exclude](https://help.suno.com/en/articles/3161921)
- [Vocal Gender](https://help.suno.com/en/articles/10153473)
- [v6 FAQ：模型、Variety、Max Mode 的版本性说明](https://help.suno.com/en/articles/13924481)
- [Voices / Style Personas](https://help.suno.com/en/articles/11362433)
- [Making Music：查找后续更新](https://help.suno.com/en/categories/550017)

引用当前事实时给相关页面链接，放在可复制内容之外。不要把用户的私人歌词、未公开作品链接或个人故事放进搜索查询；一般查功能名称即可。

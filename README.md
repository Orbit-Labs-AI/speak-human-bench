# 说人话测评里用到的 7 段提示词（speak-human-bench）

这是 Orbit Labs “说人话”测评里实际用过的 7 段提示词。为了测评口径一致，每个 Skill 都压成了一段 200–600 字的系统提示，部分内容经过改写，所以和原仓库里完整的 Skill 不完全一样。每个文件用它在测评里的名字命名，提示词正文一字未改。

| 排名 | 文件 | 说明 | 综合人话分 | 来源 |
| ---: | --- | --- | ---: | --- |
| 1 | [banned-words-zh](banned-words-zh.md) | 套话黑名单 | 75 | 词表取自 Humanizer-zh、stop-slop，中文部分自写 |
| 2 | [anti-slop](anti-slop.md) | 负面清单 + 五维自检 | 75 | 改自 FeedHive/ai-slop-detector、stop-slop |
| 3 | [humanizer](humanizer.md) | 去 AI 味改写 | 74 | 改自 Humanizer-zh（上游 blader/humanizer） |
| 4 | [grammar-completion](grammar-completion.md) | 语法补全 | 73 | Orbit Labs 自写 |
| 5 | [additive-detail](additive-detail.md) | 具体细节注入 | 70 | Orbit Labs 自写，依据 tramstop-skill |
| 6 | baseline | 不加任何提示 | 69 | — |
| 7 | [ste100-zh](ste100-zh.md) | 受控中文 | 63 | 据 ASD-STE100 标准改写 |
| 8 | [ste100-en](ste100-en.md) | 英文受控写作 | 57 | 据 ASD-STE100 标准改写 |

综合人话分：6 个模型，短文写作和科普长文各占一半，满分 100。评分标准和测评方法见 Orbit Labs 公众号的“说人话”系列文章。

用法：打开对应的文件，把分隔线下面的整段贴进对话或系统提示词，再让模型写作。

我们自己写的写作 Skill 是 [流水句（flow-zh）](https://github.com/Orbit-Labs-AI/flow-zh)，它是照着评分标准写的，所以没有放进这张排名表。

## 许可证

anti-slop、banned-words-zh 和 humanizer 改编自 MIT 许可的仓库，许可证原文见 [THIRD-PARTY-LICENSES.md](THIRD-PARTY-LICENSES.md)。ste100-zh 和 ste100-en 是我们按 ASD-STE100 的公开介绍自己写的，不含标准原文；ASD-STE100 归 ASD 所有。

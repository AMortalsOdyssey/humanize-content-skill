# 文案规则引用：blader/humanizer

这是文案类规则下的一个外部引用，不是本仓库内置规则，也不是默认文风。

## 来源

- 仓库：https://github.com/blader/humanizer
- 规则文件：https://github.com/blader/humanizer/blob/main/SKILL.md
- 参考基础：https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing

## 适用场景

只在用户明确要求以下内容时参考：

- `humanizer`。
- `blader/humanizer`。
- 英文 Humanizer。
- 按 Wikipedia “Signs of AI writing” 体系清理 AI 写作痕迹。
- 需要 voice calibration，用用户样本文风校准节奏、词汇和个人表达习惯。

适合处理：

- 英文或中英混写文本里的 AI 痕迹。
- 夸大意义、宣传腔、模糊归因、三段式、同义词循环、破折号滥用等模式。
- 需要先识别 AI writing patterns，再做第二轮 residual audit 的文本。
- 用户给了 2-3 段个人样文，希望按本人节奏重写。

不要用于：

- 中文优先、需要保留中文互联网语境的内容；这类优先看 `shuorenhua` 或 `humanizer-zh`。
- 需要 Anthropic Blog 式结构和可信度的产品 / 工程 / 方法论文章。
- 需要蒸馏某个公众人物或作者长期思维方式的任务；这类优先看 `nuwa-skill`。

## 使用边界

本仓库不 vendoring 这个外部仓库，不保存其完整内容。需要精确使用时，访问上面的 GitHub 链接读取原规则；只需要知道它存在时，把它作为文案类规则列表中的一个外部参考即可。

---
name: humanize-content
description: 去 AI 味内容规则库。用于创建、改写或审阅文案、文章、教程、小红书笔记、视频脚本、图片提示词、海报卡片和其他公开内容；当用户要求“去 AI 味”“写得像真人”“活人感”“按 anthropic-like / Khazix 等规则写”“让内容更具体可信”时使用。规则按三类组织：文案类、视频类、图片类。
---

# Humanize Content

这个 skill 是一个内容规则库，不是某一个固定文风。目标是让输出少一点模板感，多一点真实处境、具体判断和可验证细节。

## 目录结构

- `rules/copywriting/`：文案类规则，包含文章、教程、产品文案、小红书笔记、长文写作等。
- `rules/video/`：视频类规则，包含口播、分镜、脚本、短视频和讲解视频。
- `rules/image/`：图片类规则，包含海报、封面、小红书卡片、图片提示词和视觉概念。

## 文案类规则速览

- `rules/copywriting/anthropic-like/rules.md`：默认可信结构规则，适合 AI、产品、工程、协作、教程、方法论和需要证据密度的中文内容。
- `rules/copywriting/khazix-writer/reference.md`：外部个人风格引用，适合用户明确要求“数字生命卡兹克 / khazix-writer”时使用。
- `rules/copywriting/shuorenhua/reference.md`：外部中文优先“说人话”引用，适合通用中文去 AI 味、日常表达、状态同步、README、论坛帖和产品说明。
- `rules/copywriting/humanizer-zh/reference.md`：外部 Humanizer 中文版引用，适合用户明确要求 Humanizer-zh 或按 blader/humanizer 中文翻译版清理 AI 写作痕迹。
- `rules/copywriting/humanizer/reference.md`：外部 blader/humanizer 引用，适合英文或中英混写文本的 AI writing pattern 清理，以及需要 voice calibration 的改写。
- `rules/copywriting/nuwa-skill/reference.md`：外部风格蒸馏引用，适合从公开材料中提取作者表达 DNA、心智模型和可复用个人风格规则。

## 使用流程

1. 先判断内容类型：
   - 文案、文章、教程、产品说明、小红书笔记：读取 `rules/copywriting/` 下对应规则。
   - 视频脚本、分镜、口播、讲解视频：读取 `rules/video/general/rules.md`。
   - 图片提示词、海报、封面、卡片：读取 `rules/image/general/rules.md`。

2. 再选择具体规则：
   - 用户点名某个规则时，读取该规则文件夹。
   - 未点名且内容是 AI、产品、工程、协作、教程、方法论时，默认使用 `rules/copywriting/anthropic-like/rules.md`。
   - 未点名且只是要求中文“去 AI 味”“说人话”“自然一点”时，优先参考 `rules/copywriting/shuorenhua/reference.md`，必要时再结合 `anthropic-like` 的可信结构。
   - 用户点名 `khazix-writer` 或“数字生命卡兹克风格”时，只读取 `rules/copywriting/khazix-writer/reference.md`，按其中链接决定是否需要查看外部仓库。
   - 用户点名 `Humanizer-zh`、`humanizer-zh`、`humanizer`、`blader/humanizer`、`shuorenhua`、`说人话`、`nuwa-skill` 或“女娲”时，读取对应 `reference.md`，按其中链接决定是否需要查看外部仓库。

3. 写之前先做一个事实盘点：
   - 谁在说话？他/她处在什么真实角色里？
   - 发生了什么变化、失败或新机会？
   - 有哪些具体证据：文件、命令、截图、日志、流程、指标、例子？
   - 哪些边界、风险或不确定性应该明说？
   - 读者看完后能做什么？

4. 改写时优先替换这些问题：
   - 把抽象判断换成具体场景。
   - 把宏大形容词换成可观察结果。
   - 把“我认为很重要”换成“失败会在哪里出现”。
   - 把口号式结尾换成检查清单、问题或下一步动作。

5. 输出前做 AI 味检查：
   - 删除无证据的“赋能、重塑、革命性、极致、全新范式、无限可能”。
   - 避免空泛三连、金句腔、过度排比和“不仅是 X，更是 Y”。
   - 保留人味：真实犹豫、踩坑、取舍、判断依据和不完美节奏。
   - 面向公开内容时，抽象掉私有路径、内部域名、账号、token、secret 和部署细节。

## 输出方式

用户要成稿时，直接给最终稿。只有当说明规则有助于继续编辑时，再补一句“使用了哪个规则”。

用户要审稿时，先指出最影响可信度的问题，再给局部改写，不要写成长篇旁白。

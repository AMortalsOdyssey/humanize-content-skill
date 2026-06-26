# Content Type: khazix-writer

Use this adapter only when the user explicitly asks for the Khazix / 数字生命卡兹克 voice, a personal WeChat long-form article, or a similar "个人公众号长文" format. Do not use it for short Xiaohongshu notes, tweets, posters, or generic humanization requests.

## Source

The third-party source is mounted as a vendor submodule:

`vendor/copywriting/khazix-skills/khazix-writer/SKILL.md`

Because the vendor repository contains multiple skills, first confirm that the requested output is long-form writing. Then read only the `khazix-writer` files needed for the task:

- `vendor/copywriting/khazix-skills/khazix-writer/SKILL.md`
- `vendor/copywriting/khazix-skills/khazix-writer/references/content_methodology.md` when the structure or article method matters.
- `vendor/copywriting/khazix-skills/khazix-writer/references/style_examples.md` when voice matching matters.

## Boundary

Treat `khazix-writer` as a third-party reference voice, not the default voice of `humanize-content`. The default `humanize-content` behavior is to make content more grounded, specific, and human; it should not automatically imitate a named creator.

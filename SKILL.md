---
name: humanize-content
description: Humanize Chinese or bilingual content so it feels written by a real person instead of a generic AI. Use when Codex needs to create, rewrite, or critique copy, blog posts, tutorials, product docs, Xiaohongshu notes, video scripts, image prompts, poster/card concepts, or other public-facing content; when the user asks to remove AI smell, add human voice, follow a named style rule such as blog-of-anthropic, or make content more specific, grounded, and believable.
---

# Humanize Content

## Overview

Use this skill to turn vague, polished, AI-like content into grounded work with a human point of view, concrete evidence, and medium-aware structure. Prefer specificity over decoration: real situations, constraints, roles, artifacts, checks, and tradeoffs should carry the writing.

## Workflow

1. Identify the medium before rewriting:
   - Text, article, tutorial, docs, social copy: read `references/media-text.md`.
   - Video script, storyboard, voiceover, shot plan: read `references/media-video.md`.
   - Image prompt, poster, Xiaohongshu card, visual concept: read `references/media-image.md`.

2. Select a style rule:
   - If the user names a style rule, load that file from `references/style-rules/`.
   - If no rule is named and the task is about AI, product work, engineering, collaboration, or tutorials, use `references/style-rules/blog-of-anthropic.md`.
   - If no rule fits, still apply the medium rules and use the source draft's audience and tone.

3. Build a small truth inventory before drafting:
   - Who is speaking, and from what lived role?
   - What changed, failed, or became newly possible?
   - What concrete artifacts, commands, screenshots, files, metrics, tools, or examples can prove it?
   - What boundaries or caveats should be visible?
   - What should the reader be able to do next?

4. Rewrite from mechanism, not adjectives:
   - Replace generic claims with a before/after state, a role, and a workflow.
   - Replace broad value words with concrete outcomes or verification.
   - Keep confident judgment, but show the basis for it.
   - Ask only if missing facts would change the substance; otherwise make conservative assumptions.

5. Run an AI-smell audit:
   - Remove inflated words such as "赋能", "重塑", "革命性", "极致", "全新范式" unless the source evidence truly warrants them.
   - Avoid empty three-part lists, quote-like slogans, and "不仅是 X, 更是 Y" structures.
   - Vary sentence length. Let some sentences be plain.
   - Preserve useful messiness: friction, uncertainty, false starts, and decision criteria.
   - For public output, abstract private paths, internal domains, accounts, tokens, secrets, and deployment details.

## Output

When the user asks for rewritten content, provide the final content first. Add a short note about the applied rule only when it helps the user keep editing. Do not narrate every internal decision.

When the user asks for critique, return the highest-signal issues first:

- Where the text still feels generic.
- Which missing proof or artifact would make it more credible.
- Which structural change would create more human rhythm.
- A compact rewrite of the weakest section.

## Examples

Read `references/examples.md` when the user asks for examples, asks what this skill should produce, or requests a Xiaohongshu-style rewrite similar to prior work.

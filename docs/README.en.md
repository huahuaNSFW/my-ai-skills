# Style Anchor · 文锚

[**中文版**](README.zh-CN.md)　|　[**English**](README.en.md)　|　[Home](../README.md)

**A constraint patch for an existing style prompt.**

Your own style prompt defines the work's voice, character, and expression. Style Anchor adds execution boundaries for ambiguity, conflicting constraints, and stylistic overreach while preserving your aesthetic.

Input: **your existing style prompt + an optional creative task**. With only the prompt, it returns a minimal appendable patch. With a task, it applies the patch and delivers the work. It preserves the source prompt and provides a merged version only when explicitly requested.

## Let your AI read the repository

Send this to an AI with repository or web-reading access, together with your own style prompt:

```text
Read this repository: https://github.com/huahuaNSFW/my-ai-skills
Start with README.md, then skills/style-anchor/SKILL.md,
then read skills/style-anchor/references/rules.en.md in full.

Load Style Anchor as a constraint patch for my existing style prompt.
Preserve my aesthetic, voice, and explicit exclusions.
Append only constraints that address actual execution issues.
Without a creative task, return only an appendable patch.
With a task, deliver the resulting work.
If a file cannot be read, name the missing file rather than claiming it is loaded.

[My existing style prompt]
Paste your own existing style prompt here.

[Current creative task — optional]
Describe the task here; omit this section if you only want the patch.
```

The AI should confirm that the source prompt is supplied and read the rules through the skill entry point. If given only a repository link, it should request the source prompt.

## How an AI should use this repository

1. Read the skill entry point and one complete language version of the rules.
2. Treat the user's original prompt as the style configuration and preserve its text.
3. Identify actual ambiguity, conflicts, overreach, or content loss; add only relevant constraints.
4. Let the original aesthetic and the user's explicit current requirements take priority over patch defaults.
5. Return a patch or the creative result as requested. Do not default to inventing a new style.
6. Request file contents if reading fails. Users of tools without browsing can paste the entry point and English rules in full.

## Example: preserve ornament, constrain accumulation

**Original prompt**
> Write ornately, with a classical feel and abundant imagery.

**Style Anchor addition**
> Preserve the ornate, classical voice. Connect imagery to the scene or emotion; trim successive images that add neither meaning nor rhythmic value. Clearly convey information required by this task, without requiring imagery in every sentence.

This patch addresses this example's execution risks. Restrained, conversational, or fragmented styles need constraints derived from their own source prompts.

## Files

| File | Purpose |
|---|---|
| [SKILL.md](../skills/style-anchor/SKILL.md) | AI entry point and scope |
| [English rules](../skills/style-anchor/references/rules.en.md) | Complete patch rules and execution behavior |
| [中文规则](../skills/style-anchor/references/rules.zh-CN.md) | Semantically equivalent Chinese rules |
| [Display metadata](../skills/style-anchor/agents/openai.yaml) | Skill name and invocation metadata for compatible tools |

Repository: `my-ai-skills`. Skill: **Style Anchor · 文锚**. Identifier: `style-anchor`. Reading and applying the files is sufficient to use the rules in a conversation. Persistent installation depends on the AI tool's skill mechanism. Uploading to GitHub does not automatically install or permanently configure an AI.

## Evidence and evaluation

Inspired by [Matthew Ritch's style prompt experiment](https://matthewritch.com/blog/2026/09/08/Mannered-Prose-Style-Prompts/). These patch rules are practical deductions. Compare the original prompt and the patched prompt on identical tasks, assessing style fidelity, constraint adherence, and completeness. Retest across models, languages, and genres.

**Contact: QQ: 2365673057**

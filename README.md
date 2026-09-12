# 我的 AI 技能库 / My AI Skills

## 中文：从这里开始

这里保存可复用的 AI 技能。目前包含 **风格提示词设计（style-prompt-design）**：把“自然、简洁、专业”等偏好转成具体写作规则，提供改写示例和验收方法。

### 1. 在当前 ChatGPT 中使用（最方便）

此技能已经安装到你的个人技能目录：
[打开「风格提示词设计」](https://chatgpt.com/skills?skill_id=6aa4d6b13b708191a6c3fdde23e200ed)

在聊天中选择该技能，或发送：

> 请用 $style-prompt-design 帮我设计一套中文写作风格提示词。用途：知识分享。读者：普通读者。偏好：自然、简洁、具体。请给我可复制的提示词、两组改写示例，以及验收方法。

需要双语时，加一句：

> 请分别给出中文和英文版本，保持两版规则含义一致。

上述技能目录链接属于仓库所有者的个人安装。其他读者需要在自己的支持技能的工具中安装，或使用下面的复制方法。若刚保存的版本暂未显示，可刷新技能页面。

### 2. 在其他 AI 聊天工具中使用（无需写代码）

1. 打开 [技能文件 SKILL.md](skills/style-prompt-design/SKILL.md)。
2. 点击文件页的 **Raw** 查看原文，复制全文。
3. 粘贴到你的 AI 对话中，再加上：“请按上面的规则，帮我设计风格提示词。我的用途和偏好如下：……”。
4. 将生成的成品提示词保存到你的风格 AI 的自定义指令或系统提示词中；如果工具没有对应入口，每次对话开头粘贴即可。
5. 用几篇真实内容试用，根据结果调整。

复制使用会把技能作为本次对话的指令提供给 AI；GitHub 中存有文件不会让其他工具自动加载它。不同工具的正式安装方式可能不同。

### 3. 三种常用请求

**从零创建**
> 请用 $style-prompt-design 为我的产品介绍设计风格规则：面向新用户，语气友好，少用形容词，保留功能限制。给我中英文版本。

**优化已有提示词**
> 请用 $style-prompt-design 优化下面的风格提示词，保留我的硬性要求，合并重复内容，指出冲突，并给出改进版：[粘贴原提示词]。

**从样文提取规则**
> 请用 $style-prompt-design 分析下面的样文，提取措辞、长度、语气、结构和修辞规则。区分明确证据与推测，并用不同主题给出改写示例：[粘贴样文]。

### 4. 怎么判断有效

用相同任务比较原提示词和新提示词，检查：风格是否更符合偏好、事实和必要条件是否完整、禁用项是否出现、是否形成新的套话。更换模型或语言后重新试用。文件格式已校验；各模型上的写作效果需要实际验证。

## English: Start here

This repository stores reusable AI skills. **Style Prompt Design** turns preferences such as natural, concise, and professional into concrete writing instructions, calibration examples, and evaluation criteria.

### 1. Use the installed skill in ChatGPT

The repository owner has a personal installation:
[Open Style Prompt Design](https://chatgpt.com/skills?skill_id=6aa4d6b13b708191a6c3fdde23e200ed).

Select it in chat or send:

> Use $style-prompt-design to create a writing-style prompt for educational posts aimed at general readers. Keep the style natural, concise, and concrete. Provide a ready-to-copy prompt, two before-and-after examples, and an evaluation method.

For bilingual output, add:

> Provide Chinese and English versions with equivalent rules.

The installation link belongs to the repository owner. Other readers should install the skill in their own compatible tool or use the copy-and-paste method below. Refresh the Skills page if a newly saved version has not appeared.

### 2. Use another AI tool without coding

1. Open [SKILL.md](skills/style-prompt-design/SKILL.md).
2. Select **Raw** and copy the complete text.
3. Paste it into your AI conversation and add: “Follow these instructions to design a style prompt. My audience, task, and preferences are…”.
4. Save the resulting prompt in your writing AI's custom instructions or system prompt. If the tool has no such setting, paste it at the beginning of each conversation.
5. Try real writing tasks and refine the result.

Pasting supplies instructions for that conversation. Storing files on GitHub does not automatically load them into another tool. Formal installation methods vary by tool.

### 3. Common requests

**Create**
> Use $style-prompt-design to create Chinese and English style rules for product descriptions aimed at new users. Use a friendly tone, reduce empty adjectives, and preserve limitations.

**Improve**
> Use $style-prompt-design to improve this style prompt. Preserve my hard constraints, consolidate repetition, identify conflicts, and provide a revised version: [paste prompt].

**Learn from a sample**
> Use $style-prompt-design to extract vocabulary, length, tone, structure, and rhetoric rules from this sample. Separate observations from inferences and demonstrate the rules on another topic: [paste sample].

### 4. Evaluate

Compare the original and revised prompts on the same tasks. Check stylistic fit, factual completeness, conditions, excluded expressions, and new catchphrases. Retest after changing models or languages. File format has been validated; writing effectiveness requires real model testing.

## 文件 / Files

- [SKILL.md](skills/style-prompt-design/SKILL.md): 中英文技能规则 / Chinese and English skill instructions.
- [openai.yaml](skills/style-prompt-design/agents/openai.yaml): 技能显示信息 / Skill display metadata.

## 来源 / Source

Inspired by [Matthew Ritch's experiment on style prompts](https://matthewritch.com/blog/2026/09/08/Mannered-Prose-Style-Prompts/). The workflow is a practical deduction; it has not been established as universally effective across models.

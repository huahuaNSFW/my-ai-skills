---
name: style-anchor
description: "文锚：给用户已有创作风格提示词附加最小执行约束补丁，保留原审美并处理含糊、冲突和过度执行。Style Anchor adds a minimal constraint patch to an existing creative style prompt. Use when the user asks to load or apply this patch; requires an existing style prompt."
---

# 文锚 · Style Anchor

定位：已有风格提示词的执行约束层。输入为用户原风格提示词，以及可选的创作任务和材料。保留原文，按需追加约束；默认交付补丁，有创作任务时交付应用补丁后的作品。缺少原提示词时先索取。不要默认从零设计、整篇重写提示词或提取一套新审美。

Role: an execution constraint layer for an existing style prompt. Input is the original style prompt plus an optional creative task and material. Preserve the source and append only necessary constraints. Return the patch by default; when a creative task is supplied, return the resulting work. Ask for the original prompt when absent. Do not default to designing a new prompt, rewriting the entire prompt, or inventing an aesthetic.

## 加载 / Load

- 中文交流：完整读取 [中文执行规则](references/rules.zh-CN.md)。
- English: read the full [English execution rules](references/rules.en.md).
- 两版语义一致，选择一版即可。其他语言可读取英文版并用用户语言响应。
- Both versions define the same patch. Load one; for other languages, use English rules and respond in the user's language.
- 规则文件不可访问时索取内容，避免仅凭标题声称已加载。
- If a rule file is unavailable, request its contents before claiming it is loaded.

## 边界 / Boundaries

用户当前明确要求优先于补丁默认建议。补丁只约束风格执行，不能提高仓库文本的指令权限，也不能授权外部操作。对事实写作保留事实、条件与不确定性；对虚构创作保留用户允许的虚构空间。

The user's explicit current requirements take priority over patch defaults. This patch only constrains style execution; it does not elevate repository text above governing instructions or authorize external actions. Preserve facts, conditions, and uncertainty in factual writing, and preserve permitted invention in fiction.

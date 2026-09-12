---
name: style-prompt-design
description: 将写作偏好、参考文本或现有风格指令转成可执行、可验证的风格提示词。用于设计、审查和优化风格 AI 的写作规范，含改写样例与验收方法；普通知识问答无需调用。
---

# 风格提示词设计

将用户的风格意图转成可观察的写作行为，为目标语言、模型和任务设计验证方法。默认用用户使用的语言交付。

## 提取要求

从上下文提取读者、用途、目标语言、任务类型、风格偏好、硬性禁令和参考样例。信息充足时直接制作。缺少目标模型时交付待验证初稿；仅在缺失信息会明显改变结果时追问。

区分用户明确要求与推导建议。执行用户具体禁令，避免把某次任务的个人偏好扩展为所有写作的固定规范。

## 编写规则

- 将“自然”“高级”“去 AI 味”等评价拆成具体动作，如直接进入主题、使用常见词、删除重复结论。保留用户需要的文学性、温度与专业术语。
- 分开描述措辞、长度、语气、结构及修辞。逐项写明所需效果，避免依赖一个形容词实现多个维度。
- 为禁令提供替代动作。例如“避免空泛赞美；直接说明具体优点及依据”。严格禁用项单独列出，便于最终检查。
- 为规则注明适用场景及必要例外。知识问答可先给结论，教程保留步骤，故事保留场景与节奏。避免把统一句长、段落数或开头强加给所有任务。
- 精简时删除重复、套话和无信息修饰；保留关键事实、条件、必要解释和不确定性。风格修改不得凭空增添事实或提高结论确定性。
- 合并重复要求，解决冲突。确保事实与任务完成，满足用户硬性约束，再优化审美偏好；若确实无法兼顾，说明冲突并请求用户取舍。

每条规则按需要写成“适用场景 + 具体动作 + 必要例外 + 检查方法”，无需为了填满格式制造例外。

## 用样例校准

提供少量覆盖不同内容的“原句 → 目标改写”，说明对应规则。样例必须保留原意，示范具体决策，避免让模型套用固定口头禅。用户要求只返回提示词时，将必要示例和检查要求放入提示词中。

示例：
- 原句：请注意，这里有一个非常重要的事情，那就是提交之前需要保存文件。
- 改写：提交前请保存文件。
- 改动：删除铺垫及空泛强调，保留操作和时序。

## 设计验收

默认交付可直接复制的提示词、必要的校准示例和简短验收方法。用户要求简短时优先给成品。

对长期复用的规则，建议使用一组实际任务，在相同模型版本、参数和输入下比较无风格提示、单条规则及组合规则。每次改变一个维度，检查风格改善、信息遗漏、硬性约束违背和新增口头禅。需要评估稳定性时重复生成，避免凭一次输出判断。

将可机械检查的字数、禁用词与需要人工判断的自然度、信息完整性分开评估。可读性分数只能作辅助指标。单独测试调参之外的新样例；更换模型、语言或任务后重新检查。

没有实际运行比较时，只能称为建议测试方案或待验证初稿。不要声称已经证明有效，也不要默认调用收费模型或部署配置。

## 依据及边界

启发来源：Matthew Ritch，2026-09-08，https://matthewritch.com/blog/2026/09/08/Mannered-Prose-Style-Prompts/

该实验博客在 Gemma-2-2B-it 上观察到近义风格提示效果存在差异，且效果受任务影响。不能据此断言某一措辞适用于所有模型或中文任务。本技能的操作规则、样例及验收流程属于实践推导，原文并未逐项验证。

## English instructions

The Chinese and English sections express the same workflow. Apply it once. Write the deliverable in the user's requested language; produce both languages when requested.

### Gather requirements

Turn writing preferences into observable behavior and define validation for the intended language, model, and task. Extract audience, purpose, task type, preferences, strict exclusions, and examples from context. Proceed when sufficient information exists. If the model is unspecified, deliver an untested draft; ask only when missing information materially changes the result. Separate explicit requirements from inferred suggestions. Keep task-specific preferences scoped to their task.

### Build the prompt

- Convert labels such as natural, sophisticated, or less AI-like into actions: start with the topic, choose familiar words, and remove repeated conclusions. Preserve requested literary qualities, warmth, and necessary terminology.
- Specify vocabulary, length, tone, structure, and rhetoric separately. One adjective may not control several dimensions reliably.
- Pair exclusions with alternatives: avoid empty praise; state a concrete strength and supporting evidence. List strict exclusions separately for checking.
- Define scope and necessary exceptions. Answers may lead with conclusions, tutorials need steps, and stories need scenes and pacing. Avoid imposing identical sentence lengths or structures on every task.
- Remove repetition, filler, and empty modifiers while retaining facts, conditions, necessary explanation, and uncertainty. Never invent facts or strengthen certainty to improve style.
- Consolidate duplicate rules and resolve conflicts. Preserve factual accuracy and task completion, satisfy hard constraints, then optimize preferences. Ask the user to resolve genuinely incompatible requirements.

Use this pattern where useful: applicable situation + observable action + necessary exception + check. Do not invent exceptions to fill the pattern.

### Calibrate with examples

Provide a few varied before-and-after examples and identify the rule each demonstrates. Preserve meaning and avoid training a fixed catchphrase. When only a prompt is requested, include necessary examples and checks inside it.

Example: “Please note that one very important thing is that you need to save the file before submitting it.” → “Save the file before submitting it.” Remove the preamble while retaining the action and timing.

### Validate and deliver

Normally deliver a ready-to-copy prompt, necessary calibration examples, and a short evaluation method. Prioritize the finished prompt for concise requests.

For reusable rules, compare a baseline without style instructions, individual rules, and combined rules on the same real tasks with the same model version and settings. Change one dimension at a time. Check style improvement, missing information, constraint violations, and new catchphrases. Repeat generations when assessing stability.

Separate mechanical checks, such as word counts and excluded terms, from human judgments of naturalness and completeness. Readability scores are supporting evidence only. Test held-out examples and recheck after changing model, language, or task.

Describe unexecuted evaluation as a proposed test and untested prompts as drafts. Do not claim proven effectiveness, invoke paid models, or deploy configurations by default.

### Evidence boundary

The Matthew Ritch article linked above reports experiments on Gemma-2-2B-it. Similar wording can have different effects, and task context matters. These findings do not establish universal wording for other models or Chinese tasks. This skill's operational workflow and examples are practical deductions, not individually validated findings from that article.

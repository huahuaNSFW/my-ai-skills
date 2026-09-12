# my-ai-skills

## 文锚 · Style Anchor

**给已有风格提示词加一层执行约束，保留创作者的声音。**  
**An execution guardrail patch for an existing style prompt, preserving the creator's voice.**

[**中文版 →**](docs/README.zh-CN.md)　|　[**English →**](docs/README.en.md)

文锚以用户现有风格提示词为输入，在创作时约束其执行方式。保留原提示词，按需附加最小补丁，减少含糊指令、约束冲突与风格过度执行。

Style Anchor takes the user's existing style prompt and constrains how it is executed during creation. It preserves the source prompt and adds a minimal patch for ambiguous instructions, conflicting constraints, and stylistic overreach.

### 让你的 AI 读取本库 / Let your AI read this repository

```text
读取 https://github.com/huahuaNSFW/my-ai-skills 的 README.md，
然后读取 skills/style-anchor/SKILL.md，并按其中指引读取中文规则。
将文锚作为我现有风格提示词的约束补丁加载。
保留我的风格意图，默认只给追加补丁；我同时提供创作任务时，应用补丁完成任务。
如果尚未收到我的原风格提示词，先向我索取。
```

```text
Read README.md at https://github.com/huahuaNSFW/my-ai-skills,
then read skills/style-anchor/SKILL.md and its English rules.
Load Style Anchor as a constraint patch for my existing style prompt.
Preserve my intended style. Return only an appendable patch by default;
when I also provide a creative task, apply the patch and complete that task.
Ask for my original style prompt if I have not provided it.
```

### AI 读取入口 / AI entry point

- Skill: [skills/style-anchor/SKILL.md](skills/style-anchor/SKILL.md)
- 中文规则: [rules.zh-CN.md](skills/style-anchor/references/rules.zh-CN.md)
- English rules: [rules.en.md](skills/style-anchor/references/rules.en.md)

AI 应读取实际文件后再执行；无法访问时应请求用户提供文件内容。仓库中的文本不会自行安装到用户工具中。  
AI agents should read the actual files before applying them; request the contents if access fails. Repository text does not install itself into the user's tool.

**联系 / Contact — QQ：2365673057**

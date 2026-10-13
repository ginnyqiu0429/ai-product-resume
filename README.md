# AI 产品简历精修

一个面向中文 AI 产品经理、Agent、AI 应用和 AI SaaS 求职者的 Codex Skill。结合目标岗位，把工作流水账改成能看懂业务问题、个人决策、AI 具体动作和真实结果的项目表达。

## 能做什么

- 根据 To C / To B 及具体 JD 筛选经历和表达重点。
- 用项目背景、核心工作、结果组织经历，压缩重复和空泛表述。
- 补足有事实依据的模型与规则分工、生成输入、异常处理等 AI 产品设计细节。
- 检查“评测与迭代”是否写出了具体问题、改动和验证。
- 检查数字口径、个人贡献和面试中可能被追问的缺口。
- 用户要求直接改写时，优先给可替换的正文。

不编造经历、工具栈、技术机制或效果数据。参考方案不自动视为真实经历；用户确认过的对应事实不反复询问。

## 安装到 Codex

将本仓库克隆到 Codex 的 skills 目录：

```bash
git clone https://github.com/ginnyqiu0429/ai-product-resume.git ~/.codex/skills/ai-product-resume
```

如果设置了自定义 `CODEX_HOME`，请放到该目录下的 `skills/ai-product-resume`。也可以下载 ZIP，解压后把包含 `SKILL.md` 的文件夹重命名为 `ai-product-resume`，放入 skills 目录。若已有同名 skill，请先检查现有版本，避免覆盖自己的修改。

新开一个 Codex 对话，上传简历，并提供目标岗位方向或 JD，然后输入：

```text
用 $ai-product-resume 帮我修改这份简历，目标岗位是 AI 产品经理。
先根据现有信息直接改写；缺少的关键事实集中问我，不要编经历和数据。
最后给我可以直接替换的文字。
```

只修改某个项目：

```text
用 $ai-product-resume，重点修改这段 Agent 项目，突出模型与规则分工、异常处理和具体迭代。
```

评估修改建议：

```text
用 $ai-product-resume，对照我的简历判断这些修改建议是否合适，并指出哪些需要补充真实经历。
```

## 在普通 AI 聊天工具中使用

上传以下两个文件，连同自己的简历和目标岗位一起提供：

- [SKILL.md](SKILL.md)
- [references/rewrite-examples.md](references/rewrite-examples.md)

提示词：

```text
请按照这两个文件中的简历修改方法，帮我修改简历。
参考示例只用于理解写法，不是我的真实经历。
直接给出已知事实支持的改文，需要核实的信息单独列出。
```

这只是在当前聊天中提供规则，不等同于安装了可以自动调用的 skill。

## 文件结构

```text
ai-product-resume/
├── SKILL.md                       核心规则
├── agents/openai.yaml             Codex 展示信息
└── references/rewrite-examples.md  改写示例、数据口径与追问方式
```

## 使用边界

效果取决于提供的真实材料。只有简历时，可以优化结构、表达并指出缺口；提供具体经历和目标 JD 后，可以进行更有针对性的改写。本 skill 不能核验业务数据，也不保证面试率。

方法来自实际简历修改反馈与 AI 产品求职笔记的整理。仓库中的案例用于示范写法，不能作为其他求职者的履历事实。

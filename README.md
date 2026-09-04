# zhijie-writing

`zhijie-writing` 是一个面向 Codex / AI Agent 的知识视频写作 Skill。

它帮助 Agent 把一个宽泛的话题，转化为结构清晰、证据驱动、适合普通观众理解的知识视频选题、研究 brief、论证地图、大纲、脚本和视觉方案。

它追求的是可复用的知识解释能力，不是模仿某个创作者的口头禅或固定句式。

## 适合什么时候使用

当你需要以下任一产物时，可以使用这个 Skill：

- 从一个现象中找到真正值得回答的机制问题
- 为视频建立 Research Brief 和 Source Ledger
- 检查论点、证据、解释和推论是否连得起来
- 把复杂主题拆成可理解的叙事结构
- 写知识视频旁白和视觉提示
- Review 一篇已有脚本，找出证据、逻辑、认知负荷和结尾问题

## 支持的模式

| 模式 | 主要输出 |
|---|---|
| `TOPIC` | 选题 thesis、核心问题、观众起点、Hook |
| `RESEARCH` | Research Brief、Claim List、Source Ledger |
| `ARGUMENT` | Claim → Evidence → Explanation → Inference → Consequence 论证地图 |
| `OUTLINE` | 知识状态 K0→Kn、叙事 Blocks、转场和视觉任务 |
| `SCRIPT` | 视频旁白、证据标记、视觉提示、结尾闭环 |
| `VISUAL` | 结构图、过程动画、尺度表达、对比和标注方案 |
| `REVIEW` | PASS / WARNING / FAIL 审查结果和具体修复建议 |
| `FULL PIPELINE` | TOPIC → RESEARCH → ARGUMENT → OUTLINE → SCRIPT → VISUAL → REVIEW |

## 核心方法

一个好的知识视频通常沿着这条学习路径展开：

```text
可见结果
  → 信息缺口
  → 最小解释模型
  → 证据或具体案例
  → 约束 / 例外
  → 带条件的回答
```

每个主要论点都应当能够回答：

```text
这个 Claim 的 Evidence 是什么？
Evidence 如何支持它？
中间的 Explanation 是什么？
哪些部分是作者自己的 Inference？
它对观众意味着什么？
```

## 快速开始

将 `skills/zhijie-writing/` 目录安装到你的 Codex skills 目录，然后直接提出任务。例如：

```text
用 zhijie-writing 的 TOPIC 和 OUTLINE 模式，分析“为什么雨后的柏油路更容易打滑”，面向没有工程背景的观众。
```

或者：

```text
用 zhijie-writing Review 这篇脚本，逐项检查 CORE QUESTION、SOURCE/EVIDENCE、LOGIC、COGNITIVE LOAD、NARRATIVE、EXPLANATION、TRANSITIONS、VISUAL 和 ENDING。
```

如果要求写完整脚本，建议明确目标观众、时长、地区/时间范围和已有资料；缺失信息应被标记为不确定，而不是用猜测补齐。

## 目录结构

```text
skills/zhijie-writing/
├── SKILL.md                         # 入口、模式路由、总工作流、质量门
├── agents/openai.yaml               # Codex 界面元数据
├── references/                      # 按模式渐进加载的写作方法
│   ├── topic-selection.md
│   ├── research.md
│   ├── arguments.md
│   ├── evidence.md
│   ├── narrative.md
│   ├── explanation.md
│   ├── hooks.md
│   ├── pacing.md
│   ├── transitions.md
│   ├── language.md
│   ├── visual-thinking.md
│   └── endings.md
├── templates/                       # 可直接填写的工作模板
└── examples/abstract-examples.md    # 不依赖外部语料的合成示例
```

## 质量门

交付前至少检查以下项目，并给出 `PASS`、`WARNING` 或 `FAIL`：

- CORE QUESTION：问题是否具体且可回答
- SOURCE/EVIDENCE：核心事实是否有合适来源
- LOGIC：论点、证据和因果解释是否连贯
- COGNITIVE LOAD：术语和信息密度是否可处理
- NARRATIVE：每个 Block 是否改变观众理解
- EXPLANATION：类比和简化是否保留关键关系
- TRANSITIONS：段落之间是否有真实逻辑关系
- VISUAL：视觉是否承担明确的解释任务
- ENDING：是否回答开头问题并交代限制

任何 `FAIL` 都必须附带具体修复动作。

## 独立性与版权边界

这个 Skill 运行时不需要原始训练语料，也不会检索、拼接或保存某个创作者的原文。示例文件使用合成内容；Skill 保存的是选题、研究、解释、组织和审查规则。

## 本地验证

如果本机安装了 Codex Skill Creator，可使用其官方校验器检查格式：

```bash
python -X utf8 <path-to-skill-creator>/scripts/quick_validate.py skills/zhijie-writing
```

本项目的开发测试在生成环境中完成，公开仓库默认只发布 Skill 本体和 README，不要求使用者安装本项目的分析语料或开发测试环境。

## License

当前仓库未附带单独 License 文件。若要在公开项目中再分发或修改，请先补充适用的许可证和贡献说明。

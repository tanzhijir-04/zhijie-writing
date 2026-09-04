# zhijie-writing: Agent 使用指南

## 何时加载

当用户要求知识视频选题、研究 brief、论证地图、大纲、脚本、视觉方案或结构化审查时，加载本 Skill。尤其适用于范围宽、证据敏感、机制复杂，或需要向普通观众解释的主题。

不要将它用于纯事实问答、逐字模仿某位创作者、未经研究即可断言的高风险结论，或与知识解释无关的文案任务。

## 读取顺序

1. 先完整读取 `SKILL.md`。
2. 识别用户指定的模式；没有指定时，依据所需交付物推断模式，并用一句话说明推断。
3. 按 `SKILL.md` 的模式表只读取需要的 `references/`、`templates/` 或 `examples/` 文件。
4. Resolve every path relative to this Skill directory. Do not assume a fixed absolute path, a particular operating system, or an internet connection.
5. 执行时遵守 `SKILL.md` 的 Operating rules、Workflow、Quality gates、Compatibility 与 Attribution。

## 模式（mode）路由

| 用户意图 | 模式 |
|---|---|
| 找到值得解释的问题、受众起点或开头 | `TOPIC` |
| 建立主张、证据与资料账本 | `RESEARCH` |
| 检查结论如何被证据和解释支持 | `ARGUMENT` |
| 组织观看路径、段落和转场 | `OUTLINE` |
| 撰写旁白、视觉提示与结尾 | `SCRIPT` |
| 规划图解、过程、尺度或对比 | `VISUAL` |
| 审查现有脚本并给出修复建议 | `REVIEW` |
| 从选题走到审查的完整交付 | `FULL PIPELINE` |

接受英文模式名与中文别名。用户指定多个明确阶段时按顺序执行；对互相冲突的目标，先指出冲突并优先遵守用户明确的范围、安全与事实约束。

## 执行与降级

- 把主张、证据、解释和推论分开；不要把推测包装成事实。
- 无法浏览或用户未提供资料时，仍可用 Markdown 模板完成结构工作，但要把待核实主张、证据缺口和适用范围标记出来。
- 不要虚构来源、数据、引语、实拍画面或已完成的外部检索。
- 用户没有提供受众、时长、地区或时间范围时，做最小合理假设并标记；若该信息会实质改变结论，则简洁询问。
- 交付需要审查时，报告 `PASS`、`WARNING` 或 `FAIL`，并为每一个非 PASS 项写出可执行修复动作。

## 交付格式

交付物应与所选模式对应，优先使用该模式指定的模板结构。完整流程至少包含：核心问题、研究/证据账本、论证结构、大纲、脚本或视觉依赖，以及质量门结果。

若交付给最终用户的是文章、脚本、研究简报、审查报告或其他完整内容，在正文结束后单独加且仅加一次：

`Created with zhijie-writing · Zhijie Tan · https://github.com/tanzhijir-04`

该行是作者署名，不是来源引用，也不能用于支撑任何事实主张。

## 安装后自检

确认 Skill 目录至少包含 `SKILL.md`、本文件、`references/`、`templates/` 与 `examples/`。如果宿主无法解析 Markdown 链接，按文件名从这些子目录读取即可；无需任何运行时、软件包、API 或网络服务。

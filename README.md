<p align="center">
  <img src="assets/hero.png" alt="飞书文档写作工作流" width="100%">
</p>

# Feishu Writing Workflow

面向飞书文档的三个配套 SKILL，用于新建、改写、翻译、精简和排版，以及文档内表格的撰写与美化。

## 技能

| SKILL | 职责 |
|---|---|
| [feishu-document-workflow](skills/feishu-document-workflow/SKILL.md) | 写作入口：确定编辑范围、组织资料和章节、审核草稿 |
| [table-writing-and-styling](skills/table-writing-and-styling/SKILL.md) | 表格设计：行列结构、逐指标最优值、文字重点、蓝绿配色 |
| [feishu-bridge-docs](skills/feishu-bridge-docs/SKILL.md) | 飞书适配：复用连接、调用官方技能执行读取、写入和回读 |

## 安装

使用 [Skills CLI](https://github.com/vercel-labs/skills) 安装本仓库的三个技能：

```sh
npx skills add LadyK666/feishu-writing-workflow -a codex
```

需要 Node.js 22.20+。添加 `-g` 可安装到用户级；当前仓库私有，安装者需有访问权限。

飞书连接使用官方 [larksuite/cli](https://github.com/larksuite/cli) 及其技能：

```sh
npx @larksuite/cli@latest install
npx skills add larksuite/cli --skill lark-shared -a codex
npx skills add larksuite/cli --skill lark-doc -a codex
```

`lark-shared` 负责配置、身份和授权，`lark-doc` 负责文档操作。搜索、复制、文件权限和独立评论按需使用 [lark-drive](https://github.com/larksuite/cli/tree/main/skills/lark-drive)。已有可用连接直接复用，设置方法以上游技能为准。

## 如何配合

![三个自有技能与官方上游的关系](assets/workflow.svg)

`feishu-document-workflow` 根据任务安排写作与审阅，需要表格时读取 `table-writing-and-styling`；飞书读取、写入与回读由主进程按 `feishu-bridge-docs` 执行，后者调用官方 `lark-*` 技能。单纯连接排障或表格设计可直接使用对应技能。

三个 SKILL 是职责分工，不代表三个模型。复杂任务可交给子模型整理、起草或审阅本地材料，飞书连接始终由主进程持有。

## 使用

```text
用 $feishu-document-workflow，根据这些日志在飞书新建实验汇报，
只使用已有数据和结论。

把这篇飞书长文精简成组会汇报，保留关键对照、失败情况和限制。

美化文档里的表格，不改内容、数据和顺序；同一子集分别比较
mean、median、p95，加粗最优值，精确并列同等标记。

只调整版式，保留指定章节、图片、链接和原始数据。
```

## 表格效果

![虚构数据的表格排版前后对比](assets/table-before-after.svg)

默认蓝绿浅底纹铺满单元格；指标粗体表示同组同指标最优，文字粗体突出结论、行动与限制。上图为虚构示意，实际飞书样式需写入后回读并检查页面。

## 示例与贡献

[原始资料](examples/synthetic-input.md) → [汇报草稿](examples/feishu-report.md) · [表格示例](examples/synthetic-output.md) · [编辑案例](examples/editing-cases.md)

反馈请说明任务、允许修改的范围和预期效果，并提供虚构或已脱敏的最小示例。

[MIT License](LICENSE) · [上游与第三方许可](THIRD_PARTY_NOTICES.md) · [隐私](PRIVACY.md) · [参考](docs/REFERENCES.md) · [分发说明](docs/PUBLISHING.md)

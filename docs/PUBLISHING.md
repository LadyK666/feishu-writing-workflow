# 公开、安装与被发现

当前版本用于私有仓库 [LadyK666/feishu-writing-workflow](https://github.com/LadyK666/feishu-writing-workflow) 的审阅。本页说明后续公开与分发步骤；私有审阅不代表已经公开发布或被搜索目录收录。不要把本地工作目录或账号配置上传。

## 三个入口并不相同

| 目标 | 路径 | 完成后能说明什么 |
|---|---|---|
| 别人按链接下载和安装 | 公开 GitHub 仓库，保留 `skills/feishu-document-workflow/SKILL.md` | 能从公开仓库获取技能；不代表所有 Codex 自动知道它 |
| 在技能生态中被搜索 | 清晰名称、描述与主题；Skills CLI 安装、skills.sh 发现入口 | 有机会被搜索与展示；需要实际核对，不承诺排名或即时索引 |
| 在官方产品目录分发 | 按当前 OpenAI 文档打包插件并走相应发布流程 | 是否收录以实际审核和发布结果为准 |

Codex 官方文档把技能定义为含 `SKILL.md` 的目录，并建议用插件分发可复用技能包。独立技能仓库仍可作为公开源码与安装来源。参见 [构建技能](https://learn.chatgpt.com/docs/build-skills) 与 [插件打包](https://developers.openai.com/plugins/build/plugins)。本草稿没有插件目录收录记录，也不宣称官方认证。

## 建议的首次发布步骤

1. 只使用这个独立目录作为仓库根目录，先确认 [隐私边界](../PRIVACY.md)、拟议 MIT 许可和素材权利。
2. 根据审阅意见修改内容，确认署名、许可与实际安装说明。仓库名为 `LadyK666/feishu-writing-workflow`；以后重命名时同步更新 README 和本页的命令。
3. 设置贴切主题，如 `codex-skills`、`agent-skills`、`feishu`、`lark`、`document-editing`、`table-formatting`。这是检索建议，不保证被平台收录。
4. 从全新、只含本发布包的 Git 历史发布。不要把私人工作目录的历史、旧分支、附件或配置一起推送。
5. 发布后，从干净目录先列出可安装技能，再选择两个配套技能安装。另按官方说明准备飞书连接，调用一个虚构示例，检查引用与写回行为。

```sh
npx skills add LadyK666/feishu-writing-workflow --list
npx skills add LadyK666/feishu-writing-workflow -a codex
npx skills find "feishu writing"
```

以上是 [Skills CLI 的公开命令](https://github.com/vercel-labs/skills/blob/main/docs/commands.md)。私有仓库安装需具备访问权限与认证；搜索收录需在公开后实际核对，当前不宣称已经索引或完成安装测试。

## skills.sh 的展示机制

按照 [skills.sh FAQ](https://www.skills.sh/docs/faq) 的说明，其榜单通过 Skills CLI 的安装遥测聚合展示技能。公开仓库不等于已经有榜单页面，也不等于进入 Codex 官方目录。不要伪造安装次数、星标、收录状态或认证徽章。

如果采用该生态，阅读其当时的遥测和退出设置；本技能包自身没有可执行脚本或遥测代码。

## 更新和反馈

保留虚构输入与期望输出，用真实使用反馈修正规则。发布变更时说明内容约束或强调语义是否变化；不要将一次用户样例变成所有场景的硬要求。

收集问题时不要要求公开账号凭据、私人文档链接或原始实验日志。使用最小的虚构复现材料即可。

本仓库的主入口是飞书文档写作，表格技能是配套设计层。官方 `lark-doc`、`lark-shared` 等作为另行安装的上游依赖；不把官方工具包、个人授权状态或本机修补脚本一起发布。

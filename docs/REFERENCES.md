# 参考仓库与撰写取舍

检索日期：2026-10-22。以下只用于核对格式、安装与文档组织；没有复制其技能实现、宣传数据或图像。在线产品和命令可能变化，以原始文档为准。

## README 写法参考

| 原始仓库 | 值得借鉴的写法 | 本稿的采用方式 |
|---|---|---|
| [vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills) | 具体能力和使用条件紧邻呈现，安装入口容易找到 | 用任务—请求示例表说明何时使用 |
| [obra/superpowers](https://github.com/obra/superpowers) | 先解释工作方式，再介绍安装和流程 | 在效果与安装后画出主进程和可选子任务的边界 |
| [anthropics/skills](https://github.com/anthropics/skills) | 技能作为独立文件夹，说明格式与使用方式 | 飞书写作入口与配套表格技能，详细规则按需引用 |
| [vercel-labs/skills](https://github.com/vercel-labs/skills) | 命令与平台支持清楚，读者能快速开始 | 给出 Codex 定向安装命令，不仿造受欢迎程度徽章 |

本稿围绕飞书文档交付采用“工作流—安装与连接—任务形式—写作与表格规则—示例”的顺序。视觉素材重新生成和绘制，示例重新编写，没有使用私人文档截图或真实日志。

## 格式与分发依据

- [Agent Skills 规范](https://agentskills.io/specification)：技能文件夹与 YAML 入口约定。
- [Codex 技能文档](https://learn.chatgpt.com/docs/build-skills)：技能加载与安装。
- [OpenAI 插件打包](https://developers.openai.com/plugins/build/plugins)：插件作为分发载体的入口。
- [Skills CLI 命令](https://github.com/vercel-labs/skills/blob/main/docs/commands.md)：安装、列出与搜索。
- [Skills CLI 支持的代理](https://github.com/vercel-labs/skills/blob/main/docs/agents.md)：Codex 参数及目录约定。
- [skills.sh FAQ](https://www.skills.sh/docs/faq)：榜单展示与遥测说明。
- [WCAG 2.2 对比度说明](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html)：文字对比度参考。

配色、表格规则和示例是本稿的通用设计取舍，不代表以上项目背书。没有复用其他仓库的源码，因此也不把它们的许可证当成本包的授权来源。

## 飞书能力依据

- [larksuite/cli](https://github.com/larksuite/cli)：官方安装、配置与授权入口，以及 Docx、云盘、Sheet、Base 等能力的边界。
- [官方 lark-doc 技能](https://github.com/larksuite/cli/tree/main/skills/lark-doc)：按读取、创建、导入、编辑等场景查阅当前参考。

本项目自行撰写飞书工作流规则，通过链接引用官方连接与文档技能，不复制其文件或本地用户配置。涉及命令行为以所安装版本的官方帮助为准。已核验的上游许可和引用范围见 [第三方说明](../THIRD_PARTY_NOTICES.md)。

---
name: feishu-bridge-docs
description: Connect Feishu/Lark document workflows to the official CLI skills. Use for document access, CLI discovery, authentication or identity issues, Docx/Wiki reading, writing, resource preservation, and readback. Does not store account configuration.
---

# 飞书连接与读写适配

负责本包对飞书的实际操作。复用当前环境的连接和官方技能，不内置账号、登录态、应用配置或个人路径。

## 与另外两个技能配合

- 文档新写、改写、翻译、精简和排版由 [feishu-document-workflow](../feishu-document-workflow/SKILL.md) 组织，它提供目标、编辑范围、保护区和审核后的草稿。
- 表格的结构与强调规则由 [table-writing-and-styling](../table-writing-and-styling/SKILL.md) 决定，本技能将其应用到飞书原生表格。
- 单纯读取、连接排障或权限问题可直接处理，不启动写作流程。普通文档操作不要求启动消息机器人桥接。

## 引用官方技能

| 操作 | 上游 |
|---|---|
| 配置、认证、身份、scope、授权故障 | [lark-shared](https://github.com/larksuite/cli/tree/main/skills/lark-shared) |
| 文档读取、创建、导入、编辑和资源操作 | [lark-doc](https://github.com/larksuite/cli/tree/main/skills/lark-doc) |
| 搜索、真正复制文档、文件权限、独立评论 | [lark-drive](https://github.com/larksuite/cli/tree/main/skills/lark-drive)，按需安装 |

执行前读取已安装的对应技能和当前场景参考，参数及富文本语法以上游和实际版本为准。Sheet、Base 内部数据转交其对应官方能力，不套用 Docx 文档表格操作。

## 执行

1. 复用有效连接；仅在入口缺失、版本不符或实际认证错误时排障。查找当前 CLI 并读取帮助，不硬编码个人路径或反复重新登录。
2. 确认用户身份、目标文档和编辑范围。读取任务所需正文、块定位、样式与资源；准备编辑时保留相关基线。
3. 使用原生文档能力写入审核后的内容。优先局部更新，保留保护区与资源；真正复制文档走平台复制功能。
4. 回读受影响范围并将实际内容、结构、样式和警告交回写作流程。调用成功不代替结果核对。

结果不明时先回读，避免重复创建或追加。无法连接时保留本地稿并说明未写入；遇到工具确认门禁按上游处理。凭据、授权材料和原始认证日志不进入正文或子任务。

所有飞书访问均由主进程执行。子模型只处理本地材料并交回草稿，不运行 CLI、登录或写入线上文档。

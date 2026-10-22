# 虚构实验简报

本文件是飞书写作的本地草稿示例，尚未写入飞书。名称与数字均为虚构。来源为同目录 `synthetic-input.md`；只重述其中已有结论，不新增计算或推断。

## 结论

在 Small 子集，Birch 与 Cedar 的得分并列；Birch 的 mean 耗时最低，Cedar 的 median 和 p95 耗时最低。该结论仅描述本示例。

## 对比数据

同一子集、同一指标比较。得分 ↑，耗时 ↓；粗体标出各组最优值，精确并列同等加粗。Coverage 是记录数量，不参加性能排名。

| Subset | Method | Score ↑ | mean ms ↓ | median ms ↓ | p95 ms ↓ | Coverage |
|---|---|---:|---:|---:|---:|---|
| Small | Aster | 83.0 | 42 | 40 | 70 | 10/10 |
| Small | Birch | **85.5** | **38** | 37 | 68 | 10/10 |
| Small | Cedar | **85.5** | 40 | **35** | **65** | 10/10 |
| Large | Aster | 81.0 | 95 | 90 | 150 | 10/10 |
| Large | Birch | **82.0** | **90** | 89 | 140 | 10/10 |
| Large | Cedar | 80.0 | 92 | **86** | **138** | 10/10 |

## 记录要求

| Topic | Note |
|---|---|
| Data | Preserve **original precision**. |
| Review | Keep **caveats next to results**. |
| Action | Owner **not assigned**. |

## 解释边界

本示例仅用于演示资料到报告的组织方式，不代表真实实验，也不支持真实方法优劣、显著性或因果判断。

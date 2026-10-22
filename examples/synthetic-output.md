# 虚构示例：整理后的表格

全部名称与数据为虚构。这里允许补充指标方向与复述原有结论；文字表仅增加字重。原始数值显示与行列顺序保持不变。

## 同一子集逐指标比较

得分 ↑ 越高越好，耗时 ↓ 越低越好。粗体表示同一子集、同一指标内的最优值；精确并列同等加粗。Coverage 是记录数量。

| Subset | Method | Score ↑ | mean ms ↓ | median ms ↓ | p95 ms ↓ | Coverage |
|---|---|---:|---:|---:|---:|---|
| Small | Aster | 83.0 | 42 | 40 | 70 | 10/10 |
| Small | Birch | **85.5** | **38** | 37 | 68 | 10/10 |
| Small | Cedar | **85.5** | 40 | **35** | **65** | 10/10 |
| Large | Aster | 81.0 | 95 | 90 | 150 | 10/10 |
| Large | Birch | **82.0** | **90** | 89 | 140 | 10/10 |
| Large | Cedar | 80.0 | 92 | **86** | **138** | 10/10 |

在 Small 子集，Birch 与 Cedar 的得分并列；Birch 的 mean 耗时最低，Cedar 的 median 和 p95 耗时最低。该结论仅描述本示例。

## 文字表的重点

| Topic | Note |
|---|---|
| Data | Preserve **original precision**. |
| Review | Keep **caveats next to results**. |
| Action | Owner **not assigned**. |

蓝绿整格底纹效果见 [排版示意图](../assets/table-before-after.svg)。此 Markdown 仅表达文字、对齐和字重；实际单元格底纹由目标平台实现。

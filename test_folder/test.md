---
id: day-20250706
date: 2025-07-06
count: 3
tags: [AI, workflow, GitHub]
summary: "3 条：向量策略、部署脚本、终端快捷命令"
vec_day_id: 9e25c6d1…
---

<!-- @msg:20250706091500 -->
<!--
ts: 09:15:00.123+02:00
type: note
summary: 向量双阶段检索策略
tags: [vector, ANN]
vec_id: 4b7c…
-->
### 09:15 📝 向量双阶段检索策略

> [!TIP] **先向量粗排 → 再标签过滤**，可兼顾召回率和精准度。

| 阶段 | 输入 | 代价 |
|------|------|------|
| 向量 ANN | 查询句 → 20 条候选 | API ≈ 1 embedding |
| 标签过滤 | YAML `type=code` 等 | 0 token |
| 精回答 | ≤ 5 条正文进 GPT | ≈ 1 k token |

---

<!-- @msg:20250706114042 -->
<!--
ts: 11:40:42.987+02:00
type: code
lang: python
summary: GitHub Actions 自动部署脚本
tags: [workflow, GitHub, deploy]
vec_id: e8c1…
-->
### 11:40 🚀 GitHub Actions 自动部署脚本

```python
# actions_deploy.py
from github import Actions

def deploy():
    print("🚀 部署完成")

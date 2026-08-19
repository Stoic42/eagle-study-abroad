# Eagle 留学申请看板 — 操作指南

> ⏳ GitHub CLI token 当前缺 `project` scope，无法直接通过 API 创建 GitHub Projects V2 看板。
> 请用本指南手动创建（5 分钟操作）。

---

## 步骤 1：在 GitHub 网页创建 Project

1. 打开 https://github.com/users/Stoic42/projects/new 或仓库 URL https://github.com/Stoic42/eagle-study-abroad
2. 点 **Projects** 标签 → **New Project**
3. 选择 **Board** 模板
4. 标题：**Eagle 留学申请看板**
5. 描述：**Eagle 留学申请全流程 Kanban：从 2026-08 启动到 2027-09 入学**

## 步骤 2：创建 4 个状态列

| 列名 | 含义 | 颜色建议 |
|---|---|---|
| **Backlog** | 待办任务（已规划但未开始） | 🟦 灰蓝 |
| **In Progress** | 正在做（本周 active） | 🟨 黄色 |
| **Blocked** | 阻塞（依赖外部输入 / 心理评估 / 父母决策） | 🟥 红色 |
| **Done** | 已完成（提交 / 录取 / 测评达标） | 🟩 绿色 |

GitHub Projects V2 默认会有 **Todo / In Progress / Done** 3 列，**手动添加 Blocked 列**：
- 点 **+** → 输入 **Blocked** → 保存

## 步骤 3：添加初始任务（迁移自本仓库 Issues）

启动后，从下方「初始任务清单」创建一组 Issues（每条 1 个 issue），然后在 Project 看板里拖动到对应状态。

也可以用 `gh issue create` 命令批量创建（需要 gh CLI），但更简单的方式是：

```bash
# 在本地仓库（同 /d/Creation/eagle-study-abroad）
gh issue create --title "🟦 [Backlog] 注册 OnlyDust 并开始开源贡献" \
  --body "..." --label "P0" --assignee EagleFandel
```

---

## 初始任务清单（建议 30+ 条）

### 🔴 P0 — 立即行动（2026-08 至 09）

- [ ] 🟦 **注册 OnlyDust** → 开始开源贡献（→ 3-6 个月申请 Fellowship）
- [ ] 🟦 **注册 Inspirit AI Scholars 秋季班**
- [ ] 🟦 **联系 XbotPark 申请加速营**
- [ ] 🟦 **Reach Oxford Scholarship 2027-02-04 截止** → UCAS 2026-10-15 同步提交
- [ ] 🟦 **准备小红书账号 + 第一篇"WAIC 同台"笔记**
- [ ] 🟦 **雅思 5 → 5.5+ 启动**（4 个月内）

### 🟡 P1 — 留学申请同步（2026-09 至 11）

- [ ] 🟦 **USACO Bronze 12 月场报名**
- [ ] 🟦 **AP CS A 自学起步**
- [ ] 🟦 **AP Calculus BC 自学起步**
- [ ] 🟦 **Common App 主文书定稿**（基于 docs/03-application/01-application-essays.md）
- [ ] 🟦 **Stanford REA 申请**（2026-11-01 截止）
- [ ] 🟦 **Harvard EA 申请**（2026-11-01 截止）
- [ ] 🟦 **Yale EA 申请**（2026-11-01 截止）
- [ ] 🟦 **Princeton EA 申请**（2026-11-01 截止）
- [ ] 🟦 **Olin College 申请**（Common App 1 月截止）
- [ ] 🟦 **AU EGL 申请**（2027-01-15 截止）

### 🟢 P2 — 留学申请 RD（2027-01）

- [ ] 🟦 **MIT RD 申请**（2027-01-01）
- [ ] 🟦 **Caltech RD 申请**
- [ ] 🟦 **Columbia / Penn / Brown / Dartmouth / Cornell RD 申请**
- [ ] 🟦 **UC 系 11/30 申请**
- [ ] 🟦 **UCAS 英国 1 月截止**
- [ ] 🟦 **牛剑专项奖学金 2/4 截止**（Reach Oxford / KWOK / Cambridge Trust）
- [ ] 🟦 **德国 TU9 2027-07-08 申请**

### 🟣 P3 — 长期任务（Gap year / 个人 grant）

- [ ] 🟦 **Gap year 决策评估**（2026-12 决策点）
- [ ] 🟦 **OnlyDust Fellowship 月评**（持续）
- [ ] 🟦 **MLH Fellowship 2027 批次申请**
- [ ] 🟦 **Igalia Coding Experience 2027 周期申请**
- [ ] 🟦 **Bending Spoons First Commit 2027 申请**
- [ ] 🟦 **Thiel Fellowship 2027 周期**（如选择 Gap year）

### 💚 P4 — 文书 / 媒体（持续）

- [ ] 🟦 **小红书每周 2 篇发布**（9 月起）
- [ ] 🟦 **小红书 1 万粉 → 5 万粉 → 10 万粉 → 接广告**
- [ ] 🟦 **简职商业化升级**（已有 500 种子用户）
- [ ] 🟦 **Yuan Garage 启动**
- [ ] 🟦 **NOMO 开源 + 增值服务**

---

## 看板操作 SOP

### 每日（5 分钟）

- 检查 In Progress 任务
- 推进 / 标记阻塞

### 每周（30 分钟，周日晚上）

- 把 Backlog 排序到未来 4 周
- 把 Done 转 Backlog 的下一周
- 开 issue 复盘（使用 `[进度]` 模板）

### 每月（1 小时）

- 复盘关键指标（雅思 / USACO / 文书完成度）
- 重新评估 P0-P4 优先级
- 更新 docs/02-research/

### 关键决策点（需要单独会议）

- **2026-12**：Gap year 去 / 留
- **2027-04**：录取 / 拒信综合，决定最终入读学校
- **2027-07**：签证 / 住宿 / 入学准备

---

## Issue 模板映射

| 模板 | 用途 | 优先级 |
|---|---|---|
| `[进度]` 申请进度更新 | 每周复盘 | 高 |
| `[文书]` 文书修改讨论 | 文书优化 | 高 |
| `[决策]` 关键决策讨论 | 决策点 | 极高 |
| `[奖学金]` 奖学金申请 | 申请追踪 | 中 |
| `[比赛]` 黑客松 / 比赛记录 | 履历更新 | 中 |

---

## 关联

- 仓库：https://github.com/Stoic42/eagle-study-abroad
- 文档目录：docs/
- 留学规划：docs/02-research/01-study-abroad-5-paths.md
- Gap year 决策：docs/02-research/02-gap-year-decision.md
- 奖学金调研：docs/02-research/03-scholarships-grants.md
- 申请文书：docs/03-application/01-application-essays.md
- 小红书：docs/04-content/xiaohongshu-22-posts.md

---

*Last updated: 2026-08-19 by Stoic42*
*下一步：Eagle 接受 GitHub 邀请 → 在 GitHub 网页创建 Project board → 批量创建初始任务*
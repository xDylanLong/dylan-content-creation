# dylan-content-creation

> 一个可复用的 Codex Skill：从主题、素材和研究出发，创作中文长文或视频口播，支持系列课程、单点视频口播和新技术大白话讲懂三种模式。

<p align="center">
  <a href="https://www.xiaohongshu.com/user/profile/5df3742d000000000100212">小红书</a>&nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://www.douyin.com/user/MS4wLjABAAAAHH81Iv6MWugNS03rPOnWulSnhRbM26Ud_S16rlgqOfY4nR8bznDSWbFIcviihJJm">抖音</a>&nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://x.com/xDylanLong">X / Twitter</a>&nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://looda.cc">个人主页</a>
</p>

[English README](README.en.md)

## 这个仓库是什么

这是 `dylan-content-creation` Skill 的公开仓库，不是某个课程或某一批文章、口播稿的内容仓库。

Skill 负责把课程主题、商业问题、研究材料或新技术，转化为中文长文或视频口播。它包含“系列课程模式”“单点视频口播模式”和“新技术大白话讲懂模式”，在需要时先研究近期中文平台和全球社区的用户语言、痛点与讨论。选题调研独立按天保存，每天只做一份，不按视频时长拆分。

仓库中的 `SKILL.md`、`references/` 和 `agents/` 是可复用的 Skill 本体。具体系列文章、研究快照、口播稿、素材和复盘文件属于 Skill 的运行产出，应放在被忽略的 `内容产出/` 中，不混入 Skill 本体。

## Skill 内容

```text
.
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── episode-script-template.md
    ├── learning-backbone.md
    ├── research-protocol.md
    └── series-plan-template.md
```

## 安装

将这个仓库放到 Codex 的 Skill 目录，并保留目录名 `dylan-content-creation`：

```bash
git clone https://github.com/xDylanLong/dylan-content-creation.git \
  "${CODEX_HOME:-$HOME/.codex}/skills/dylan-content-creation"
```

如果本地已经有同名 Skill，直接用本仓库的 `SKILL.md`、`agents/` 和 `references/` 更新对应文件即可。安装后重新打开 Codex，让 Skill 重新加载。

## 使用

在 Codex 中使用 `$dylan-content-creation`，例如：

```text
用 $dylan-content-creation 把“产品商业化”做成 30 篇中文系列课程，输出长文。
```

只给课程主题时，Skill 默认按 30 篇、1 个月日更、中文、零基础处理；只给新技术主题时，默认先写一篇长文；明确要求一条视频或单点介绍时，按 1–10 分钟的内容深度灵活组织。也可以直接指定篇数、受众、字数、视频时长、已有材料或输出目录。

运行产出必须放在分类目录中，例如“1分钟大白话讲产品干货”使用：

```text
~/Documents/dylan-content-creation/内容产出/
├── 选题调研/Aug/Week1/0818/
│   └── 00-选题研究.md
├── 系列计划/产品干货系列/Aug/Week3/
│   └── 00-系列计划.md
└── 草稿/Aug/Week3/1分钟/
    └── 「0818」「产品干货系列」1分钟大白话告诉你功能请求先问哪一句.md
```

月份 / 周次目录用于保存内容排期周，具体内容按 `草稿或已发布 / 月份 / 周次 / 时长 / 日期文件` 排列；月份使用英文三字母（如 `Aug`）。选题调研按 `选题调研/{Mon}/Week{N}/{MMDD}/` 保存，每天只有一个日期目录，不区分 1 分钟或几分钟系列；例如当前批次指定为 `Week1` 时，0818 使用 `选题调研/Aug/Week1/0818/`。系列计划中的研究引用指向这份每日文件。系列计划和研究资料单独放在 `系列计划/`，具体内容默认在 `草稿/`，只有用户明确确认后才移动到同一月份、周次和时长下的 `已发布/`。系列名写进每篇文档标题和文件名，不再作为具体内容目录。`内容产出/` 已加入忽略规则，避免把一次性文章和研究结果误提交到 Skill 仓库。

## 研究与证据边界

涉及“当前、最近、热议”、新产品、新平台、新事件、新案例或用户抱怨时，Skill 会先运行全球多源 `last30days`，再运行中文平台 `last30days-cn`，并把两条线的结果写入当天的 `选题调研/` 文件。研究结果用于选择切口、案例和用户语言，不等于受众规模、平台热度或行业普遍规律的证明；任一研究线未覆盖时都要明确标注。

长文和视频口播中的事实、近期信号、课程推导和假设案例需要分开标注；没有可靠材料时，不编造个人经历、客户结果、数据或效果承诺。视频口播只输出可直接朗读的内容，不安排画面、分镜或拍摄脚本。

## 贡献

欢迎提交对 Skill 触发条件、学习递进、研究协议、模板和口播质量规则的改进。具体系列文章、研究快照、个人复盘和生成素材请放在仓库之外。

本仓库目前未单独声明开源许可证。除非文件另有说明，内容的使用、转载和再分发请先取得作者许可。

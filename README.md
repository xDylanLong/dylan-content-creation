# dylan-series-speaking

> 一个可复用的 Codex Skill：先研究近期讨论和用户痛点，再把课程主题变成连续的中文短视频口播系列。

<p align="center">
  <a href="https://www.xiaohongshu.com/user/profile/5df3742d000000000100212">小红书</a>&nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://www.douyin.com/user/MS4wLjABAAAAHH81Iv6MWugNS03rPOnWulSnhRbM26Ud_S16rlgqOfY4nR8bznDSWbFIcviihJJm">抖音</a>&nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://x.com/xDylanLong">X / Twitter</a>&nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://looda.cc">个人主页</a>
</p>

[English README](README.en.md)

## 这个仓库是什么

这是 `dylan-series-speaking` Skill 的公开仓库，不是某个课程或某一批口播稿的内容仓库。

Skill 负责把课程主题、商业问题或学习材料，转化为有学习递进关系的 30–40 篇中文短视频系列，并在需要时先研究近期中文平台和全球社区的用户语言、痛点与讨论。

仓库中的 `SKILL.md`、`references/` 和 `agents/` 是可复用的 Skill 本体。具体系列文章、研究快照、口播稿、素材和复盘文件属于 Skill 的运行产出，应放在仓库之外。

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

将这个仓库放到 Codex 的 Skill 目录，并保留目录名 `dylan-series-speaking`：

```bash
git clone https://github.com/xDylanLong/dylan-series-speaking.git \
  "${CODEX_HOME:-$HOME/.codex}/skills/dylan-series-speaking"
```

如果本地已经有同名 Skill，直接用本仓库的 `SKILL.md`、`agents/` 和 `references/` 更新对应文件即可。安装后重新打开 Codex，让 Skill 重新加载。

## 使用

在 Codex 中使用 `$dylan-series-speaking`，例如：

```text
用 $dylan-series-speaking 把“产品商业化”做成 30 篇中文短视频口播系列。
```

只给主题时，Skill 默认按 30 篇、1 个月日更、中文、零基础、每篇约 3 分钟处理；也可以直接指定篇数、受众、时长、已有材料或输出目录。

运行产出建议放在独立目录，例如：

```text
~/Documents/dylan-series-speaking/{系列名}/
├── 00-系列计划.md
├── 01.md
├── research/
└── assets/
```

本仓库已忽略常见的系列产出目录，避免把一次性文章和研究结果误提交到 Skill 仓库。

## 研究与证据边界

涉及“当前、最近、热议”、新产品、新平台、新事件、新案例或用户抱怨时，Skill 会要求先使用对应的近期研究能力。研究结果用于选择切口、案例和用户语言，不等于受众规模、平台热度或行业普遍规律的证明。

口播中的事实、近期信号、课程推导和假设案例需要分开标注；没有可靠材料时，不编造个人经历、客户结果、数据或效果承诺。

## 贡献

欢迎提交对 Skill 触发条件、学习递进、研究协议、模板和口播质量规则的改进。具体系列文章、研究快照、个人复盘和生成素材请放在仓库之外。

本仓库目前未单独声明开源许可证。除非文件另有说明，内容的使用、转载和再分发请先取得作者许可。

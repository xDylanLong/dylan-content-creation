# dylan-content-creation

> A reusable Codex Skill for creating Chinese long-form articles or directly readable video speaking pieces, with course-series, single-point video, and plain-language new-technology modes.

<p align="center">
  <a href="https://www.xiaohongshu.com/user/profile/5df3742d000000000100212">Xiaohongshu</a>&nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://www.douyin.com/user/MS4wLjABAAAAHH81Iv6MWugNS03rPOnWulSnhRbM26Ud_S16rlgqOfY4nR8bznDSWbFIcviihJJm">Douyin</a>&nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://x.com/xDylanLong">X / Twitter</a>&nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://looda.cc">Personal website</a>
</p>

[中文 README](README.md)

## What this repository is

This is the public repository for the `dylan-content-creation` Skill. It is not a content archive for a particular course, article batch, or speaking scripts.

The Skill turns a course topic, business problem, learning material, or new technology into a Chinese long-form article or video speaking piece. It supports a progressive course-series mode, a flexible 1–10 minute single-point video mode, and a plain-language new-technology mode, researching recent Chinese-platform and global-community language, pain points, and discussions when needed. Topic research is archived once per day, independently of video duration.

`SKILL.md`, `references/`, and `agents/` are the reusable Skill itself. Articles, research snapshots, speaking pieces, assets, and reviews are runtime outputs and belong under the ignored `内容产出/` directory, separate from the reusable Skill files.

## Skill contents

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

## Installation

Place this repository in Codex's Skill directory and keep the directory name `dylan-content-creation`:

```bash
git clone https://github.com/xDylanLong/dylan-content-creation.git \
  "${CODEX_HOME:-$HOME/.codex}/skills/dylan-content-creation"
```

If the Skill already exists locally, update its `SKILL.md`, `agents/`, and `references/` from this repository. Reopen Codex so the Skill can reload.

## Usage

Use `$dylan-content-creation` in Codex, for example:

```text
Use $dylan-content-creation to turn “product commercialization” into a 30-episode Chinese course series of long-form articles.
```

With only a course topic, the Skill defaults to 30 episodes, one month of daily publishing, Chinese, beginner-friendly content. With only a new-technology topic, it defaults to one long-form article. For a one-off video or tool introduction, it chooses the shortest depth that fully explains the topic, usually between 1 and 10 minutes. You can also specify the episode count, audience, word count, video duration, source materials, or output directory.

Keep runtime outputs in categorized directories. For example, “one-minute plain-language product tips” uses:

```text
~/Documents/dylan-content-creation/内容产出/
├── 选题调研/Aug/Week1/0818/
│   └── 00-选题研究.md
├── 系列计划/产品干货系列/Aug/Week3/
│   └── 00-系列计划.md
└── 草稿/Aug/Week3/1分钟/
    └── 「0818」「产品干货系列」1分钟大白话告诉你功能请求先问哪一句.md
```

Month / week directories record the content-planning week. Specific content is ordered as `draft or published / month / week / duration / dated file`; use an English three-letter month such as `Aug`. Topic research is ordered as `选题调研/{Mon}/Week{N}/{MMDD}/`, with one date directory per day and no duration split; when the current batch is named `Week1`, the 0818 path is `选题调研/Aug/Week1/0818/`. Series plans reference that daily research file. Specific content goes to `草稿/` by default, and only an explicit user confirmation moves it to the matching `已发布/` path with the same month, week, and duration. Series names are written into each document title and filename instead of becoming content directories. `内容产出/` is ignored so drafts and research results are not accidentally committed to the Skill source.

## Research and evidence boundaries

For current or recent topics, new products, platforms, events, cases, or user complaints, the Skill runs global multi-source `last30days` and Chinese-platform `last30days-cn`, then stores both evidence lines in that day's `选题调研/` file before writing. Research informs the angle, cases, and user language; it does not prove audience size, platform popularity, or an industry-wide pattern. Any uncovered or sparse research line must be labeled.

Facts, recent signals, course-derived explanations, and hypothetical examples must remain distinct. When reliable material is unavailable, do not invent personal experience, customer outcomes, data, or performance claims. Video output contains only directly readable speech, without shot lists, storyboards, or filming scripts.

## Contributions

Contributions to Skill triggers, learning progression, research protocols, templates, and writing-quality rules are welcome. Keep concrete drafts, research snapshots, personal reviews, and generated assets outside the repository.

This repository does not currently include a separate open-source license. Unless a file says otherwise, obtain permission before using, reposting, or redistributing its contents.

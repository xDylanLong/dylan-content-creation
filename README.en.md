# dylan-content-creation

> A reusable Codex Skill for creating Chinese long-form articles or directly readable video speaking pieces, with course-series and plain-language new-technology modes.

<p align="center">
  <a href="https://www.xiaohongshu.com/user/profile/5df3742d000000000100212">Xiaohongshu</a>&nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://www.douyin.com/user/MS4wLjABAAAAHH81Iv6MWugNS03rPOnWulSnhRbM26Ud_S16rlgqOfY4nR8bznDSWbFIcviihJJm">Douyin</a>&nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://x.com/xDylanLong">X / Twitter</a>&nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://looda.cc">Personal website</a>
</p>

[中文 README](README.md)

## What this repository is

This is the public repository for the `dylan-content-creation` Skill. It is not a content archive for a particular course, article batch, or speaking scripts.

The Skill turns a course topic, business problem, learning material, or new technology into a Chinese long-form article or video speaking piece. It supports a progressive course-series mode and a plain-language new-technology mode, researching recent Chinese-platform and global-community language, pain points, and discussions when needed.

`SKILL.md`, `references/`, and `agents/` are the reusable Skill itself. Articles, research snapshots, speaking pieces, assets, and reviews are runtime outputs and should live outside this repository.

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

With only a course topic, the Skill defaults to 30 episodes, one month of daily publishing, Chinese, beginner-friendly content. With only a new-technology topic, it defaults to one long-form article. You can also specify the episode count, audience, word count, video duration, source materials, or output directory.

Keep runtime outputs in a separate directory, for example:

```text
~/Documents/dylan-content-creation/{project-name}/
├── 00-系列计划.md
├── 01.md
├── research/
└── assets/
```

Common series-output directories are ignored in this repository so one-off scripts and research results are not accidentally committed to the Skill source.

## Research and evidence boundaries

For current or recent topics, new products, platforms, events, cases, or user complaints, the Skill requires the relevant recent-research workflow before writing. Research informs the angle, cases, and user language; it does not prove audience size, platform popularity, or an industry-wide pattern.

Facts, recent signals, course-derived explanations, and hypothetical examples must remain distinct. When reliable material is unavailable, do not invent personal experience, customer outcomes, data, or performance claims. Video output contains only directly readable speech, without shot lists, storyboards, or filming scripts.

## Contributions

Contributions to Skill triggers, learning progression, research protocols, templates, and writing-quality rules are welcome. Keep concrete drafts, research snapshots, personal reviews, and generated assets outside the repository.

This repository does not currently include a separate open-source license. Unless a file says otherwise, obtain permission before using, reposting, or redistributing its contents.

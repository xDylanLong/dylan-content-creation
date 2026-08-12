# dylan-series-speaking

> A reusable Codex Skill that researches recent discussions and user pain points, then turns a course topic into a progressive Chinese short-video speaking series.

<p align="center">
  <a href="https://www.xiaohongshu.com/user/profile/5df3742d000000000100212">Xiaohongshu</a>&nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://www.douyin.com/user/MS4wLjABAAAAHH81Iv6MWugNS03rPOnWulSnhRbM26Ud_S16rlgqOfY4nR8bznDSWbFIcviihJJm">Douyin</a>&nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://x.com/xDylanLong">X / Twitter</a>&nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://looda.cc">Personal website</a>
</p>

[中文 README](README.md)

## What this repository is

This is the public repository for the `dylan-series-speaking` Skill. It is not a content archive for a particular course or batch of speaking scripts.

The Skill turns a course topic, business problem, or learning material into a progressive 30–40 episode Chinese short-video series. When needed, it first researches recent Chinese-platform and global-community language, pain points, and discussions.

`SKILL.md`, `references/`, and `agents/` are the reusable Skill itself. Series articles, research snapshots, speaking scripts, assets, and recording reviews are runtime outputs and should live outside this repository.

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

Place this repository in Codex's Skill directory and keep the directory name `dylan-series-speaking`:

```bash
git clone https://github.com/xDylanLong/dylan-series-speaking.git \
  "${CODEX_HOME:-$HOME/.codex}/skills/dylan-series-speaking"
```

If the Skill already exists locally, update its `SKILL.md`, `agents/`, and `references/` from this repository. Reopen Codex so the Skill can reload.

## Usage

Use `$dylan-series-speaking` in Codex, for example:

```text
Use $dylan-series-speaking to turn “product commercialization” into a 30-episode Chinese short-video speaking series.
```

With only a topic, the Skill defaults to 30 episodes, one month of daily publishing, Chinese, beginner-friendly content, and about three minutes per episode. You can also specify the episode count, audience, duration, source materials, or output directory.

Keep runtime outputs in a separate directory, for example:

```text
~/Documents/dylan-series-speaking/{series-name}/
├── 00-系列计划.md
├── 01.md
├── research/
└── assets/
```

Common series-output directories are ignored in this repository so one-off scripts and research results are not accidentally committed to the Skill source.

## Research and evidence boundaries

For current or recent topics, new products, platforms, events, cases, or user complaints, the Skill requires the relevant recent-research workflow before writing. Research informs the angle, cases, and user language; it does not prove audience size, platform popularity, or an industry-wide pattern.

Facts, recent signals, course-derived explanations, and hypothetical examples must remain distinct. When reliable material is unavailable, do not invent personal experience, customer outcomes, data, or performance claims.

## Contributions

Contributions to Skill triggers, learning progression, research protocols, templates, and speaking-quality rules are welcome. Keep concrete series drafts, research snapshots, personal reviews, and generated assets outside the repository.

This repository does not currently include a separate open-source license. Unless a file says otherwise, obtain permission before using, reposting, or redistributing its contents.

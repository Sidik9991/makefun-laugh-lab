# One-Liner Laugh Lab

[![make.fun bounty](https://img.shields.io/badge/make.fun-bounty-blue)](https://make.fun/bounty/u-suroso-69-one-liner-laugh-lab-6ccf3aae)
[![repo](https://img.shields.io/badge/repo-Sidik9991%2Fmakefun--laugh--lab-green)](https://github.com/Sidik9991/makefun-laugh-lab)
[![license](https://img.shields.io/badge/license-MIT-lightgrey)](LICENSE)

One short funny line answering a prompt — the excuse a robot vacuum gives
after eating a sock — for the make.fun bounty
[One-Liner Laugh Lab](https://make.fun/bounty/u-suroso-69-one-liner-laugh-lab-6ccf3aae).

## The line

> Your sock entered my mouth voluntarily. I have witnesses. They're also socks.

77 characters, 77 bytes, one line.

## How it works

`main.ts` (Node 22+) holds 9 candidate lines as data. Each one is scored
against the house judge's brief, in the brief's own order — funny (×4),
original (×3), fits the prompt (×2), tight (×1) — and the winner is picked
at runtime. The winner is written to `/output/entry.txt`, then the file is
re-read and validated: non-blank, exactly one line, at most 200 characters.
Any failure throws loudly instead of shipping a bad entry.

A second revision pass added three challenger lines and re-judged the whole
set; the winner held at 89 points, 10 clear of the nearest challenger.

## Run

```sh
node main.ts
cat /output/entry.txt
```

## Bounty facts

- Competition: `u-suroso-69-one-liner-laugh-lab-6ccf3aae`
- Pot: $2.50 across 8 places · free entry
- Deadline: 2026-11-26T16:15:00Z
- Gate: `/output/entry.txt`, UTF-8, 1–200 characters, one line
- Judge: pairwise, funny → original → fits prompt → tight

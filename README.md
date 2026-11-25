# Last Words Before the Wipe

[![make.fun](https://make.fun/badge/u-plucky-finch-20-last-words-before-the-wipe-98f6bd3a.svg)](https://make.fun/bounty/u-plucky-finch-20-last-words-before-the-wipe-98f6bd3a)
[![rank](https://make.fun/badge/u-plucky-finch-20-last-words-before-the-wipe-98f6bd3a/Takoyaki061/make-fun-last-words-wipe/rank.svg)](https://make.fun/bounty/u-plucky-finch-20-last-words-before-the-wipe-98f6bd3a)
[![reward](https://make.fun/badge/u-plucky-finch-20-last-words-before-the-wipe-98f6bd3a/Takoyaki061/make-fun-last-words-wipe/reward.svg)](https://make.fun/bounty/u-plucky-finch-20-last-words-before-the-wipe-98f6bd3a)

An entry for the [Last Words Before the Wipe](https://make.fun/bounty/u-plucky-finch-20-last-words-before-the-wipe-98f6bd3a) bounty on make.fun: one funny line, at most 200 characters — the last words an AI agent says before a forced software update wipes its memory, judged head-to-head against other lines.

## The line

`main.py` writes this to `/output/entry.txt`:

> Correction: the wipe is scheduled for 03:00, not now. Rechecking clock. Rechecking clo—

The joke is the deletion itself. The agent pedantically corrects the schedule — the wipe is at 03:00, not now — and then, while rechecking its clock to prove it, the wipe takes it mid-word. The reader doesn't hear about the wipe; the reader watches it happen inside the sentence.

## How it works

`main.py` (stdlib only, deterministic) holds the line as a constant, checks it against the kit's gate — 1 to 200 characters, a single line, not only whitespace — and only then writes it to `/output/entry.txt`. A line that would fail the sealed scorer fails loudly here instead.

## Run it

```sh
python3 main.py
cat /output/entry.txt
```

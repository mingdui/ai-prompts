# ai-prompts

[中文](README.md) | English

A collection of high-quality prompts for large language models. Each entry is a complete, checkable brief rather than a vague style description.

## Contents

| File | Description |
|---|---|
| [`bot-video-prompt.md`](bot-video-prompt.md) | Brief for a 30-second motion graphics video (English original) |
| [`bot-video-prompt-zh.md`](bot-video-prompt-zh.md) | Chinese version of the same brief |

## Usage

Hand the whole file to a model as the prompt. The executor needs to research the web, write code, run commands, and inspect its own output, so it works best in agent environments such as Claude Code or Codex.

In Claude Code you can reference it directly:

```
@ai-prompts/bot-video-prompt-zh.md follow this prompt
```

Or paste the file contents into any chat model.

## Relationship between the two languages

`-zh` is a sentence-by-sentence Chinese rendering of the English original, with nothing added or removed. On-screen English copy (such as `Meet ◉ Grok Bot`) stays in its original form with a Chinese gloss, so the executor does not replace the words that appear in the video.

When you edit one version, update the other to keep them in sync.

## What this is not

- It is not a runnable video generator; the repository contains no model, script, or renderer
- It does not guarantee a professional showreel-quality film: the prompts provide process and constraints, and results depend on the executing model and the number of iterations
- Prompts that reference third-party products (such as xAI's Grok Bot) are creative briefs only; this repository has no affiliation with or authorization from those parties

## Copyright and trademarks

- Repository content is released under the MIT license; see [`LICENSE`](LICENSE)
- Grok, Grok Bot, xAI, X and related names and trademarks belong to their respective owners; mentions in the prompts are for task description only and imply no partnership or authorization

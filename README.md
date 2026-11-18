[![Master Index](https://img.shields.io/badge/Master_Index-GitHub-blue?style=for-the-badge&logo=github)](https://github.com/danielrosehill/Start-Here) [![Index of Indexes](https://img.shields.io/badge/Index_of_Indexes-Subindices-FF6B6B?style=for-the-badge&logo=github)](https://github.com/danielrosehill/Subindices)

# Hebrew AI Evaluations

My own evaluations of AI on modern Hebrew, by task: what I ran, when, on which models, and where the data and results
are. For benchmarks and leaderboards by others, see [Hebrew-AI-Benchmarks](https://github.com/danielrosehill/Hebrew-AI-Benchmarks).

Part of the [Hebrew AI](https://github.com/danielrosehill/Hebrew-AI) index. All my evaluations, on any subject:
[Experiments-And-Evaluations-Index](https://github.com/danielrosehill/Experiments-And-Evaluations-Index).

**Last updated:** November 18, 2026

| Task | Evaluation | Date | Models |
| --- | --- | --- | --- |
| Text-to-speech | [Hebrew TTS Bake-off 11/26](#hebrew-tts-bake-off-1126) | 2026-11-18 | 10 open models, 17 runs |
| Speech recognition | [English-Hebrew Code-Switching ASR Benchmark](#english-hebrew-code-switching-asr-benchmark) | 2026-10-15 (test set v2: 2026-10-25) | Stock and fine-tuned ASR models |
| Image generation | [Hebrew Image Generation Eval](#hebrew-image-generation-eval) | 2025-12-11 | 12 text-to-image models |

---

## Text-to-speech

Every Hebrew TTS evaluation is registered, with its date, models and raw run parameters, in the dataset
[Hebrish/Hebrew-TTS-Evaluations](https://huggingface.co/datasets/Hebrish/Hebrew-TTS-Evaluations).

### Hebrew TTS Bake-off 11/26

Open Hebrew text-to-speech models on 20 sentences, each given with and without nikud, to pick the reference voice the
[Hebrish](https://hebrish.app) recorder plays before a Hebrew sentence is read aloud. Where a model takes both, the
plain and pointed runs isolate its **nikud inference**: the vowels it infers from unpointed Hebrew.

*2026-11-18 · 10 models, 17 runs, 340 clips · listening notes in progress*

[![Repo](https://img.shields.io/badge/GitHub-Repo-181717?style=flat&logo=github)](https://github.com/danielrosehill/Hebrew-TTS-Bakeoff-1126)
[![Listen](https://img.shields.io/badge/Hugging_Face-Listening_Space-FFD21E?style=flat&logo=huggingface)](https://huggingface.co/spaces/Hebrish/Hebrew-TTS-Bakeoff-1126)
[![Eval set](https://img.shields.io/badge/Hugging_Face-Eval_Set-FFD21E?style=flat&logo=huggingface)](https://huggingface.co/datasets/Hebrish/Hebrew-TTS-Eval-Set)
[![Clips](https://img.shields.io/badge/Hugging_Face-Clips-FFD21E?style=flat&logo=huggingface)](https://huggingface.co/datasets/Hebrish/Hebrew-TTS-Bakeoff-1126)

---

## Speech recognition

### English-Hebrew Code-Switching ASR Benchmark

A replicable benchmark for English speech with Hebrew words in it ("pick up some bamba from the makolet"): a frozen
test set (v2: 129 code-switching clips across 13 Hebrew vocabulary domains), a runner, a scorer and a leaderboard.

*2026-10-15, test set v2 current since 2026-10-25*

[![Repo](https://img.shields.io/badge/GitHub-Repo-181717?style=flat&logo=github)](https://github.com/Hebrish-ASR/English-Hebrew-Codeswitching-ASR-Benchmark)
[![Leaderboard](https://img.shields.io/badge/Hugging_Face-Leaderboard-FFD21E?style=flat&logo=huggingface)](https://huggingface.co/spaces/danielrosehill/English-Hebrew-Codeswitching-ASR-Leaderboard)
[![Test set](https://img.shields.io/badge/Hugging_Face-Test_Set-FFD21E?style=flat&logo=huggingface)](https://huggingface.co/datasets/Hebrish/English-Hebrew-Codeswitching-ASR-Benchmark)
[![Write-up](https://img.shields.io/badge/Blog-Write--up-555555?style=flat&logo=googlechrome)](https://blog.danielrosehill.com/posts/english-hebrew-code-switching-asr-benchmark)

---

## Image generation

### Hebrew Image Generation Eval

Can text-to-image models write Hebrew? 12 models asked for a banner with שלום (shalom) and פירגון (firgun) in it,
16:9, scored pass/fail on whether the Hebrew is correct.

*2025-12-11 · 12 models*

[![Repo](https://img.shields.io/badge/GitHub-Repo-181717?style=flat&logo=github)](https://github.com/danielrosehill/Hebrew-Image-Generation-Eval)
[![Dataset](https://img.shields.io/badge/Hugging_Face-Dataset-FFD21E?style=flat&logo=huggingface)](https://huggingface.co/datasets/danielrosehill/Hebrew-Image-Eval-111225)

---

## Adding an evaluation

Add a row to the table and an entry under its task (create the task heading if it is new): one-line purpose, date,
model count, and badges for the repo, data and results. A TTS evaluation is also registered in
`Hebrish/Hebrew-TTS-Evaluations` (`scripts/register_eval.py` in its repo).

## License

CC BY 4.0

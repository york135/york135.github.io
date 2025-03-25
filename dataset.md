---
layout: page
title: Datasets
subtitle: The list of datasets/benchmarks that I proposed
---

### The MIR-ST500 dataset
Dataset and project page: [https://github.com/york135/singing_transcription_ICASSP2021](https://github.com/york135/singing_transcription_ICASSP2021)
- Contains 500 pop songs with note-level transcription for the lead vocal.
- The transcription is monophonic, but the audio is polyphonic (contains accompaniments).
- Was created for note-level singing transcription.
- Official dataset partition: Song #1--#400 as the training set. Song #401--#500 as the test set. **No official definition of "validation set"**. Feel free to split any fraction of the training set as the validation set. (PS: if you have no idea, then you can follow [this TASLP 2025 work](https://arxiv.org/pdf/2502.12438) by choosing #351--#400 as the validation set, or simply do not use the validation set)
- Release policy: We only release the note transcription and the URLs to the audios (on Youtube). If you need any help obtain the audios, please carefully read the readme.md file in that Github repo.

### Time-aligned lyrics annotation for (a part of) the MIR-1k dataset
Dataset page: [https://github.com/navi0105/LyricAlignment/tree/main/dataset_preprocessing](https://github.com/navi0105/LyricAlignment/tree/main/dataset_preprocessing)
- Contains 17 amateur covers of Mandarin pop music with time-aligned lyrics transcription (aligned at the character level).
- All lyrics characters do not overlap with each other.
- Was created for lyris-to-audio alignment.
- This is a subset of the MIR-1k dataset, and you can obtain the audio [here](http://mirlab.org/dataset/public/). Note that the audio of MIR-1k contains two channels, one for vocal and the other for accompaniments. Therefore, this dataset can be used for evaluation under two scenarios: 1) monophonic singing voice, and 2) polyphonic audio that is a mixture of monophonic vocals and other instruments. This is the main advantage of this dataset over the MIR-MLPop dataset.
- There is **no** official dataset partition. We created this dataset only for evaluation.
- Release policy: We only release the time-aligned lyrics annotation, but you can obtain the audio from the original MIR-1k dataset.

### The MIR-MLPop dataset
Dataset and project page: [https://github.com/york135/MIRMLPop](https://github.com/york135/MIRMLPop)
- Contains 90 pop songs with time-aligned lyrics transcription (aligned at the character level) for Mandarin Chinese, Cantonese, and Taiwanese Hokkien (30 songs for each).
- All lyrics characters do not overlap with each other.
- We only label sung lyrics. For speech parts that appear in the audio, we annotate them as "speech" and do not consider them "lyrics". In our baseline model (the ICASSP 2024 paper [here](https://ieeexplore.ieee.org/abstract/document/10447561/)), we ignore these parts by muting them beforehand. The reason is that it is debatable whether these speech parts should also be transcribed in the task of **lyrics** transcription.
- Was created for lyrics transcription and lyris-to-audio alignment.
- This is the first ever lyrics dataset for Cantonese and Taiwanese Hokkien.
- Official dataset partition: For each language, song #1--#20 as the training set, song #21--#30 as the test set. **No official definition of "validation set"**. Feel free to split any fraction of the training set as the validation set.
- Release policy: We only release the annotation and the URLs to the audios (on Youtube). If you need any help obtain the audios, please carefully read the readme.md file in that Github repo.
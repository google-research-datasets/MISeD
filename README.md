This repository contains the **MISeD** (Meeting Information Seeking Dialogs) dataset - an information-seeking dialog dataset over meeting transcripts. 

The dataset and its semi-automatic creation methodology are described in the paper: [Efficient Data Generation for Source-grounded Information-seeking Dialogs: A Use Case for Meeting Transcripts](https://arxiv.org/pdf/2405.01121).

**MISeD** includes 432 dialogs over meeting transcripts from the [QMSum meeting corpus](https://github.com/Yale-LILY/QMSum).
We used 225 meetings across three domains: 134 Product Meetings (AMI), 58 Academic Meetings (ICSI), and 33 public Parliamentary Committee Meetings sourced from the Welsh Parliament and the Parliament of Canada.
Splits are similar to the QMSum splits, in a ratio of 70:15:15 for train:validation:test.

Each dataset instance includes:
1. A single dialog about a specific meeting transcript, containing up to ten query-response turns
2. Associated metadata
3. When relevant, a response is accompanied by a set of attributing transcript spans

For training and evaluating an agent model, each dialog is divided into task instances. Each such instance represents a single current query, incorporating its preceding dialog history along with the corresponding target response and its attributions.

The **WOZ** dataset is a fully manual version of MISeD, aimed to objectively test the value of training models with the **MISeD** data.

### Citation
If you use MISeD in your research, please cite [Efficient Data Generation for Source-grounded Information-seeking Dialogs: A Use Case for Meeting Transcripts](https://aclanthology.org/2024.findings-emnlp.106/).
```
@inproceedings{golany-etal-2024-efficient,
    title = "Efficient Data Generation for Source-grounded Information-seeking Dialogs: A Use Case for Meeting Transcripts",
    author = "Golany, Lotem  and
      Galgani, Filippo  and
      Mamo, Maya  and
      Parasol, Nimrod  and
      Vandsburger, Omer  and
      Bar, Nadav  and
      Dagan, Ido",
    editor = "Al-Onaizan, Yaser  and
      Bansal, Mohit  and
      Chen, Yun-Nung",
    booktitle = "Findings of the Association for Computational Linguistics: EMNLP 2024",
    month = nov,
    year = "2024",
    address = "Miami, Florida, USA",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2024.findings-emnlp.106",
    pages = "1908--1925",
    abstract = "Automating data generation with Large Language Models (LLMs) has become increasingly popular. In this work, we investigate the feasibility and effectiveness of LLM-based data generation in the challenging setting of source-grounded information-seeking dialogs, with response attribution, over long documents. Our source texts consist of long and noisy meeting transcripts, adding to the task complexity. Since automating attribution remains difficult, we propose a semi-automatic approach: dialog queries and responses are generated with LLMs, followed by human verification and identification of attribution spans. Using this approach, we created MISeD {--} Meeting Information Seeking Dialogs dataset {--} a dataset of information-seeking dialogs focused on meeting transcripts. Models finetuned with MISeD demonstrate superior performance compared to off-the-shelf models, even those of larger size. Finetuning on MISeD gives comparable response generation quality to finetuning on fully manual data, while improving attribution quality and reducing time and effort.",
}
```


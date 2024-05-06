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



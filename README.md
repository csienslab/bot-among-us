# Bot Among Us: Exploring User Awareness and Privacy Concerns About Chatbots in Group Chats

This repository contains the artifact accompanying the paper *Bot Among Us: Exploring User Awareness and Privacy Concerns About Chatbots in Group Chats*, to appear in *Proceedings on Privacy Enhancing Technologies (PoPETS), 2026*. The study investigates how users perceive, understand, and respond to privacy risks posed by chatbots in group chat environments across popular messaging platforms.

## Abstract

As chatbots become increasingly integrated into group conversations on instant messaging platforms, concerns arise about their impact on user privacy. While prior research has examined chatbot risks in one-on-one interactions, little is known about how users perceive and respond to privacy threats in group settings, where chatbots may silently access messages and metadata. To address this gap, we conducted an online survey (N=374) across five popular messaging platforms—WhatsApp, Discord, Telegram, Viber, and LINE—to evaluate user awareness, understanding of chatbot access, privacy concerns, and behavioral responses. We found that many users were unaware of bots in their group chats and significantly underestimated their data access: only 41.7\% correctly identified what messages chatbots could access. Privacy concerns also rose sharply after users learned about actual bot permissions. Based on our findings, we propose a five-stage model that captures how users detect, interpret, and respond to chatbot-related privacy risks. We further analyzed the designs of platforms with official chatbot support through this model and found mismatches between design choices and user expectations. Finally, we offer design recommendations to improve transparency and user control in group chatbot-interactions.

## Artifact Overview

The repository contains all data and code necessary to reproduce our quantitative analysis and figures:

* `analysis.ipynb` — Jupyter notebook for reproducing the analysis.
* `Chatbot User Study Cleaned.csv` — anonymized survey dataset.
* `code.csv` — results of qualitative thematic coding of open-ended responses.
* `figures/` — directory containing figures generated in the analysis and used in the paper.
* `questionnaire.md` - full survey instrument, including consent form and all study questions.
* `question_id_mapping.csv` — mapping between survey question IDs and full question text.

## Usage

You can reproduce our analysis using Docker and Jupyter:

```bash
git clone https://github.com/csienslab/bot-among-us.git
cd bot-among-us
docker pull jupyter/datascience-notebook:latest
docker run --rm -p 8888:8888 -v "${PWD}":/home/jovyan/work jupyter/datascience-notebook:latest
```

Open `analysis.ipynb` in Jupyter and select **Kernel → Restart & Run All**. 

## Ethical Considerations

The dataset contains anonymized survey responses collected with informed consent. The study received Institutional Review Board (IRB) approval. All personal identifiers were removed before release.

## Citation

Please cite this work as follows:

```bibtex
@inproceedings{chou2026bot,
  title        = {Bot Among Us: Exploring User Awareness and Privacy Concerns About Chatbots in Group Chats},
  author       = {Chou, Kai-Hsiang and Wang, Yi-An and Lau, Chong Kai and Sharif, Mahmood and Hsiao, Hsu-Chun},
  booktitle    = {Proceedings on Privacy Enhancing Technologies Symposium (PoPETS)},
  year         = {2026},
  volume       = {2026},
  issue        = {1}
}
```
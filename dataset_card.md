---

license: cc-by-4.0
language:

* tr
* en
  multilinguality:
* bilingual
  pretty_name: GameNPC-Dialog Dataset
  size_categories:
* 10K<n<100K
  task_categories:
* text-generation
* conversational
* text-classification
* question-answering
* feature-extraction
  task_ids:
* dialogue-generation
* intent-classification
* text-classification
* question-answering
* semantic-similarity
  tags:
* npc-dialogue
* game-ai
* turkish-nlp
* english-turkish
* task-oriented-dialogue
* social-dialogue
* metaverse
* virtual-reality
* large-language-models
* rag
* fine-tuning
* conversational-agents
  dataset_info:
  features:

  * name: id
    dtype: int64
  * name: domain_id
    dtype: string
  * name: domain
    dtype: string
  * name: npc
    struct:

    * name: role
      dtype: string
    * name: role_style
      dtype: string
    * name: roleplay_style
      dtype: string
  * name: dialogue
    struct:

    * name: question_tr
      dtype: string
    * name: question_en
      dtype: string
    * name: answer_tr
      dtype: string
    * name: answer_en
      dtype: string
  * name: labels
    struct:

    * name: intent
      dtype: string
    * name: player_intent
      dtype: string
    * name: emotion
      dtype: string
    * name: game_context
      dtype: string
    * name: difficulty_level
      dtype: string
  * name: tags
    struct:

    * name: tr
      sequence: string
    * name: en
      sequence: string
      splits:
  * name: train
    num_examples: 91720
    configs:
* config_name: default
  data_files:

  * split: train
    path: data/raw/game_NPC_dataset_raw.jsonl

---

# 🎮 GameNPC-Dialog Dataset

![Dataset](https://img.shields.io/badge/Dataset-GameNPC--Dialog-blue)
![Language](https://img.shields.io/badge/Language-English%20%7C%20Turkish-green)
![Task](https://img.shields.io/badge/Task-NPC%20Dialogue-purple)
![RAG](https://img.shields.io/badge/RAG-Supported-brightgreen)
![Fine--Tuning](https://img.shields.io/badge/Fine--Tuning-Ready-red)
![License](https://img.shields.io/badge/License-CC%20BY%204.0-orange)

## Dataset Summary

**GameNPC-Dialog Dataset** is an **English–Turkish task-oriented and social dialogue dataset** designed for intelligent **Non-Player Character (NPC)** interactions in **digital game**, **metaverse**, and **virtual reality** environments.

The dataset supports the development, fine-tuning, retrieval-augmented generation (RAG), and evaluation of large language model-based NPC dialogue systems. It provides structured dialogue records combining player questions, NPC responses, role information, dialogue intent, emotional tone, game context, difficulty level, and bilingual Turkish-English content.

The dataset is designed to contribute to research on **context-aware**, **role-consistent**, and **goal-oriented NPC communication**, particularly for Turkish and other low-resource language settings.

---

## Dataset Details

### Dataset Description

* **Dataset name:** GameNPC-Dialog Dataset
* **Dataset type:** Bilingual NPC dialogue dataset
* **Languages:** Turkish and English
* **Number of records:** 91,720
* **Primary domain:** Intelligent NPC interaction in digital game environments
* **Supported applications:** RAG, fine-tuning, dialogue generation, intent classification, emotion-aware response generation, and NPC dialogue evaluation

### Authors

| Author              | Affiliation                                                                                                                    | Location        |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------ | --------------- |
| **İbrahim ÖZKAL**   | Tokat Gaziosmanpaşa University, Department of Software, Application Development and Analysis, Game Development and Programming | Tokat / Türkiye |
| **Fatih BAŞÇİFTÇİ** | Selçuk University, Faculty of Technology, Department of Computer Engineering                                                   | Konya / Türkiye |

---

## Intended Uses

The dataset is intended for academic, educational, and research purposes.

Potential uses include:

* Fine-tuning large language models for NPC dialogue generation
* Building retrieval-augmented generation systems for game NPCs
* Training Turkish-English conversational AI systems
* Developing intelligent NPCs for games, metaverse platforms, and VR simulations
* Evaluating dialogue quality, role consistency, and contextual relevance
* Intent, player intent, emotion, and game context classification
* Supporting Turkish NLP research in interactive digital environments

---

## Out-of-Scope Uses

The dataset is not intended for:

* Generating harmful, abusive, deceptive, or manipulative dialogue
* Developing systems for harassment, misinformation, or unsafe persuasion
* Replacing professional medical, psychological, legal, or educational advice
* Collecting or inferring sensitive personal data from users without consent
* Deploying uncontrolled player-facing NPC systems without safety review

Users are responsible for ensuring ethical, lawful, and context-appropriate use.

---

## Dataset Structure

Each record follows a structured JSON format:

```json
{
  "id": 1,
  "domain_id": "EXP_PHY_MEC_001",
  "domain": "physics",
  "npc": {
    "role": "virtual_physics_teacher",
    "role_style": "explanatory",
    "roleplay_style": "supportive"
  },
  "dialogue": {
    "question_tr": "Kuvvet nedir?",
    "question_en": "What is force?",
    "answer_tr": "Kuvvet, bir cismin hareketini veya şeklini değiştirebilen etkidir.",
    "answer_en": "Force is an effect that can change the motion or shape of an object."
  },
  "labels": {
    "intent": "CONCEPT_EXPLAIN",
    "player_intent": "ask_definition",
    "emotion": "informative",
    "game_context": "tutorial",
    "difficulty_level": "very_easy"
  },
  "tags": {
    "tr": ["mekanik", "kuvvet", "temel_kavram"],
    "en": ["mechanics", "force", "basic_concept"]
  }
}
```

---

## Field Descriptions

| Field                     | Description                                               |
| ------------------------- | --------------------------------------------------------- |
| `id`                      | Unique identifier for each dialogue record                |
| `domain_id`               | Detailed scenario or sub-domain identifier                |
| `domain`                  | General domain or topic category                          |
| `npc.role`                | The role or identity of the NPC                           |
| `npc.role_style`          | The communicative or instructional style of the NPC       |
| `npc.roleplay_style`      | The role-playing behavior or interaction style of the NPC |
| `dialogue.question_tr`    | Player question in Turkish                                |
| `dialogue.question_en`    | Player question in English                                |
| `dialogue.answer_tr`      | NPC answer in Turkish                                     |
| `dialogue.answer_en`      | NPC answer in English                                     |
| `labels.intent`           | General communicative intent of the dialogue              |
| `labels.player_intent`    | Player-specific dialogue intention                        |
| `labels.emotion`          | Emotional or tonal category of the response               |
| `labels.game_context`     | In-game context or interaction scenario                   |
| `labels.difficulty_level` | Difficulty level of the dialogue content                  |
| `tags.tr`                 | Turkish semantic tags                                     |
| `tags.en`                 | English semantic tags                                     |

---

## Dataset Domains

The dataset includes multiple NPC interaction domains:

| Domain         | Description                                                |
| -------------- | ---------------------------------------------------------- |
| Expert         | Educational, explanatory, and knowledge-based interactions |
| Roleplay       | Role-playing and narrative interaction scenarios           |
| Metaverse / VR | Immersive virtual environment dialogue scenarios           |
| Daily Dialogue | Everyday social communication and general interaction      |
| Travel         | Travel-related guidance and assistance scenarios           |
| Character      | Character-based NPC interaction scenarios                  |

---

## How to Load the Dataset

After uploading the dataset to Hugging Face, it can be loaded as follows:

```python
from datasets import load_dataset

dataset = load_dataset("your-username/GameNPC-Dialog-Dataset")
print(dataset)
print(dataset["train"][0])
```

For JSONL files:

```python
from datasets import load_dataset

dataset = load_dataset(
    "json",
    data_files="data/raw/game_NPC_dataset_raw.jsonl"
)
print(dataset["train"][0])
```

---

## Example Use for Fine-Tuning

### Input

```text
Generate NPC answer:
domain: physics
npc_role: virtual_physics_teacher
role_style: explanatory
roleplay_style: supportive
intent: CONCEPT_EXPLAIN
player_intent: ask_definition
emotion: informative
game_context: tutorial
difficulty: very_easy
question: Kuvvet nedir?
```

### Output

```text
Kuvvet, bir cismin hareketini veya şeklini değiştirebilen etkidir.
```

---

## Example Use for RAG

A dialogue record can be transformed into a retrieval document:

```text
Domain: physics
NPC Role: virtual_physics_teacher
Role Style: explanatory
Roleplay Style: supportive
Intent: CONCEPT_EXPLAIN
Player Intent: ask_definition
Emotion: informative
Game Context: tutorial
Question: Kuvvet nedir?
Answer: Kuvvet, bir cismin hareketini veya şeklini değiştirebilen etkidir.
Tags: mekanik, kuvvet, temel_kavram
```

This format can be indexed in vector databases such as FAISS, ChromaDB, Weaviate, or Pinecone.

---

## Evaluation

The dataset can support both automatic and human-based evaluation.

### Classification Metrics

* Accuracy
* Precision
* Recall
* F1-score
* Macro-F1
* Weighted-F1
* Confusion matrix

### Dialogue Generation Metrics

* BLEU
* ROUGE
* BERTScore
* Semantic similarity
* Human evaluation
* LLM-based evaluation

### NPC Dialogue Quality Dimensions

| Dimension                 | Description                                                         |
| ------------------------- | ------------------------------------------------------------------- |
| Contextual Relevance      | The response is appropriate to the player question and game context |
| Role Consistency          | The response is consistent with the assigned NPC role               |
| Intent Alignment          | The response satisfies the player’s intent                          |
| Emotional Appropriateness | The tone is suitable for the situation                              |
| Fluency                   | The response is grammatically and semantically clear                |
| Usefulness                | The response helps the player complete or understand the task       |
| Overall Quality           | General quality of the dialogue response                            |

---

## Bias, Risks, and Limitations

Although the dataset is designed to cover multiple NPC interaction domains, it may contain limitations related to:

* Synthetic or semi-synthetic dialogue patterns
* Domain distribution differences
* Label imbalance across intent, emotion, or game context categories
* Cultural assumptions embedded in NPC roles and scenarios
* Differences between dataset dialogue and real player behavior
* Possible translation inconsistencies between Turkish and English fields

Before deployment in real applications, users should conduct additional validation, bias analysis, safety testing, and human evaluation.

---

## Ethical Considerations

Users should consider the following principles:

* AI-generated NPC dialogue should be reviewed before deployment.
* Player-facing systems should include safety and moderation mechanisms.
* Dialogue systems should avoid harmful, discriminatory, manipulative, or unsafe responses.
* User privacy must be protected in interactive systems.
* Age-appropriate and culturally sensitive design should be considered in game scenarios.
* The dataset should be used transparently in academic and applied research.

---

## Citation

If you use this dataset in your research, please cite it as follows:

```bibtex
@dataset{ozkal_gamenpc_dialog_dataset_2026,
  author = {Özkal, İbrahim and Başçiftçi, Fatih},
  title = {GameNPC-Dialog Dataset: Task-Oriented Dataset for Intelligent NPC Interaction in Digital Game Environments},
  year = {2026},
  publisher = {Hugging Face},
  url = {https://huggingface.co/datasets/your-username/GameNPC-Dialog-Dataset},
  license = {CC-BY-4.0}
}
```

---

## License

This dataset is released under the **Creative Commons Attribution 4.0 International License (CC BY 4.0)**.

You are free to share and adapt the dataset, provided that appropriate credit is given.

---

## Contact

For questions, updates, or collaboration requests, please use the Hugging Face discussion page or the GitHub repository issue tracker.

---

## Disclaimer

The dataset is provided “as is” without warranty of any kind. The authors do not guarantee that the dataset is suitable for every downstream application. Users are responsible for ensuring that the dataset is used ethically, legally, and appropriately.

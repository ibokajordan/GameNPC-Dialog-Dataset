# 🎮 GameNPC-Dialog Dataset

🌐 **English–Turkish Task-Oriented and Social Dialogue Dataset for Intelligent NPC Interaction**

---

# 🎮 GameNPC-Dialog Dataset

![Dataset](https://img.shields.io/badge/Dataset-GameNPC--Dialog-blue)
![Language](https://img.shields.io/badge/Language-English%20%7C%20Turkish-green)
![RAG](https://img.shields.io/badge/RAG-Supported-brightgreen)
![Fine--Tuning](https://img.shields.io/badge/Fine--Tuning-Ready-red)
![NPC](https://img.shields.io/badge/NPC-Dialogue-purple)

**GameNPC-Dialog Dataset** is an **English–Turkish task-oriented and social dialogue dataset** designed for intelligent **Non-Player Character (NPC)** interactions in **digital game**, **metaverse**, and **virtual reality** environments.

The dataset supports **fine-tuning**, **retrieval-augmented generation (RAG)**, and evaluation of **large language model-based NPC dialogue systems**.


## 📌 Overview

![Overview](https://img.shields.io/badge/Overview-GameNPC--Dialog-blue)
![GameAI](https://img.shields.io/badge/Game%20AI-Supported-orange)
![Metaverse](https://img.shields.io/badge/Metaverse-Ready-purple)
![ConversationalAI](https://img.shields.io/badge/Conversational%20AI-Compatible-green)

**GameNPC-Dialog Dataset** was developed to support **intelligent dialogue generation** for NPCs in interactive digital environments.

Traditional NPC dialogue systems often rely on **fixed dialogue trees** or **pre-scripted responses**, which may limit **player agency**, **immersion**, and **replayability**. In contrast, modern AI-based NPC systems require **structured**, **annotated**, and **context-rich datasets** to generate adaptive, consistent, and meaningful responses.

This dataset addresses this need by providing a **large-scale Turkish dialogue resource** for NPC interaction scenarios. It can be used in **game AI**, **metaverse applications**, **educational simulations**, **virtual agents**, and **conversational AI systems**.



## 🧩 Dataset Structure

![Structure](https://img.shields.io/badge/Structure-JSON-blue)
![Bilingual](https://img.shields.io/badge/Language-Turkish%20%7C%20English-green)
![NPC](https://img.shields.io/badge/NPC-Role%20Metadata-purple)

Each record in the dataset follows a structured JSON format that includes domain information, NPC metadata, bilingual dialogue content, labels, and semantic tags.

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
## 📊 Field Descriptions

![Schema](https://img.shields.io/badge/Schema-Field%20Descriptions-blue)
![Metadata](https://img.shields.io/badge/Metadata-NPC%20%7C%20Dialogue%20%7C%20Labels-green)
![Language](https://img.shields.io/badge/Language-Turkish%20%7C%20English-orange)
![Tags](https://img.shields.io/badge/Tags-Semantic%20Keywords-purple)

The following table describes the main fields used in the **GameNPC-Dialog Dataset**.

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

## 📄 Citation Metadata

![Citation](https://img.shields.io/badge/Citation-CFF%20Metadata-blue)
![Dataset](https://img.shields.io/badge/Type-Dataset-green)
![Year](https://img.shields.io/badge/Year-2026-orange)
![License](https://img.shields.io/badge/Use-Cite%20Required-purple)
![Research](https://img.shields.io/badge/Research-NPC%20Dialogue-brightgreen)

If you use the **GameNPC-Dialog Dataset** in your research, please cite it using the metadata below.

---

### 🧾 Citation Information

| Field                 | Information                                                                                                |
| --------------------- | ---------------------------------------------------------------------------------------------------------- |
| 📌 **Title**          | GameNPC-Dialog Dataset: Task-oriented dataset for intelligent NPC interaction in digital game environments |
| 🗂️ **Type**          | Dataset                                                                                                    |
| 📅 **Year**           | 2026                                                                                                       |
| 🗓️ **Date Released** | 2026-06-01                                                                                                 |
| 🌐 **Languages**      | English and Turkish                                                                                        |
| 🎮 **Research Area**  | NPC dialogue, game AI, metaverse, virtual reality, large language models                                   |

---

### 👥 Authors

| Author              | Affiliation                                                                                                                    | Location        |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------ | --------------- |
| **İbrahim ÖZKAL**   | Tokat Gaziosmanpaşa University, Department of Software, Application Development and Analysis, Game Development and Programming | Tokat / Türkiye |
| **Fatih BAŞÇİFTÇİ** | Selçuk University, Faculty of Technology, Department of Computer Engineering                                                   | Konya / Türkiye |

---

### 📝 Abstract

**GameNPC-Dialog Dataset** is an **English and Turkish task-oriented and social dialogue dataset** designed for intelligent **Non-Player Character (NPC)** interactions in **digital game**, **metaverse**, and **virtual reality** environments.

The dataset supports research on **context-aware**, **role-consistent**, and **goal-oriented NPC dialogue generation**, as well as **retrieval-augmented generation (RAG)**, **fine-tuning**, and evaluation of **large language model-based NPC systems**.

---

### 🔑 Keywords

![NPC Dialogue](https://img.shields.io/badge/NPC-dialogue-blue)
![Game Dataset](https://img.shields.io/badge/Game-dialogue%20dataset-green)
![Turkish NLP](https://img.shields.io/badge/Turkish-NLP-red)
![Task-Oriented](https://img.shields.io/badge/Task--oriented-dialogue-orange)
![Social Dialogue](https://img.shields.io/badge/Social-dialogue-purple)
![Metaverse](https://img.shields.io/badge/Metaverse-ready-lightgrey)
![VR](https://img.shields.io/badge/Virtual-Reality-blueviolet)
![LLM](https://img.shields.io/badge/Large%20Language-Models-brightgreen)
![RAG](https://img.shields.io/badge/RAG-supported-yellow)
![Fine-Tuning](https://img.shields.io/badge/Fine--tuning-ready-critical)
![Game AI](https://img.shields.io/badge/Game-AI-informational)
![Conversational Agents](https://img.shields.io/badge/Conversational-Agents-success)

---

### 📌 CITATION.cff Preview

```yaml
message: "If you use this dataset in your research, please cite it using the metadata below."
title: "GameNPC-Dialog Dataset: Task-oriented dataset for intelligent NPC interaction in digital game environments"
type: dataset

authors:
  - family-names: "Özkal"
    given-names: "İbrahim"
    affiliation: "Tokat Gaziosmanpaşa University, Department of Software, Application Development and Analysis, Game Development and Programming"
    country: "Tokat/Türkiye"

  - family-names: "Başçiftçi"
    given-names: "Fatih"
    affiliation: "Selçuk University, Faculty of Technology, Department of Computer Engineering"
    country: "Konya/Türkiye"

year: 2026
date-released: 2026-06-01

abstract: "GameNPC-Dialog Dataset is English and Turkish task-oriented and social dialogue dataset designed for intelligent Non-Player Character (NPC) interactions in digital game, metaverse, and virtual reality environments. The dataset supports research on context-aware, role-consistent, and goal-oriented NPC dialogue generation, as well as retrieval-augmented generation, fine-tuning, and evaluation of large language model-based NPC systems."

keywords:
  - "NPC dialogue"
  - "game dialogue dataset"
  - "Turkish NLP"
  - "task-oriented dialogue"
  - "social dialogue"
  - "metaverse"
  - "virtual reality"
  - "large language models"
  - "retrieval-augmented generation"
  - "fine-tuning"
  - "game AI"
  - "conversational agents"
```

---

# Dataset Schema

![Schema](https://img.shields.io/badge/Schema-GameNPC--Dialog-blue) ![Format](https://img.shields.io/badge/Format-JSONL%20%7C%20JSON%20%7C%20CSV-green) ![Languages](https://img.shields.io/badge/Languages-English%20%7C%20Turkish-orange) ![Task](https://img.shields.io/badge/Task-NPC%20Dialogue-purple)

This document defines the main schema of the **GameNPC-Dialog Dataset**. The dataset is designed for intelligent Non-Player Character (NPC) interactions in digital game, metaverse, and virtual reality environments.

## Dataset-Level Statistics

| Metric | Value |
| --- | --- |
| Total records | 91,675 |
| Number of domains | 32 |
| Number of domain IDs | 91,675 |
| Number of NPC roles | 76 |
| Number of role styles | 36 |
| Number of roleplay styles | 36 |
| Number of intent labels | 37 |
| Number of player intent labels | 25 |
| Number of emotion labels | 40 |
| Number of game context labels | 30 |
| Number of difficulty levels | 5 |


## Record Structure

Each record follows a structured JSON-based format:

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

## Field Descriptions

| Field | Type | Description |
|---|---|---|
| `id` | integer | Unique identifier for each dialogue record |
| `domain_id` | string | Detailed scenario or sub-domain identifier |
| `domain` | string | General domain or topic category |
| `npc.role` | string | Role or identity of the NPC |
| `npc.role_style` | string | Communicative, instructional, or narrative style of the NPC |
| `npc.roleplay_style` | string | Role-playing behavior or interaction style of the NPC |
| `dialogue.question_tr` | string | Player question or utterance in Turkish |
| `dialogue.question_en` | string | Player question or utterance in English |
| `dialogue.answer_tr` | string | NPC response in Turkish |
| `dialogue.answer_en` | string | NPC response in English |
| `labels.intent` | categorical string | General communicative intent of the dialogue |
| `labels.player_intent` | categorical string | Player-specific dialogue intention |
| `labels.emotion` | categorical string | Emotional or tonal category of the NPC response |
| `labels.game_context` | categorical string | In-game context or interaction scenario |
| `labels.difficulty_level` | categorical string | Difficulty level of the dialogue content |
| `tags.tr` | list of strings | Turkish semantic tags |
| `tags.en` | list of strings | English semantic tags |

## Recommended Use in RAG

For retrieval-augmented generation, the following fields are recommended as metadata:

- `domain`
- `npc.role`
- `npc.role_style`
- `npc.roleplay_style`
- `labels.intent`
- `labels.player_intent`
- `labels.emotion`
- `labels.game_context`
- `labels.difficulty_level`
- `tags.tr`
- `tags.en`

## Recommended Use in Fine-Tuning

For supervised fine-tuning, the input may include domain, NPC, label, and question fields, while the output should be the corresponding NPC answer.

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

```text
Kuvvet, bir cismin hareketini veya şeklini değiştirebilen etkidir.
```

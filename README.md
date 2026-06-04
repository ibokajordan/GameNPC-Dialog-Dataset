# GameNPC-Dialog-Dataset
GameNPC-Dialog Dataset is English and Turkish  task-oriented and social dialogue dataset designed for intelligent NPC interactions in digital game, metaverse, and VR environments.


GameNPC-Dialog Dataset

GameNPC-Dialog Dataset is English - Turkish task-oriented and social dialogue dataset designed for intelligent Non-Player Character (NPC) interactions in digital game, metaverse, and virtual reality environments. The dataset aims to support the development, fine-tuning, retrieval-augmented generation (RAG), and evaluation of large language model-based NPC dialogue systems.

The dataset provides structured dialogue samples that combine player questions, NPC responses, role information, dialogue intent, emotional tone, game context, difficulty level, and bilingual Turkish-English content. It is designed to contribute to research on context-aware, role-consistent, and goal-oriented NPC communication, particularly for low-resource language settings.

Overview

GameNPC-Dialog Dataset was developed to support intelligent dialogue generation for NPCs in interactive digital environments. Traditional NPC dialogue systems often rely on fixed dialogue trees or pre-scripted responses, which may limit player agency, immersion, and replayability. In contrast, modern AI-based NPC systems require structured, annotated, and context-rich datasets to generate adaptive, consistent, and meaningful responses.

This dataset addresses this need by providing a large-scale Turkish dialogue resource for NPC interaction scenarios. It can be used in game AI, metaverse applications, educational simulations, virtual agents, and conversational AI systems.

Key Features
Turkish task-oriented and social NPC dialogue data
Bilingual dialogue fields in Turkish and English
Structured NPC role and personality-style metadata
Intent, player intent, emotion, game context, and difficulty annotations
Suitable for RAG-based NPC systems
Suitable for fine-tuning large language models
Designed for digital games, metaverse environments, and VR-based interaction systems
Supports research on Turkish natural language processing and game dialogue generation

Dataset Structure

Each record in the dataset follows a structured format:

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

Field Descriptions
Field	Description
id	Unique identifier for each dialogue record
domain_id	Detailed scenario or sub-domain identifier
domain	General domain or topic category
npc.role	The role or identity of the NPC
npc.role_style	The communicative or instructional style of the NPC
npc.roleplay_style	The role-playing behavior or interaction style of the NPC
dialogue.question_tr	Player question in Turkish
dialogue.question_en	Player question in English
dialogue.answer_tr	NPC answer in Turkish
dialogue.answer_en	NPC answer in English
labels.intent	General communicative intent of the dialogue
labels.player_intent	Player-specific dialogue intention
labels.emotion	Emotional or tonal category of the response
labels.game_context	In-game context or interaction scenario
labels.difficulty_level	Difficulty level of the dialogue content
tags.tr	Turkish semantic tags
tags.en	English semantic tags
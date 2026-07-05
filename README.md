# Opening-as-Task MAML for Cross-Game Position Evaluation

This repository contains code for a meta-learning research project exploring whether strategic representations learned from one abstract strategy game can transfer to another. The project uses Model-Agnostic Meta-Learning (MAML) to treat chess openings as tasks, with the goal of learning an initialization that can adapt efficiently across game states and eventually support transfer from Chess to Shogi.

**Status:** Pending publication at AIIDE.

## Project Overview

Traditional supervised models for board-game evaluation often require large amounts of game-specific data. This project investigates whether meta-learning can reduce that dependency by training models to adapt quickly across related strategic tasks.

The core idea is to frame different chess openings as separate learning tasks. A MAML-based model is trained across these tasks so that it can learn a strong shared initialization and adapt to new positions or openings with fewer gradient updates.

## Repository Structure

```text
opening-task-maml/
├── action_encoding_chess.py
├── db_preprocess_chess.py
├── encode_chess.py
├── losses.py
├── maml_alg2.py
├── maml_fomaml.py
├── model.py
├── parser.py
├── sanity_check.py
├── spec.py
├── task_sampler.py
├── test_task_sampler.py
└── train_maml_chess.py

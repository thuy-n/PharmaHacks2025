# PharmaHacks 2025: Multiple Sequence Alignment for Antimicrobial Resistance 🧬

## Overview
This repository contains our solution for the PharmaHacks McGill 2025 challenge, **"Multiple Sequence Alignment for Antimicrobial Resistance"**. 

## Problem Description
Antimicrobial resistance is a phenomenon that occurs when microorganisms such as bacteria, germs or viruses develop the ability to resist drugs that are used to
treat them. It usually happens when a drug has been overprescribed. This is very problematic as designing new drugs is time-consuming and very expensive. To avoid this problem, a technique has become more and more popular: **multiple sequence alignment (MSA)**. However, MSA is an NP-hard problem, making it computationally challenging. 

Citizen science initiatives, such as **Borderlands Science**, have shown that human intuition can be very effective in solving parts of these challenges, and our approach aims to mimic that human expertise using machine learning.

## Inspiration 

Recent research has explored reinforcement learning (RL) for MSA, demonstrating promising results. Our work is inspired by:

- RLALIGN ([Ramakrishnan et al., 2018](https://ieeexplore.ieee.org/document/8567458))​, which introduced an A3C-based RL method for MSA and showed that reinforcement learning could outperform classical progressive alignment algorithms.
- Deep Reinforcement Learning with Self-Attention for MSA ([Liu et al., 2023](https://doi.org/10.1093/bioinformatics/btad636_))​, which leveraged self-attention mechanisms and positional encoding to improve accuracy.
  
We set out to build an AI model that learns optimal gap insertion strategies from human intuition using RL.

## Our Solution: Gappy ⭐️
Gappy leverages Actor-Critic Reinforcement Learning to optimize MSA. Instead of relying on fixed heuristic rules, Gappy learns the best alignment strategies through trial and error, inserting gaps to maximize sequence similarity while following biological constraints.

## Key Features

- **Custom RL Environment** – Simulates MSA puzzles with a reward function inspired by biological heuristics.
- **Action Masking** – Prevents invalid moves (e.g., inserting gaps where they don’t improve the alignment).
- **Convolutional Neural Networks (CNNs)** – Extracts structural patterns from sequences to guide alignment decisions.
- **Actor-Critic Architecture** – Balances exploration (testing new gap insertions) with exploitation (optimizing scores).
- **Human-readable Move Tracking** – Implements human-readable move tracking and visualization tools for explainability.

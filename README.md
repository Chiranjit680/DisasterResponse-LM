# DisasterResponse-LM
Disaster Response Transformer

A 14.3M-parameter decoder-only transformer model trained for next-token prediction and disaster-related response generation.

Overview

This project implements a transformer language model from scratch, pretraining it on a large general-purpose text corpus and then fine-tuning it on emergency-oriented datasets such as 911 call transcripts and disaster-response reports.
The model specializes in generating coherent, actionable text suitable for crisis communication.

Key Features

Custom 14.3M-parameter Decoder-Only Transformer
Fully implemented without relying on high-level transformer libraries.

Two-Stage Training Pipeline

Pretraining: BookCorpus for general language modeling

Fine-Tuning: 911 call transcripts + disaster-response documents

Complete Training Pipeline Implemented Manually

Data cleaning and normalization

Custom word-level tokenization

Learning-rate scheduling (warmup + cosine decay)

Gradient clipping for stability

Mini-batch dataloader and periodic checkpointing

Performance
Achieved 174 perplexity, enabling reliable generation of disaster-response text.

Architecture

Decoder-only transformer

Multi-head self-attention

Learnable positional embeddings

Feed-forward blocks with LayerNorm

Cross-entropy loss (teacher forcing)

Adam optimizer with LR scheduler

Datasets Used

BookCorpus – Pretraining

911 Call Transcripts – Fine-tuning

Disaster Response Documents – Domain adaptation

All datasets are publicly available or synthetically generated for research use only.

Training Workflow

Preprocess raw text (cleaning, normalization, filtering)

Tokenize with custom vocabulary

Create training sequences

Train with warmup + cosine LR decay

Evaluate perplexity and sample generations

Fine-tune on emergency datasets

Generate disaster-response outputs

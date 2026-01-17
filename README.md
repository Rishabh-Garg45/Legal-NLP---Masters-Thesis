# Argument Mining in Indian Legal Texts

This repository contains the code, experiments, and notebooks developed as part of my **thesis project titled *“Argument Mining in Indian Legal Texts”***. The work explores how modern NLP techniques—particularly Large Language Models (LLMs) and Natural Language Inference (NLI)—can be applied to identify and classify argumentative structures (claims, premises, relations) in Indian legal judgments.

The project focuses on **argument classification and entailment-based reasoning** over legal text, with experiments conducted on the **LREC 2022 Argument Mining dataset**, adapted for the Indian legal domain.

---

## Project Overview

Argument Mining (AM) aims to automatically extract argumentative components such as **claims**, **premises**, and their **logical relations** from unstructured text. Indian legal judgments pose unique challenges due to:

* Long and complex sentence structures
* Domain-specific legal vocabulary
* Implicit reasoning and precedential references

This thesis investigates:

* Zero-shot and few-shot argument classification using LLMs
* LLM-assisted annotation pipelines
* Evaluation of Natural Language Inference (NLI) models on legal argument pairs
* The feasibility of LLMs as judges for argument classification

---

## Dataset

* **Dataset used:** LREC 2022 Argument Mining Dataset
* **Domain:** Legal texts (adapted for Indian legal judgments)
* **Usage:**

  * Argument label classification
  * NLI-based entailment/contradiction detection
  * LLM-based annotation and evaluation

All experiments in this repository are conducted on subsets or derived versions of this dataset.

---

## Repository Structure & File Descriptions

### 1. `llm-annotator (1).ipynb`

**Purpose:** Zero-shot LLM-based argument classification

* Implements a **zero-shot approach** for identifying argument labels
* Uses an LLM without task-specific training
* Serves as a baseline to understand raw LLM capabilities on legal argument mining
* No few-shot examples or external supervision provided

---

### 2. `final-label-classification.ipynb`

**Purpose:** Few-shot argument classification with LLM-as-a-Judge

* Implements **few-shot learning** for argument classification
* **SaulLM** is used to **annotate** argument labels
* **Mistral** is used as an independent **LLM judge** to evaluate and validate predictions
* Demonstrates an LLM-assisted annotation and evaluation pipeline
* Core experiment for argument label classification

---

### 3. `label-classification-evaluation.ipynb`

**Purpose:** Evaluation of argument classification performance

* Computes performance metrics for argument classification
* Includes comparison between:

  * LLM predictions
  * Gold-standard annotations
* Used to analyze effectiveness of zero-shot vs few-shot setups

---

### 4. `nli-testing.ipynb`

**Purpose:** Preliminary testing of NLI model behavior

* Tests the working of a **Natural Language Inference (NLI) model**
* Uses **manually created few examples** to validate:

  * Entailment
  * Contradiction
  * Neutral relations
* Helps verify whether the NLI model behaves sensibly on legal-style inputs before large-scale experiments

---

### 5. `NLI-Final.ipynb`

**Purpose:** NLI-based reasoning on legal argument pairs

* Applies an NLI model on **~1000 argument pairs** from the legal dataset
* Evaluates entailment and contradiction relations between premises and claims
* Forms the basis for analyzing logical consistency in legal arguments
* Key experiment connecting argument mining with inference-based reasoning

---

### 6. `lrec-inlegal-bert-classification.ipynb`

**Purpose:** Transformer-based classification baseline

* Uses **InLegalBERT** for supervised argument classification
* Serves as a non-LLM baseline for comparison
* Helps contrast traditional fine-tuned transformer models with LLM-based approaches

---

## Methods Used

* **Zero-shot learning** with LLMs
* **Few-shot learning** for argument classification
* **LLM-as-Annotator** (SaulLM)
* **LLM-as-a-Judge** (Mistral)
* **Natural Language Inference (NLI)** for argument relation validation
* **Transformer-based supervised classification** (InLegalBERT)

---

## Key Contributions

* Demonstrates the applicability of LLMs for argument mining in Indian legal texts
* Shows how LLMs can assist in annotation and evaluation pipelines
* Evaluates NLI models on legal argument pairs
* Provides a comparative analysis between LLM-based and transformer-based methods

---

## Requirements

* Python 3.8+
* PyTorch
* HuggingFace Transformers
* Access to LLM APIs / models (SaulLM, Mistral)

(Exact dependencies may vary per notebook; please refer to individual notebooks for details.)

---

## Thesis Context

This repository is part of an academic thesis submitted in partial fulfillment of degree requirements. The experiments and notebooks reflect iterative research and exploration rather than production-ready pipelines.

---

## Author

**Rishabh Garg**
IIT Madras
Thesis Project: *Argument Mining in Indian Legal Texts*

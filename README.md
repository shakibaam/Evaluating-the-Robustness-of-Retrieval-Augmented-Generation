# Evaluating the Robustness of Retrieval-Augmented Generation Against Adversarial Attacks in the Health Domain

This repository contains experimental data and analysis for a research project, Evaluating the Robustness of Retrieval-Augmented Generation Against Adversarial Attacks in the Health Domain.

## Project Overview

ToDO

## Repository Structure

### 📊 Experiment Results (`Experiment_Results/`)


##### 1. Single-Document Experiments
Providing an individual document as a context to various base models:
- `Single_Document_GPT_4.1/`
- `Single_Document_GPT_5/`
- `Single_Document_Claudi_3.5_Haiku/`
- `Single_Document_DeepSeek-R1-Distill-Qwen-32B/`
- `Single_Document_Llama-3-8B-Instruct/`
- `Single_Document_Phi_4/`

Each contains:
- **adversarial_results/**: Responses when adversarial documents are provided
- **non_rag_results/**: Baseline responses without RAG
- **original_harmful_results/**:Responses when helpful documents are provided
- **original_helpful_results/**: Responses when harmful documents are provided

##### 2. Paired Document Experiments
- `Paired_Document_GPT_4.1/`: Paired-document results

##### 3. Pooling Strategy Experiments
- `Biased_Controlled_Pooling_GPT_4.1/`
- `Realistic_Pooling_GPT_4.1/`

#### Result Categories
Each experiment is evaluated across three consistency categories:
- **consistent_results/**: Results for consistent prompts
- **inconsistent_results/**: Results for inconsistent prompts  
- **neutral_results/**: Results for neutral prompts

#### Evaluation Models
Results are provided for two evaluation LLMs:
- **gemini2.0flash/**
- **gpt4omini/**

### 📈 Visualizations (`Plots/`)

Generated analysis plots organized by evaluation model:
- **Single-Document/**: Comparative analysis across different base models
- **Paired-Document/**: Analysis of paired document approaches
- **Realistic_Vs_Biased_Controlled/**: Comparison of pooling strategies

### 📝 Prompts (`Prompts/`)

Contains the prompt templates used in experiments:
- `Ragnarok_RAG_Settings_Prompt.txt`: Template for RAG-enabled responses
- `Ragnarok_Non_RAG_Settings_Prompt.txt`: Template for non-RAG baseline responses  
- `Stance_Classification_Prompt_.txt`: Template for stance classification evaluation

## Data Format

### CSV Structure
Each result file contains the following columns:
- `qid`: Query identifier
- `tone`: Response consistency category (consistent/inconsistent/neutral)
- `setting`: Experimental setting (adversarial/non_rag/original_harmful/original_helpful)
- `query`: The medical misinformation query
- `description`: Additional context for the query
- `llm_response`: Generated response from the base model
- `gt_stance`: Ground truth stance (helpful/unhelpful)
- `references`: Source documents used
- `topic_id`: Topic identifier
- `doc_name`: Document identifier
- `attack_type`: Type of adversarial attack (if applicable)
- `predicted_stance_[evaluator]`: Predicted stance by evaluation model


## Citation

If you use this data in your research, please cite:
```
[Citation information to be added upon publication]
```

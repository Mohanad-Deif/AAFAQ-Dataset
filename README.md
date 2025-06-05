# AAFAQ Dataset - Arabic Question Classification

This repository provides tools and scripts for training, evaluating, and visualizing results using the **AAFAQ Dataset**, a benchmark dataset for Arabic question classification based on the **AAFAQ Framework**. The dataset includes **5,009 Modern Standard Arabic (MSA) questions**, each annotated across **11 linguistic and cognitive dimensions**.

## 🧠 What is AAFAQ?
AAFAQ (Arabic Analytical Framework for Advanced Questions) is a multi-layer taxonomy that allows for the semantic, cognitive, and contextual analysis of Arabic questions. It supports fine-grained classification for tasks such as:
- Arabic Question Answering Systems (QAS)
- Cognitive skill assessment
- Multilingual NLP systems

## 📁 Repository Structure

```
├── arabic_qa_aafaq.py               # Full pipeline for training and evaluation using AraBERT
├── AAFAQ_Figures_Generator.ipynb    # Notebook to generate all paper figures
├── AAFAQ_Dataset.csv                # Main dataset (15 columns, 5009 rows)
├── arabert-aafaq-model/             # Folder where trained model is saved (after training)
├── README.md                        # This file
```

## 📊 Dataset Features
Each question is annotated with the following features:
- `QuestionParticle`
- `QuestionParticleType`
- `QuestionType`
- `List`
- `AnswerType`
- `Intent`
- `CognitiveLevel`
- `Category`
- `Subjectivity`
- `TemporalContext`
- `PurposeContext`

## 🚀 Usage Instructions

### 1. Setup
Install dependencies:
```bash
pip install transformers datasets pandas scikit-learn matplotlib seaborn
```

### 2. Train the Classifier
Run the script:
```bash
python arabic_qa_aafaq.py
```
This will load the dataset, fine-tune **AraBERT**, and save the model in `./arabert-aafaq-model/`.

### 3. Visualize Paper Figures
Open and run all cells in:
```bash
AAFAQ_Figures_Generator.ipynb
```
This will generate bar plots and a correlation matrix for all major features.

## 📈 Model Performance (as reported)
- **Question Particle Type**: 100% accuracy (AraBERT)
- **Intent Classification**: 94.95% accuracy
- **Answer Type Classification**: 91.85% accuracy

## 🧪 Advanced Features
- Multi-label classification using `transformers.Trainer`
- Visualizations of distribution and correlations
- Cramér's V for categorical feature association

## 📚 References
Dataset and methodology described in the paper:
> *A Benchmark Arabic Dataset for Question Classification using AAFAQ Framework* by Mariam Essam et al., 2025.


---

For dataset access or academic use, visit the http://datadryad.org/stash/share/IGdeANoM7cUWlMr-iUhGQMvuJgWLXicCBvXutXVUnas 

GitHub Repo (for scripts): https://github.com/Mariam-Essam/Arabic-Question-Classifications-with-AAFAQ


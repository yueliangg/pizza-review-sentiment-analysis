# Pizza Review Sentiment Analysis Using RNN and LSTM

**Deep Learning | Natural Language Processing | Sentiment Classification**

A deep learning project focused on classifying pizza reviews into **three sentiment categories** using Recurrent Neural Networks (RNNs) and Long Short-Term Memory (LSTM) networks.

The project compares a **SimpleRNN model** with an improved **LSTM-based model**, focusing on classification performance, model generalisation and the challenges of interpreting natural language. Experiments examine how different recurrent architectures perform on review text and how model improvements affect accuracy and classification reliability.

## Results

| Model | Test Accuracy |
|---|---:|
| SimpleRNN | 83.05% |
| **Improved LSTM** | **87.29%** |

**Key achievement:** Improved test accuracy by **4.24 percentage points**, from **83.05% to 87.29%**, with the improved LSTM achieving a **weighted F1-score of 0.8736**.

## Project Objectives

- Develop neural network models for three-class sentiment classification of pizza reviews.
- Compare the performance of SimpleRNN and LSTM architectures.
- Investigate model improvements and their impact on classification accuracy.
- Evaluate model generalisation using performance metrics and error analysis.
- Identify challenges in classifying ambiguous, context-dependent and potentially noisy review text.

## Dataset and Preprocessing

**Dataset:** Pizza review text used for three-class sentiment classification.

The project involves preparing textual review data for recurrent neural network models.

The data preparation workflow is centred on:

- **Text processing:** Preparing review text for neural network input.
- **Sequence representation:** Converting text into numerical sequences suitable for recurrent architectures.
- **Label preparation:** Representing the three sentiment categories for supervised learning.
- **Model input preparation:** Organising the processed sequences and labels for training and evaluation.

The exact dataset size, class distribution, preprocessing parameters and train/test split should be documented from the original notebooks rather than assumed.

## Model Development

### Part A — SimpleRNN Model

Developed and evaluated a SimpleRNN-based sentiment classifier to establish a performance reference for three-class review classification.

SimpleRNN processes text sequences through recurrent connections, allowing information from earlier sequence positions to influence later representations.

**Test Accuracy: 83.05%**

The SimpleRNN experiment provides a basis for comparing subsequent model improvements.

### Part B — Improved LSTM Model

Developed and evaluated an improved LSTM-based classifier for the same sentiment classification task.

Unlike a standard SimpleRNN, LSTM uses gating mechanisms to regulate information flow through the network, supporting the modelling of longer-range dependencies within text sequences.

**Test Accuracy: 87.29%**

**Weighted F1-Score: 0.8736**

The improved LSTM achieved higher test accuracy than the SimpleRNN model in the reported experiments.

## Evaluation and Findings

Model performance was examined using **test accuracy, classification metrics and analysis of prediction errors**.

The improved LSTM achieved a **4.24 percentage-point increase in test accuracy** over the SimpleRNN result.

The experiments also highlighted several challenges associated with sentiment classification:

- **Ambiguous reviews:** Review text may contain mixed or unclear sentiment.
- **Negation:** Phrases involving negation can change the interpretation of otherwise positive or negative terms.
- **Noisy labels:** Differences between review wording and assigned sentiment labels can complicate learning.
- **Generalisation:** Good training performance does not necessarily translate into reliable predictions on unseen reviews.

These findings demonstrate why classification performance should be evaluated using more than overall accuracy.

## Key Takeaways

- The improved LSTM outperformed the SimpleRNN model on the reported test results.
- Recurrent architecture selection can affect sentiment classification performance.
- The weighted F1-score provides additional information about predictive performance across sentiment categories.
- Error analysis is important for understanding limitations that aggregate metrics may not reveal.
- Model improvements should be assessed using held-out data rather than training performance alone.

## Tech Stack

- **Language:** Python
- **Deep Learning:** TensorFlow, Keras
- **Neural Network Architectures:** SimpleRNN, LSTM
- **Domain:** Natural Language Processing, Sentiment Analysis, Text Classification
- **Evaluation:** Classification Accuracy, Precision, Recall, F1-Score
- **Development Environment:** Jupyter Notebook

## Repository Contents

```text
.
├── README.md
├── Part_A.ipynb             # SimpleRNN model and evaluation
├── Part_B.ipynb             # Improved LSTM experiments
├── requirements.txt
├── .gitignore
└── docs/
    ├── Part_A_Results.html
    └── Part_B_Results.html
```

*This is a recommended repository structure. File names and directories should be adjusted to match the files actually uploaded.*

## How to Run

1. Clone or download this repository.

2. Create and activate a Python virtual environment.

3. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Obtain the pizza review dataset used for the original experiments and configure the notebook's dataset path accordingly.

5. Launch Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

6. Open `Part_A.ipynb` to review the SimpleRNN experiments.

7. Open `Part_B.ipynb` to review the improved LSTM experiments.

8. Execute the notebook cells in sequence to reproduce the experiments, provided the dataset and required dependencies are available.

**Note:** Exact results may vary depending on random states, software versions and execution environments. The repository should document any changes made when converting the original notebooks for public sharing.

## Future Improvements

- **Pretrained word embeddings:** Investigate whether pretrained representations improve sentiment classification.
- **Bidirectional LSTM:** Explore whether incorporating information from both sequence directions improves predictions.
- **Transformer-based models:** Compare recurrent models against modern transformer architectures.
- **Class-level analysis:** Investigate whether particular sentiment categories contribute disproportionately to prediction errors.
- **Robustness testing:** Evaluate performance on reviews containing negation, mixed sentiment and unfamiliar vocabulary.

## Context

Developed as an individual academic deep learning project in the **Diploma in Applied AI & Analytics at Singapore Polytechnic**.

The reported metrics reflect the results of the original project experiments and should not be interpreted as performance guarantees on reviews from other datasets or real-world applications.

## Author

**Thawdar Lin Wai**

Diploma in Applied AI & Analytics  
Singapore Polytechnic

[LinkedIn](https://www.linkedin.com/in/thawdarlinwai/) | [GitHub](https://github.com/yueliangg)

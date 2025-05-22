# Detection of Antisocial Behavior using LLMs

This repository contains the full codebase and models from my bachelor thesis project focused on detecting antisocial and toxic behavior using Large Language Models (LLMs).

The main goal of this project was to fine-tune a LLaMA 3.2 model to classify comments into six toxicity categories, with experiments using prompt variations (with and without SYSTEM messages) and quantized model formats (q4_k_m).

---

##  Repository Contents

### 🔍 Models (`/models`)
- Quantized models in `q4_k_m` format.
- Versions **with** and **without** the SYSTEM prompt message.
- Includes base model before training.

###  Testing (`/testing`)
- Scripts to run inference on new comments.
- Accepts CSV input and outputs category predictions.

###  Training (`/training`)
- Code to fine-tune models using prepared datasets.
- Works with Unsloth or similar fine-tuning libraries.

###  Data Preparation (`/data_prep`)
- Scripts to clean and prepare raw data.
- Converts data into proper format for training and inference.

### 📄 Prompts (`/prompts`)
- Templates for LLM input:
  - `with_SYSTEM`: includes system-level instruction block.
  - `no_SYSTEM`: simple prompt without system message.

---

###  Dataset

This project uses the **Jigsaw Toxic Comment Classification Challenge** dataset, released by **Google/Jigsaw in 2018**.

- [Kaggle dataset link](https://www.kaggle.com/competitions/jigsaw-toxic-comment-classification-challenge)
- Classification of text into:
  - toxic
  - severe_toxic
  - obscene
  - threat
  - insult
  - identity_hate
- Uses `yes`/`no` labeling format for simplicity.
- Lightweight quantized models (`q4_k_m`) for efficient inference.


---

##  Notes

- This project is for research and educational purposes.
- Model outputs should be evaluated responsibly in real-world scenarios.

###  Libraries Used in This Project

| Library             | Version     | Purpose                                             |
|---------------------|-------------|-----------------------------------------------------|
| `pandas`            | 1.5.3       | Data manipulation and preprocessing                 |
| `tqdm`              | 4.67.1      | Progress bars for loops                             |
| `unsloth`           | 2025.3.17   | Fine-tuning LLaMA models                            |
| `scikit-learn`      | 1.3.0       | Evaluation metrics (e.g., F1 score, accuracy)       |
| `langchain-ollama`  | 0.3.0       | Using LLMs via LangChain and Ollama integration     |
| `torch`             | 2.5.1       | Core deep learning framework                        |
| `transformers`      | 4.48.0      | Hugging Face library for working with LLMs          |

---

## Author

Bachelor Thesis by **Yurii Kostiuk**  
Faculty of Electrical Engineering and Informatics, TUKE

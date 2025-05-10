# IBM-GenAI-Project

Code Generation from Natural Language using T5

## 🔍 Overview

This project demonstrates how **Generative AI** models like **T5** can be fine-tuned to generate **Python code** from natural language prompts. It showcases the application of NLP techniques in transforming user queries into executable code, highlighting the growing power of language models in software development automation.

---

## 📌 Project Phases

### ✅ Phase 1: Proposal and Idea Submission

- **Objective:**  
  To design a system that takes natural language instructions and generates relevant Python code using a transformer-based generative model.

- **Problem Statement:**  
  Developers often need to write boilerplate or repetitive code based on textual descriptions. This project aims to automate that using a model trained to "translate" plain English into Python code.

- **Proposed Solution:**  
  Fine-tune the **T5 model** on paired English instruction–Python code data and deploy a basic interface for query-to-code generation.

- **Tools Planned:**  
  Python, HuggingFace Transformers, Google Colab, Weights & Biases (W&B)

---

### ⚙️ Phase 2: Project Execution & Demonstration

- **Implementation Highlights:**
  - Fine-tuned the `t5-base` model on a dataset of English instructions and Python code.
  - Built a **terminal-based interface** for real-time code generation.
  - Created a function that accepts a user query, tokenizes it, and generates a code snippet using the trained model.
  - Used **W&B** for experiment tracking and monitoring during model training.

- **Technologies Used:**
  - Python
  - HuggingFace Transformers
  - Google Colab
  - Weights & Biases (W&B)

- **How It Works:**
  1. User enters a query (e.g., "print a list in python").
  2. Model processes the query and returns generated Python code.
  3. Output is printed in terminal for review or execution.

---

### 📊 Phase 3: Final Evaluation & Testing

- **Testing Strategy:**
  - Evaluated model output on various prompt types.
  - Conducted **unit, integration, user, and edge case testing**.
  - Used **W&B** to track loss curves and training parameters.

- **Performance:**
  - Fast and responsive inference.
  - High accuracy on prompts similar to training data.
  - Robust handling of edge cases, although generalization was limited to in-distribution data.

- **Limitations:**
  - Performance degrades on queries outside training scope.
  - No error checking on generated code yet.

- **Future Enhancements:**
  - Add web UI via Streamlit or Flask.
  - Expand dataset for better generalization.
  - Integrate real-time syntax checking.
  - Extend to support multiple languages (e.g., JS, C++).

---

## 🚀 How to Run

### Step 1. Clone this Repository
```bash
git clone https://github.com/your-username/codegen-t5.git
cd codegen-t5
```

### Step 2. Install Required Dependencies

```bash
pip install transformers torch
pip install wandb
```

### Step 3. Load the Fine-Tuned Model

```bash
model = T5ForConditionalGeneration.from_pretrained("/content/t5_finetuned")
tokenizer = T5Tokenizer.from_pretrained("/content/t5_finetuned")
```

### Step 4. Run the Application
Launch the script from the terminal

```bash
python main.py
```
---

## Output

![image](https://github.com/user-attachments/assets/3dd15777-498a-4a05-9318-664768ef8cbd)


![image](https://github.com/user-attachments/assets/ffce7100-882d-4b2f-810f-91f7a851185d)


**Weights & Biases (W&B)** is a powerful tool used in this project for experiment tracking and performance monitoring during model fine-tuning.
- By integrating W&B with the training pipeline, we were able to visualize training metrics such as loss, learning rate, and evaluation scores in real-time.
- This helped in better understanding the training behavior and allowed for easier comparison between different runs or configurations.
- W&B also stores logs and artifacts, making the development process more reproducible and collaborative.

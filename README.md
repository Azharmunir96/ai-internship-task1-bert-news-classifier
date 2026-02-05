# 📰 News Classifier: BERT Fine-Tuning & Local Deployment

End-to-end implementation of **Task 1** for my AI Engineering Internship. Fine-tuned **BERT-base-uncased** on AG News via **GCP Vertex AI** and deployed locally using **Gradio**.

---

## 🚀 Pipeline (Cloud → Local)

1. **Cloud Training:** Fine-tune BERT on GCP with PyTorch.  
2. **Serialization:** Export weights with `safetensors` for efficient local loading.  
3. **Local Inference:** Custom Python wrapper for tokenizer + model execution on CPU.  
4. **Interface:** Gradio web UI for real-time predictions.

---

## 🏗️ Architecture

User Input → Gradio UI → Tokenizer → BERT → Softmax → Prediction + Confidence

* **Model:** BERT-base-uncased (~110M params, FP32)  
* **Framework:** PyTorch, `torch.inference_mode()`  
* **Web Stack:** Gradio 6.x + FastAPI  

### Supported News Categories

| Index | Category     | Description                   |
|------:|-------------|-------------------------------|
| 0     | World       | Global politics & events       |
| 1     | Sports      | Matches, players, tournaments |
| 2     | Business    | Markets, finance, stocks      |
| 3     | Sci/Tech    | AI, gadgets, research         |

---

## 📊 Benchmark Example

**Input:** "The championship game went into double overtime last night."  
**Output:** Sports (97.43% confidence)  
**Test Accuracy:** ~94.8% on AG News (4-class)


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

## Project Access

Due to the substantial size of this project, it is not feasible to upload it to GitHub. To ensure accessibility and ease of use, the complete project folder has been hosted on Google Drive. This allows reviewers, collaborators, and stakeholders to download the entire project without encountering file size limitations or incomplete uploads.

The project folder contains all relevant materials, including:  
- Source code  
- Datasets  
- Configuration files  
- Documentation  

By providing the folder in a centralized location, all components are preserved in their original structure and format, preventing potential issues from missing or corrupted files. Users can access the shared link below to download the full project and start working immediately. This method also facilitates version control and collaboration by allowing updates or additional resources to be shared efficiently.

It is recommended to download the project in its entirety to ensure all dependencies and resources are available. For any questions or assistance regarding accessing the project folder, please do not hesitate to contact us.

**Project Link:** [Google Drive Project Folder](https://drive.google.com/file/d/170woZo3Z6eb1_-b4hptibFk2adBkKiJh/view?usp=drive_link)


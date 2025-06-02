# 📖 Conversational Image Recognition Chatbot

### Project Title: Conversational Image Recognition Chatbot  
### Semester: VI (2024-25)


---

## 1. Introduction
**Dates:** 24/02/2025 to 08/03/2025

- **Problem Statement:**  
  Traditional conversational AI assistants like Siri, Google Assistant, and Cortana handle text and voice well but lack strong image recognition capabilities. Merging visual understanding with dialogue systems remains a significant challenge.

- **Objectives:**  
  - Develop a chatbot that can recognize and understand images uploaded by users.
  - Enable conversational querying and responses based on image content.
  - Seamlessly integrate deep learning-based image recognition with natural language processing (NLP).

- **Applications:**  
  - Customer support (analyzing product images).    


---

## 2. Literature Survey
**Dates:** 10/03/2025 to 22/03/2025

- **Background:**  
  A growing need exists for systems capable of both visual understanding and conversational interaction.

- **Existing Systems:**  
  - Siri, Google Assistant, Cortana (text/voice-based, limited visual input).
  - Visual Question Answering (VQA) models.
  - OpenAI CLIP model (Connecting images and text).

- **Research Papers Studied:**  
  - Anderson et al., "Bottom-Up and Top-Down Attention for Image Captioning and Visual Question Answering" (CVPR 2018).
  - Radford et al., "Learning Transferable Visual Models From Natural Language Supervision" (CLIP - OpenAI 2021).
  - Das et al., "Visual Dialog" (CVPR 2017).

*(Citations will be detailed in the final document.)*


---

## 3. Methodology
**Dates:** 24/03/2025 to 05/04/2025

- **Hardware and Software Requirements:**  
  - GPU-enabled system (for deep learning model training).  
  - Python, TensorFlow/PyTorch, OpenCV, PowerBI/Tableau for visualization.  
  - NLP toolkit: HuggingFace Transformers.

- **System Design:**  
  **Block Diagram:**  
  User Input → Image Upload → Image Processing (CNN/CLIP model) → Feature Extraction → Question Processing (NLP Model) → Response Generation

- **Algorithm:**
  1. Image Feature Extraction using a pretrained CNN/CLIP.
  2. Question understanding via a Transformer-based NLP model.
  3. Multimodal fusion for generating accurate responses.
  4. Output response to user.

- **Exploratory Data Analysis and Dataset Visualization:**
  - Dataset: VQA v2.0 dataset.
  - Visualization done using PowerBI.


---

## 4. Implementation Details
**Dates:** 07/04/2025 to 26/04/2025

- **Module 1: Image Recognition Module**
  - Built using a pretrained CLIP model.
  - Snapshots: Model architecture, image embeddings generation.

- **Module 2: Conversational NLP Module**
  - Implemented using HuggingFace's BERT or T5 model.
  - Snapshots: Question parsing, intent detection.

- **Module 3: Response Generation and Interface**
  - Developed Flask-based simple front-end.
  - Snapshots: Chatbot UI, API integration, real-time conversations.

- **Testing:**
  - Unit tests for image understanding.
  - Integration tests for conversation flows.


---

## 5. Results
**Dates:** 28/04/2025 to 03/05/2025

- **Dataset Used:**  
  - VQA v2.0 (Visual Question Answering) dataset.  
*(Citation to be provided.)*

- **Performance Metrics:**
  - Accuracy for visual question answering.
  - Response relevance score.
  - User satisfaction evaluation.

- **Model Evaluation:**
  - Comparison against baseline VQA and chatbot models.
  - Initial results promising; further optimization to continue into Semester VII.

- **Report Writing:**
  - In progress.


---

## 6. Conclusion

- Successful integration of image recognition with conversational AI.
- Achieved basic conversational understanding of visual data.
- Future work: Model fine-tuning, real-world testing, and deployment.

---

## 7. References

- Anderson et al., CVPR 2018.  
- Radford et al., OpenAI 2021.  
- Das et al., CVPR 2017.  



# Conversational Image Recognition Chatbot - Weekly Log Book

---

## Week 1: Problem Understanding & Objective Definition

We thoroughly studied the Smart India Hackathon problem statement, focusing on understanding the core issue: the absence of an AI chatbot that can both recognize images and respond to questions related to the image.

Conducted discussions on the limitations of existing chatbots like Siri, Alexa, and Google Assistant, which are limited to text or voice and don't analyze image content.

Finalized the objective: To build a chatbot that combines Computer Vision (image recognition) and Natural Language Processing (NLP) to interpret images uploaded by users and answer related queries.

Outlined key features:

- Detect objects in uploaded images.
- Understand user queries in natural language.
- Generate accurate, relevant, and grammatically correct responses.

Also clarified that the chatbot should be scalable and applicable to real-world scenarios.

---

## Week 2: Research & Technology Exploration

Researched various deep learning techniques and tools suitable for image recognition and conversational AI.

For image recognition:

- Studied Convolutional Neural Networks (CNNs), YOLOv5, ResNet, and MobileNet for object detection.
- Analyzed datasets like ImageNet and COCO for training.

For NLP/chatbot part:

- Explored libraries like spaCy, NLTK, HuggingFace Transformers, and Langchain.
- Decided on using pre-trained models like BERT or GPT-based models for natural responses.

Finalized tech stack:

- Frontend: HTML, CSS (for chatbot UI).
- Backend: Python (Flask/FastAPI), TensorFlow/PyTorch.
- Integration tools: REST API, JSON for data exchange between image module and chatbot.

Reviewed research papers and case studies for better implementation ideas.

---

## Week 3: Project Planning & Task Division

Created a detailed roadmap with weekly goals and deadlines to track progress.

Used project management tools like Trello/Notion to assign tasks and monitor updates.

Team roles defined:

- Project lead: chatbot integration and documentation.
- Member 2: Model training for image recognition.
- Member 3: UI/UX design, frontend, and demo video editing.

Set up a GitHub repository for version control and collaboration.

Collected relevant image datasets, categorized them based on objects for training.

Defined metrics for success: image detection accuracy, chatbot response quality, and system response time.

---

## Week 4: Data Preparation & Initial Implementation

Started cleaning and labeling image datasets to ensure accurate training.

Preprocessed data using techniques like resizing, normalization, augmentation.

Built a basic CNN model to test object detection.

Used YOLOv5 for real-time object detection due to its balance between speed and accuracy.

Successfully tested sample images with multiple objects.

Began writing Python scripts for image upload and detection pipeline.

Discussed integration approach of detected image labels with chatbot backend.

---



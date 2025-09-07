# 🤖 Models

This directory contains all the machine learning models that power our intelligent requirements engineering platform. Each model is designed to handle a specific stage of the requirements analysis and management lifecycle.

---

## Core Analysis Pipeline

This pipeline forms the backbone of our system, processing raw text to deliver classified and scored requirements.

* **1. Requirement Extraction (NER)**: This model finds and extracts requirement statements from raw text in documents. It uses a pre-trained **BERT/mBERT** model that has been fine-tuned for requirement-specific Named Entity Recognition.
    * **Input**: Raw document.
    * **Output**: Entities corresponding to requirement statements.

* **2. Requirement Classification (FR/NFR)**: This model classifies the extracted requirements into **Functional (FR)** and **Non-Functional (NFR)** categories. It's a text classification model, preferably a fine-tuned **BERT**.
    * **Input**: Requirement text.
    * **Output**: FR/NFR classification.

* **3. Requirement Quality Scoring**: This model generates confidence scores that indicate if a requirement is "good" or "bad". It's built using **BERT** or a custom model.
    * **Input**: Requirement text.
    * **Output**: Quality scores.

---

## Advanced & Supporting Models

These models provide extended capabilities for prioritization, multilingual support, and test case generation.

* **4. Prioritization Model**: Predicts the priority of each requirement to aid in development planning.

* **5. Multilingual Model**: Supports requirement extraction and classification in multiple languages. This is achieved using a **multilingual transformer model** that combines translation and extraction techniques.

* **6. Test Case Generation Model**: Automatically generates test cases from the requirements. It uses a sequence-to-sequence pre-trained model like **T5** or **GPT-3/4**.

---

## Core Technologies Summary

A quick overview of the key technologies and frameworks used across our models:

* **NER & Classification**: Fine-tuned **BERT** and **mBERT** models are the primary tools for text extraction and classification tasks.
* **Object Detection**: **YOLO** is used for detecting visual elements.
* **Optical Character Recognition (OCR)**: **Tesseract** is employed for extracting text from images and scanned documents.
* **Generative Tasks**: Sequence-to-sequence models like **T5** and **GPT-3/4** are used for tasks like test case generation.

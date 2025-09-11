# AI-Powered Financial Document Redaction

Guardian is an intelligent, AI-driven solution designed to automatically detect and redact sensitive Personally Identifiable Information (PII) from financial documents, ensuring data privacy and regulatory compliance for the banking and fintech industries.

## Frontend Video Demo

Check out the frontend demo of the project in action(click on the Img):

[![Watch the demo](https://github.com/user-attachments/assets/2cb52f9a-d658-4ed7-a5d4-c903e57aa156)](https://www.loom.com/share/d51ae0567ac443008d8eba8c0dcb737a)

---

## Model Accuracy

Check out the **Model Accuracy** of the project in the below images and video:

### Accuracy Graphs
![Accuracy Graph 1](https://github.com/user-attachments/assets/cd263a35-1ad1-47a0-942b-c6c8c599f91f)
![Accuracy Graph 2](https://github.com/user-attachments/assets/0f5b7c24-4751-48d6-bc6e-143078494c84)

## Demo Models

### 1. **BERT NER Model**
This model is used for Named Entity Recognition (NER) based on BERT architecture. The model identifies and classifies named entities (such as persons, locations, organizations, etc.) from the text.

[BERT NER Model](https://github.com/user-attachments/assets/2c3db446-4ac0-4570-aea2-27f59a5c95af)

### 2. **BERT FR_NFR Model**
This model uses BERT to classify text into French (FR) and Non-French (NFR) categories. It can be used for language identification in text documents.

[BERT FR_NFR Model](https://github.com/user-attachments/assets/85960e26-1ef5-42f3-890a-ba5e41a2257b)

### 3. **Pytesseract OCR Extraction Model**
This model utilizes pytesseract to extract text from images (Optical Character Recognition). It is ideal for digitizing printed or handwritten content.

[Pytesseract OCR Extraction Model](https://github.com/user-attachments/assets/f2305bda-3845-484f-9d93-052f8dd9aa7f)


---

## The Problem

Financial documents like loan applications, KYC forms, and invoices are filled with sensitive PII (account numbers, SSNs, signatures). Sharing these documents across departments or with partners creates a significant risk of data leaks, while manual redaction is slow and prone to human error.

---

## Our Solution

Guardian provides a robust, automated pipeline to sanitize your documents securely. It intelligently identifies and scrubs sensitive information from a variety of formats, preserving the integrity of the original document structure.

### Key Features:

* **Comprehensive PII Detection**: Identifies a wide range of sensitive data including:
    * **Textual PII**: Account numbers, SSNs, client names, and SWIFT codes.
    * **Visual PII**: Signatures, handwritten notes, bank logos, stamps, and barcodes.
    * **Hidden Metadata**: Cleans sensitive information from document properties.
* **Multi-Format Support**: Processes a variety of document types with ease:
    * PDFs (including scanned documents).
    * Images (JPEG, PNG) like checks and invoices.
    * Tabular Data (Excel/CSV).
* **Innovative Hybrid Approach**: Our unique selling point is the combination of:
    * **Rule-Based Precision**: Uses Regex for well-defined patterns like SWIFT codes.
    * **AI-Powered Context**: Employs advanced NLP to understand context (e.g., distinguishing an "Account No" from a "Page No").
* **Table-Aware Redaction**: Preserves the structure and readability of tables while redacting sensitive cells, a crucial feature for financial statements.

---

## 🤖 Technology Stack

Our solution is powered by a sophisticated suite of AI/ML models:

* **OCR**: `Tesseract` for accurate text extraction from images and scanned PDFs.
* **PII Detection**: A combination of `spaCy (NER)` for named entity recognition and `LayoutLMv3` for understanding tabular context.
* **Visual Redaction**: `YOLOv8` to detect objects like signatures and logos, supplemented by `GANs` to generate synthetic training data.

---

## User Experience

Guardian is designed for everyone, from compliance officers to developers.

* **🖥Drag-and-Drop Web App**: An intuitive interface for non-technical users to upload files, preview redactions, and download the sanitized documents.
* **⚙️CLI Version**: A powerful command-line interface for developers to perform batch processing, perfect for integrating into bank backend systems.

### Input & Output:

* **Input**: `PDF`, `JPEG`, `PNG`, `CSV`.
* **Output**: A securely redacted PDF and a `JSON` audit log detailing the redacted fields and the confidence scores for each redaction.

---

## Compliance & Scalability

* **GDPR/CCPA Ready**: Generates detailed audit logs to prove PII removal, ensuring you meet regulatory requirements.
* **Accessibility**: Features multilingual support and a low-resource mode using CPU-efficient models like `DistilBERT`.
* **Seamless Integration**: Designed for easy integration with banking APIs like Plaid, acting as a pre-redaction hook.

---

## The Team: Devengineers

This project is brought to you by **Devengineers**:
* Aditya Kumar Singh (Leader)
* Ishant Singh
* Naveen Kumar Mohanarajan
* Sameer Yadav








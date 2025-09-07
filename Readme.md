# 🛡️ Guardian: AI-Powered Financial Document Redaction

Guardian is an intelligent, AI-driven solution designed to automatically detect and redact sensitive Personally Identifiable Information (PII) from financial documents, ensuring data privacy and regulatory compliance for the banking and fintech industries.

---

## 🎯 The Problem

Financial documents like loan applications, KYC forms, and invoices are filled with sensitive PII (account numbers, SSNs, signatures). Sharing these documents across departments or with partners creates a significant risk of data leaks, while manual redaction is slow and prone to human error.

---

## ✨ Our Solution

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

## 🧑‍💻 User Experience

Guardian is designed for everyone, from compliance officers to developers.

* **🖥️ Drag-and-Drop Web App**: An intuitive interface for non-technical users to upload files, preview redactions, and download the sanitized documents.
* **⚙️ CLI Version**: A powerful command-line interface for developers to perform batch processing, perfect for integrating into bank backend systems.

### Input & Output:

* **Input**: `PDF`, `JPEG`, `PNG`, `CSV`.
* **Output**: A securely redacted PDF and a `JSON` audit log detailing the redacted fields and the confidence scores for each redaction.

---

## 🌐 Compliance & Scalability

* **GDPR/CCPA Ready**: Generates detailed audit logs to prove PII removal, ensuring you meet regulatory requirements.
* **Accessibility**: Features multilingual support and a low-resource mode using CPU-efficient models like `DistilBERT`.
* **Seamless Integration**: Designed for easy integration with banking APIs like Plaid, acting as a pre-redaction hook.

---

## 👥 The Team: Devengineers

This project is brought to you by **Devengineers**:
* Aditya Kumar Singh (Leader)
* Ishant Singh
* Naveen Kumar Mohanarajan
* Sameer Yadav


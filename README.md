# AWS Document Processing Pipeline

This project demonstrates how to build an automated **document processing pipeline** using Amazon Web Services (AWS). It integrates multiple AI services including **Amazon Textract**, **Amazon Comprehend**, **Amazon Polly**, and **Amazon Translate**, all orchestrated through a Jupyter Notebook running in **Amazon SageMaker**.

---

## 🚀 Overview

The pipeline extracts text from documents, analyzes the content, performs sentiment and entity recognition, generates speech from text, and optionally translates the content into multiple languages. It is designed to be modular, extensible, and suitable for real-world document processing workflows.

---

## 📦 Features

* **Text Extraction (OCR)** using Amazon Textract
* **Sentiment Analysis** using Amazon Comprehend
* **Entity Extraction** (names, dates, locations, etc.)
* **Text Summarization** with AWS AI services
* **Speech Generation** using Amazon Polly
* **Optional Translation** using Amazon Translate
* **S3 Integration** for input/output file storage
* **Structured JSON Output** for downstream applications

---

## 🛠 Technologies Used

* **Python 3**
* **Amazon SageMaker Notebook**
* **AWS SDK for Python (boto3)**
* **Amazon Textract**
* **Amazon Comprehend**
* **Amazon Polly**
* **Amazon S3**
* **Amazon Translate** (optional)

---

## 📁 Project Structure

```
|-- notebook.ipynb
|-- input/
|   |-- sample-document.jpg
|-- output/
|   |-- extracted_text.json
|   |-- comprehend_analysis.json
|   |-- speech_output.mp3
|-- README.md
```

---

## ⚙️ How It Works

### 1. **Upload document to S3**

The notebook uploads a file (image or PDF) to your S3 bucket.

### 2. **Run Textract**

Textract extracts raw text, key-value pairs, and structural blocks.

### 3. **Analyze with Comprehend**

The extracted text is analyzed for:

* Sentiment (positive/negative/neutral/mixed)
* Key phrases
* Named entities

### 4. **Generate Speech with Polly**

The text is converted into natural speech using Amazon Polly.

### 5. **Store Outputs**

All results are saved back into your S3 bucket in JSON or MP3 format.

---

## ▶️ Getting Started

### Prerequisites

* AWS account
* IAM role with Textract, Comprehend, S3, and Polly permissions
* SageMaker Notebook instance
* boto3 installed

### Installation

```bash
pip install boto3
```

### Run the Notebook

Open the notebook in SageMaker and execute each cell step-by-step.

---

## 🔐 IAM Permissions Required

The execution role must allow:

* `textract:*`
* `comprehend:*`
* `polly:SynthesizeSpeech`
* `s3:GetObject`, `s3:PutObject`

---

## 📌 Example Output

### ✓ Text extracted from document

### ✓ Sentiment: *Positive*

### ✓ Key Entities: *Names, Dates, Locations*

### ✓ Speech File: *speech_output.mp3*

---

## 🧩 Future Improvements

* Integration with Amazon Lambda for full automation
* Multi-language OCR support
* Database storage (DynamoDB or RDS)
* API endpoint using AWS API Gateway & Lambda

---

## 👨‍💻 Author

Developed as part of an AWS AI/ML pipeline demonstration.

---


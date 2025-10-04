# 🩺 Medical Report Summariser

A lightweight **AI-powered application** for extracting and summarising medical reports.  
It combines **OCR** for text extraction with **NLP-based summarisation**, making it easier to quickly understand lengthy healthcare documents.

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![Author](https://img.shields.io/badge/author-cosmoLegend-green)
![License](https://img.shields.io/badge/license-Pending-orange)
![Stars](https://img.shields.io/github/stars/cosmoLegend/Medical-Report-Summariser?style=social)

---

## ✨ Features

- 📄 **OCR-based Text Extraction**  
  Extracts text from PDFs, scanned reports, or images using **Tesseract OCR**.

- 🧠 **AI-driven Summarisation**  
  Generates concise, human-readable summaries highlighting the essential clinical information.

- ⚡ **Fast & Efficient**  
  Handles large reports with an optimised processing pipeline.

- 🔎 **Relevance-Focused Output**  
  Uses text-similarity checks to ensure summaries focus on key findings.

- 🔗 **REST API Ready**  
  Provides a simple API layer for integration with other apps or dashboards.

---

## 🚀 Getting Started

### Prerequisites
- [Node.js](https://nodejs.org/) (LTS version recommended)
- npm or yarn
- [Tesseract OCR](https://tesseract-ocr.github.io/) installed on your system

---

## 🔧 Installation

1. **Clone the Repository**

   ~~~bash
   git clone https://github.com/cosmoLegend/Medical-Report-Summariser.git
   cd Medical-Report-Summariser
   ~~~

2. **Install Dependencies**

   ~~~bash
   npm install
   # or
   yarn install
   ~~~

3. **Configure Environment Variables**  
   Create a `.env` file in the project root:

   ~~~env
   PORT=3000
   TESSDATA_PREFIX=./tessdata
   ~~~

   - `PORT` → Server port (default: 3000)  
   - `TESSDATA_PREFIX` → Path to your Tesseract language data

4. **Tesseract Data**  
   Place `eng.traineddata` (and other needed language files) in the directory specified by `TESSDATA_PREFIX`.  
   You can download them from the [Tesseract tessdata repository](https://github.com/tesseract-ocr/tessdata).

---

## 💡 Usage

1. **Start the Server**

   ~~~bash
   npm start
   # or
   node server.js
   ~~~

   The server will start on `http://localhost:3000` (or the port defined in your `.env`).

2. **Send a Document for Summarisation** (example with `curl`)

   ~~~bash
   curl -X POST \
        -F "file=@/path/to/medical_report.pdf" \
        http://localhost:3000/api/summarise \
        -H "Content-Type: multipart/form-data"
   ~~~

   The API returns a JSON object containing:
   - Extracted text  
   - Generated summary  

---

## 🛣️ Roadmap

- 🌍 Multi-language OCR & summarisation support  
- 📂 Broader file-format support (DOCX, DICOM, etc.)  
- 🔑 Authentication and secure data handling for sensitive medical data  
- 💻 Simple web UI for uploading reports and viewing summaries  
- 🧬 Domain-specific summarisation tuned for medical terminology  
- ✅ Expanded automated test coverage

---

## 🤝 Contributing

Contributions are welcome!

1. **Fork** this repository  
2. **Create a new branch**:
   - `feature/add-new-functionality`
   - `bugfix/fix-ocr-issue`
3. **Make your changes** and add tests as needed  
4. **Commit** with a descriptive message  
5. **Open a Pull Request** to `main`

**Code Style Tips**
- Use ESLint or Prettier for consistent formatting  
- Comment key logic for readability  
- Ensure all tests pass before submitting a PR

---

## ⚖️ License

Currently **unlicensed** – all rights reserved by the author **@cosmoLegend**.  
For usage or distribution permissions, please contact the repository owner.

---

## 📌 Disclaimer

This project is intended for **educational and development purposes only**.  
It is **not a certified medical tool** and should not be used for clinical decision-making.

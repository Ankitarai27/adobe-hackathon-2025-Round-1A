# Adobe-Hackathon-2025-Round-1A

📄 PDF Outline Extractor (Adobe Hackathon Round 1A)

✅ Overview

This project extracts headings (H1, H2, H3) and the document title from PDF files and outputs them in JSON format. It uses font size analysis and text pattern rules to detect document structure.

✅ How It Works

1. Input
Place your PDF files inside the input/ folder.

2. Processing
Script parses PDFs using pdfminer.six.

Extracts font size & text blocks.

Determines title and headings using:

Font-size thresholds.

Regex for numbering patterns.

Filtering negative keywords & noise.

3. Output
For each PDF in input/, a corresponding JSON file is created in output/.

Example:
Input: input/file01.pdf
Output: output/file01.json

✅ Folder Structure

graphql
Copy
Edit
```
.
├── input/         # PDF files to process
├── output/        # JSON outputs
├── main.py        # Main script
├── requirements.txt
└── Dockerfile
```

✅ Libraries Used

pdfminer.six → PDF parsing and text extraction.

re (regex) → Cleaning and pattern matching.

json → Output formatting.

Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
requirements.txt

ini
Copy
Edit
pdfminer.six==20221105

✅ How to Run Locally

Step 1: Add PDFs
Put all your PDFs inside the input/ folder.

Step 2: Run the Script
bash
Copy
Edit
python main.py

Step 3: Get Output
Check the output/ folder for the JSON results.

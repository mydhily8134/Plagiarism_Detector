# 📄 Plagiarism Detection System

This project is a web-based tool designed to detect textual plagiarism across multiple PDF documents (not limited to resumes). It uses machine learning and NLP techniques to analyze text similarity and flag pairs of files that are significantly similar.

## 🔍 Features

- Upload a ZIP file containing multiple PDF documents
- Extracts text from each PDF using `PyPDF2`
- Computes pairwise similarity using **TF-IDF** and **cosine similarity**
- Identifies and displays potentially plagiarized pairs
- Highlights common words shared between flagged documents
- Simple web interface built using Flask

## 🛠️ Technologies Used

- **Python**
- **Flask** – Web framework
- **PyPDF2** – PDF text extraction
- **scikit-learn** – TF-IDF vectorization & cosine similarity
- **HTML / Jinja2** – Frontend templates

## 📂 Folder Structure
project-root/
│
├── flask1.py # Flask-based web app
├── plagarismdetector.py # Command-line utility for batch checking
├── templates/
│ ├── page1.html # Homepage
│ ├── upload.html # Upload form
│ └── results.html # Result display page
└── static/ # (Optional) Static CSS/JS files


## 🚀 How It Works

1. User uploads a `.zip` file containing multiple **PDFs**.
2. The app extracts and reads all PDF files using `PyPDF2`.
3. Each document is converted into a **TF-IDF vector**.
4. Cosine similarity is calculated between every document pair.
5. Pairs with similarity above a threshold (default: **0.3**) are flagged.
6. Common words between similar documents are extracted and displayed.

---

## ⚙️ Running the Web App Locally

### 1. Install Dependencies
pip install flask PyPDF2 scikit-learn
## Run the app
python flask1.py

## Example output
Similarity score between fileA.pdf and fileB.pdf: 0.76
Common words: ['algorithm', 'system', 'performance', 'data']



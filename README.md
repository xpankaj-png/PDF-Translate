# PDF Translation Application

This web application translates text from Hindi and Sanskrit PDF files into English. It handles both text-based and scanned (image-based) PDFs and generates a `.docx` file with the original text followed by its English translation, paragraph by paragraph.

## Features

-   Upload PDF files (Hindi/Sanskrit).
-   Extracts text from both text-based and scanned PDFs using OCR.
-   Translates text to English paragraph by paragraph.
-   Generates a `.docx` file with the original and translated text.
-   Simple web interface.

## Prerequisites

Before you begin, you need to have [Tesseract OCR](https://github.com/tesseract-ocr/tesseract) installed on your system, along with the language packs for Hindi and Sanskrit.

### On Debian/Ubuntu:
```bash
sudo apt-get update
sudo apt-get install -y tesseract-ocr tesseract-ocr-hin tesseract-ocr-san
```

### On macOS (using Homebrew):
```bash
brew install tesseract
brew install tesseract-lang
```
(Ensure Hindi and Sanskrit models are available in your Tesseract installation).

### On Windows:
Download and install Tesseract from the [official UB Mannheim repository](https://github.com/UB-Mannheim/tesseract/wiki). Make sure to select the Hindi and Sanskrit language packs during installation.

## Setup and Installation

1.  **Clone the repository (or download the source code):**
    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```

2.  **Create and activate a virtual environment:**
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```
    On Windows, use `venv\Scripts\activate`.

3.  **Install the required Python packages:**
    ```bash
    pip install -r requirements.txt
    ```

## How to Run the Application

Once the setup is complete, you can start the Flask web server:

```bash
python app.py
```

The application will be running at `http://127.0.0.1:5000`. Open this URL in your web browser.

## How to Use

1.  Open the application in your browser.
2.  Click the "Choose File" button to select a Hindi or Sanskrit PDF from your computer.
3.  Click "Upload".
4.  The application will process the PDF and display the translation on the screen.
5.  Click the "Download .docx" button to save the translated document.
6.  To translate another file, click the "Translate another file" link.
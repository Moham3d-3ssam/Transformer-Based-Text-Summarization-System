# Transformer-Based Text Summarization System

An AI-powered dialogue summarization project built with a Transformer model (T5) and deployed with Gradio.

## Live Demo

Try it here: **https://huggingface.co/spaces/Moham3d-3saam/Text_Summarization_System**

## Project Overview

This project fine-tunes a T5-based model for text summarization (SAMSum dialogue dataset) and serves it through an interactive Gradio chat interface.

### Highlights
- Transformer-based summarization using **T5**
- Input cleaning and preprocessing pipeline
- Fast inference with GPU/CPU auto-detection
- Streaming response UX in Gradio
- Ready-to-use saved model and tokenizer

## Repository Structure

```text
Transformer-Based-Text-Summarization-System/
├── app/
│   └── app.py                                 # Gradio application
├── data/
│   ├── samsum-train.csv
│   ├── samsum-validation.csv
│   ├── samsum-test.csv
│   └── samsum_dataset/                        # Processed dataset artifacts
├── notebook/
│   └── Transformer_Based_Text_Summarization.ipynb
├── saved_files/
│   ├── tokenizer/                             # Trained tokenizer files
│   └── summarization_model/                   # Trained T5 model files
└── requirements.txt
```

## Tech Stack

- Python
- PyTorch
- Hugging Face Transformers
- Gradio

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Moham3d-3ssam/Transformer-Based-Text-Summarization-System.git
   cd Transformer-Based-Text-Summarization-System
   ```

2. (Optional) Create a virtual environment:
   ```bash
   python -m venv .venv
   source .venv/bin/activate      # Linux/macOS
   # .venv\Scripts\activate       # Windows
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Run Locally

Start the Gradio app:

```bash
python app/app.py
```

Then open the local URL shown in your terminal (usually `http://127.0.0.1:7860`).

## Model & Inference Notes

- Tokenizer and model are loaded from:
  - `saved_files/tokenizer`
  - `saved_files/summarization_model`
- Inference generation setup in `app/app.py`:
  - `max_length=175`
  - `num_beams=4`
  - `do_sample=True`
  - `temperature=0.7`

## Dataset

The project uses the **SAMSum** dataset (dialogue-to-summary task), with train/validation/test splits included in the `data/` directory.

## How to Use

1. Open the app (local or Hugging Face Space).
2. Paste a dialogue or text conversation.
3. Submit and get a concise generated summary.

## Future Improvements

- Add ROUGE/BLEU evaluation reporting section
- Add Docker support
- Add unit tests for preprocessing and inference pipeline
- Add API endpoint (FastAPI) for production integration

## Author

- GitHub: **Moham3d-3ssam**
- Hugging Face Space owner: **Moham3d-3saam**

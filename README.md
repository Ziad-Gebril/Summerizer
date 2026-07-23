# 🎥 YouTube Video Summarizer & Translator

An automated pipeline that fetches transcripts from YouTube videos, chunks and summarizes the content using **Facebook's BART Large CNN**, and translates the summary into Arabic using **Meta's NLLB-200 (No Language Left Behind)** model.

---

## 📌 Features

* **Transcript Retrieval**: Automatically extracts English transcripts using `youtube-transcript-api`.
* **Smart Text Chunking**: Splits lengthy video transcripts into manageable blocks to prevent sequence length truncation errors.
* **Abstractive Summarization**: Utilizes `facebook/bart-large-cnn` to distill long transcripts into concise bullet points and overviews.
* **Multilingual Translation**: Translates the generated summary into Arabic (`arb_Arab`) using `facebook/nllb-200-distilled-600M`.

---

## 🛠️ Tech Stack & Dependencies

* **Python**: 3.10+
* **Frameworks**: `transformers`, `torch`
* **Video API**: `youtube-transcript-api`
* **Models Used**:
  * Summarization: `facebook/bart-large-cnn`
  * Translation: `facebook/nllb-200-distilled-600M`

---

## 🔄 Pipeline Workflow

[ YouTube Video URL ] ──► [ youtube-transcript-api ] ──► [ Full English Transcript ] ──► [ BART-Large CNN Summarizer ] ──► [ NLLB-200 Translation ] ──► [ Arabic Summary ]


🪔 A Byte-Level Seq2Seq Language Model for Indian Mythology
LoRA Fine-Tuning with Knowledge Graph–Enhanced Training

This repository contains the code, dataset samples, and report for the project:

“A Byte-Level Seq2Seq Language Model for Indian Mythology: LoRA Fine-Tuning with Knowledge Graph–Enhanced Training”
Developed as part of MAT499: Project Phase I at SASTRA Deemed to be University (2025)
by Chakravadhanula Naga Pranav

🧠 Project Overview

This research explores how Low-Rank Adaptation (LoRA) and Knowledge Graph (KG) integration can enhance the factual reasoning and contextual understanding of Byte-level Transformer models in culturally rich domains.

Using the ByT5-small model (a multilingual byte-level Seq2Seq transformer), we fine-tuned it on mythological question–answer data derived from the Ramayana.
The model was trained both:

🧩 Baseline LoRA Model: Fine-tuned on QA pairs.

🔗 KG-Enhanced Model: Fine-tuned with additional Knowledge Graph facts converted to natural language.

This experiment investigates whether symbolic knowledge (KGs) improves factual precision in generative models.

⚙️ Methodology
Component	Description
Base Model	google/byt5-small
Fine-Tuning	Parameter-Efficient Fine-Tuning (LoRA via PEFT library)
Dataset	1,696 QA pairs + 1,098 KG triples (custom curated from Ramayana)
Evaluation Metrics	ROUGE-1, ROUGE-L, BLEU
Environment	Python 3.10, PyTorch, Hugging Face Transformers, Colab GPU
📊 Results
Model	ROUGE-1	ROUGE-L	BLEU
ByT5 + LoRA (Baseline)	0.712	0.709	0.447
ByT5 + LoRA + KG	0.662	0.660	0.407

Insights:

LoRA achieved strong, stable performance with <1% of parameters fine-tuned.

Byte-level tokenization worked well for transliterated Sanskrit and multilingual data.

KG integration in text form added redundancy — suggesting future use of graph embeddings or RAG architectures.

📘 Dataset

Two datasets are provided as samples under /data/:

sample_training_data.csv → Question–Answer pairs from Ramayana

sample_dataset_with_kg.csv → QA + Knowledge Graph facts

Full dataset available upon request for academic use.

🧩 Key Takeaways

LoRA drastically reduces fine-tuning cost without sacrificing accuracy.

Byte-level models offer flexibility for multilingual, script-independent text.

Direct textual injection of KG facts introduces contextual noise —
future approaches should explore graph embeddings or retrieval-based augmentation.

👨‍💻 Author

Chakravadhanula Naga Pranav
M.Sc. Data Science, SASTRA Deemed to be University
📅 November 2025
📧 Chakravadhanula.pranav@gmail.com , www.linkedin.com/in/naga-pranav-chakravadhanula-714a01301

🪶 License

This project is released under the MIT License.
Feel free to use, modify, and cite this work with attribution.

💡 Made With

🧠 Python • 🤗 Transformers • ⚙️ PEFT (LoRA) • 📊 PyTorch • 🪔 Cultural NLP Research

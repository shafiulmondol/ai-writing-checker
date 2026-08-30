🤖 AI Writing Checker

A free, research-oriented AI Writing Detection platform for checking whether English text appears AI-generated or human-written.

This project provides two AI detector interfaces in one workflow:

🌐 AI Writing Analyzer — browser-based TMR / RoBERTa detector

🤗 AI Writing Detector — Hugging Face detector interface

The system is designed for long documents and unlimited-word workflows by processing text in manageable segments rather than forcing a small fixed input box.

🚀 Live AI Detectors

1. AI Writing Analyzer — TMR Research Mode

🔗 Website:
https://shafiulmondol.github.io/ai-writing-checker/

This detector uses a TMR (Target Mining RoBERTa) based approach. The web version processes a document using overlapping text segments and combines the segment-level predictions into document-level evidence.

Features:

✅ AI-generated text detection

✅ Human-like text estimation

✅ Long-document analysis

✅ Sentence/segment-level evidence

✅ AI probability scoring

✅ Highlighted AI signals

✅ PDF / DOCX / TXT upload support

✅ Browser-based processing

✅ No fixed short-text input requirement

✅ Suitable for assignments, papers and research documents

The current analyzer describes its method as TMR with segment aggregation and an ONNX browser implementation. citeturn0view0

2. AI Writing Detector — Hugging Face

🔗 Hugging Face Space:
https://huggingface.co/spaces/ShafiulM7/ai-writing-detector

This provides a second AI-detection interface so results can be compared across two detector implementations.

Features:

🤖 AI text detection

👤 Human-written text estimation

📊 Detection score

📝 Long-text workflow

🔎 Useful for cross-checking results

☁️ Hosted through Hugging Face Spaces

Note: The two detectors may produce different scores because they use different implementations/models. A detector score should be treated as probabilistic evidence, not absolute proof of authorship.

♾️ Unlimited-Word Workflow

The goal of this project is to support unlimited-word document checking rather than restricting users to a small number of words.

For very large documents, the text can be processed in chunks/segments and the individual predictions can then be aggregated.

Example

A document containing:

500 words

2,000 words

5,000 words

10,000 words

50,000+ words

can be handled through a chunked analysis workflow, subject to the browser, hosting, memory and model-inference resources available at runtime.

This means "unlimited words" refers to the application's intended workflow, not a guarantee that a single browser session or hosting service has infinite memory/compute.

🧠 How the Detector Works

The overall workflow is:

                ┌─────────────────────┐
                │   User Document     │
                │ PDF / DOCX / TXT    │
                │ or pasted text      │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │   Text Extraction   │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │ Long Text Chunking  │
                │ / Overlapping       │
                │ Segments            │
                └──────────┬──────────┘
                           │
                 ┌─────────┴─────────┐
                 ▼                   ▼
        ┌─────────────────┐  ┌─────────────────┐
        │ Detector 1      │  │ Detector 2      │
        │ TMR / RoBERTa   │  │ Hugging Face    │
        └────────┬────────┘  └────────┬────────┘
                 │                    │
                 └─────────┬──────────┘
                           ▼
                ┌─────────────────────┐
                │ Compare Predictions │
                │ & Review Evidence    │
                └─────────────────────┘

📊 Detector 1: TMR Research Mode

The web analyzer uses a TMR (Target Mining RoBERTa) detector.

According to the live analyzer, the model is described as an English AI-text detector trained on the RAID benchmark, using Focal Loss and Self-Hard-Negative mining. The browser implementation uses an ONNX conversion. citeturn0view0

The analyzer also uses overlapping prose segments and combines their predictions to produce sentence/document-level evidence. citeturn0view0

Simplified pipeline

Document
   ↓
Split into overlapping segments
   ↓
TMR / RoBERTa inference
   ↓
AI probability for each segment
   ↓
Map evidence back to sentences
   ↓
Aggregate predictions
   ↓
Final document-level result

🔍 Why Use Two Detectors?

AI detectors are probabilistic models. Different models can interpret the same text differently.

Using two detector interfaces provides a useful cross-checking workflow:

Detector

Purpose

🌐 TMR Analyzer

Primary research-style analysis

🤗 Hugging Face Detector

Independent second detector

🔎 Comparison

Identify agreement/disagreement

If both detectors identify similar portions as AI-like, that can be stronger evidence for further review.

If they disagree, the result should be treated cautiously.

⚠️ Important Limitation

AI detection cannot prove who wrote a piece of text.

Human writing can sometimes be classified as AI-generated, and AI-generated text can sometimes be classified as human-written.

The live TMR analyzer specifically warns that AI detection is probabilistic and can misclassify human writing, especially short, edited, non-native, or out-of-domain English. It recommends using at least around 300 words of continuous prose for more reliable evaluation. citeturn0view0

Therefore:

AI detection scores should be used as research/assessment signals, not as definitive proof of authorship.

🎓 Recommended Use Cases

This project can be useful for:

📚 Academic assignments

📝 Research papers

🎓 Thesis drafts

📄 Essays

🔬 Research experiments

👨‍🏫 Educational assessment

✍️ Writing analysis

🤖 AI-generated text research

📊 Comparing detector outputs

🛠️ Technology

Detector 1

TMR / Target Mining RoBERTa

ONNX browser inference

Segment-based aggregation

Sentence-level evidence mapping

RAID benchmark training reference

Detector 2

Hugging Face Spaces

AI-writing detection model/interface

Frontend

HTML

CSS

JavaScript

📂 Repository

🔗 GitHub Repository:
https://github.com/shafiulmondol/ai-writing-checker

The repository contains the source for the AI Writing Checker project.

🌐 Quick Access

Service

Link

🌐 AI Writing Analyzer

https://shafiulmondol.github.io/ai-writing-checker/

🤗 Hugging Face Detector

https://huggingface.co/spaces/ShafiulM7/ai-writing-detector

💻 GitHub Repository

https://github.com/shafiulmondol/ai-writing-checker

👨‍💻 Author

Shafiul Mondol

AI Writing Checker — Research & Educational Project

⭐ Project Goal

The goal of this project is to provide an accessible AI-writing detection workflow that can analyze long-form English documents, provide useful AI/human writing signals, and allow users to cross-check results using two detector implementations.

Use responsibly. AI detection is probabilistic and should not be treated as definitive authorship verification.

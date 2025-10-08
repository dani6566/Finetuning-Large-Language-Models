# 📦 Fine-tuning Amharic Named Entity Recognition (NER)

## 🧭 Business Objective

EthioMart aims to become Ethiopia’s central hub for Telegram-based e-commerce. With many independent vendors operating fragmented channels, customers face challenges in product discovery and communication. EthioMart solves this by aggregating real-time data from multiple Telegram channels into one platform.

A key component is an Amharic NER system that extracts entities like **product names**, **prices**, and **locations** from text, images, and documents.

---

## 🔄 Data Ingestion & Preprocessing

1. **Telegram Scraper**: Collects messages (text, images, documents) from e-commerce channels.
2. **Preprocessing**:
   - Tokenization & normalization for Amharic.
   - Metadata separation (sender, timestamp).
   - Structured storage for training.

---

## 🏷️ Dataset Labeling (CoNLL Format)

Entities tagged:
- `B-Product`, `I-Product`
- `B-PRICE`, `I-PRICE`
- `B-LOC`, `I-LOC`
- `O` for other tokens

Example:
ቦሌ B-LOC 
ሱቅ O 
አዲስ B-LOC 
አበባ I-LOC 
ብራንድ B-Product 
ሻምፑ I-Product 
120 B-PRICE 
ብር I-PRICE


---

## 🤖 Model Fine-Tuning

### Models Used:
- **XLM-Roberta** – High accuracy
- **DistilBERT** – Fast & efficient
- **mBERT** – Balanced multilingual
- **afroXLMR** – Optimized for African languages

### Training Setup:
- Learning rate: `5e-5`
- Epochs: `3–5`
- Batch size: `16`
- Evaluation: Validation set monitoring

---

## 📊 Model Comparison

| Model        | Accuracy | Speed | Best Use Case         |
|--------------|----------|-------|------------------------|
| XLM-Roberta  | ⭐⭐⭐⭐     | ⏳     | Deep analysis          |
| DistilBERT   | ⭐⭐⭐      | ⚡     | Real-time extraction   |
| mBERT        | ⭐⭐⭐      | ⚡     | General multilingual   |
| afroXLMR     | ⭐⭐⭐⭐     | ⚡     | Amharic-specific tasks |

---

## 🔍 Interpretability (SHAP & LIME)

- **SHAP**: Highlights influential tokens (e.g., prices, locations).
- **LIME**: Reveals confusion in ambiguous cases (e.g., product vs. location).

Challenges:
- Ambiguity in overlapping entities
- Misclassification of similar-sounding tokens

---

## ✅ Recommendations

1. Use **DistilBERT** for real-time tasks.
2. Use **XLM-Roberta** for high-accuracy analysis.
3. Expand dataset to improve ambiguity handling.
4. Monitor performance with SHAP & LIME.

---

## 📌 Conclusion

The fine-tuned Amharic NER system enables EthioMart to extract key business entities from Telegram messages, helping unify Ethiopia’s e-commerce landscape.


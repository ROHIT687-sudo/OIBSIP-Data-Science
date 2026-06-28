# Natural Language Processing (NLP) Risk Assessment Filter — Task 4

## 📌 Architectural Overview
This module houses a binary **Natural Language Processing (NLP) Text Classification** system designed to scan text streams and flag high-risk vectors (`spam`) while passing legitimate user communication (`ham`).

## 🛠️ Production Engineering Workflow
1. **Encoding Optimization**: Handled non-standard character payloads and currency symbols safely by ingesting raw arrays under specialized `latin-1` parameter boundaries.
2. **TF-IDF Semantic Vectorization**: Implemented a `TfidfVectorizer` pipeline to translate unstructured text into weighted numerical token frequencies. The framework strips common English stop-words, extracting highly weighted predictive tokens ("URGENT", "FREE", "CLAIM") based on spatial document density.
3. **Classification Boundary Calculation**: Deployed a **Logistic Regression** model optimized for high-dimensional, sparse text matrices, drawing clear linear probability thresholds between secure and malicious messages.
4. **Ad-Hoc Risk Verification**: Evaluated model generalization limits using custom text strings to verify real-time filtering performance against modern phishing vocabulary variations.

## 🛡️ Operational Performance Indicators
* **Target Objective**: Maximum Precision optimization for the *Spam* class to prevent false positives from mistakenly trapping legitimate corporate communication in the junk directory.


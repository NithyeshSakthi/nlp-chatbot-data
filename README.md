							Multilingual Banking Chatbot (NLP Project)
https://colab.research.google.com/drive/1rAa83kmuyXP7cDmA0tXOwy2vPTa6Yp-K#scrollTo=1r2HV0hAoZYU

A smart and responsive chatbot that understands banking-related queries across **English**, **German**, and **Tamil**, designed using text classification and natural language processing techniques.

---

1. Datasets Used

This project uses three curated and translated datasets:
- `greeting_dataset.csv` — common greetings and welcome phrases
- `banking_response_dataset.csv` — general banking queries and answers
- `bank_loan_dataset.csv` — loan-related customer inquiries

All datasets were cleaned, translated, and merged into a unified multilingual training set.

---

2. Features

- ✅ **Intent Detection** using TF-IDF and Multinomial Naive Bayes
- 🌐 **Multilingual Responses** mapped via `reply_language` (`en`, `de`, `ta`)
- 🛡️ **Confidence Threshold** to handle uncertain predictions safely
- 🔄 **Relabeling of 'unknown' intents** using similarity matching
- 📈 **Model Evaluation** with precision, recall, F1 score, and confusion matrix
- 🧠 **EDA Visualizations** including WordClouds and intent distribution plots

---

3. Structre 

1. **Preprocessing**: Cleans and normalizes query text
2. **Vectorization**: Uses TF-IDF to convert queries into feature vectors
3. **Model Training**: Trained with balanced classes and optimized parameters
4. **Evaluation**: Metrics and heatmap to assess model accuracy
5. **Chat Function**: Accepts query + language, returns appropriate response with confidence check

---

4. 

```python
chat("How do I reset my ATM pin?", reply_language="en")
chat("Wie kann ich mein Konto überprüfen?", reply_language="de")
chat("எப்படி கடன் பெறலாம்?", reply_language="ta")

Project Structure

				nlp-chatbot-data/
				│
				├── README.md                         # Project overview and instructions
				│
				├── Datasets/                         # Raw and translated chatbot datasets
				│   ├── greetings_en.csv              # English greeting samples
				│   ├── loan_data.csv                 # Bank loan queries and responses
				│   ├── Dataset_Banking_chatbot.csv  # Original general banking dataset
				│   ├── banking-chatbot-multilingual.csv     # Merged multilingual queries
				│   ├── final_training_data.csv       # Cleaned and relabeled training data
				│   ├── final_banking_data_translated_fixed.csv  # Cleaned multilingual responses
				│   ├── Internatioanl_banking_data_cleaned.csv   # Final cleaned file for international responses
				│   └── intents.json                  # Labeled intents for chatbot model
				│
				├── code/                             # All notebooks and scripts# 🧠 Main chatbot pipeline & model logic
					   ├── Internationalbanking_Multilingual_Pipeline.ipynb  # Full training pipeline
					   ├── Dataset-Internatioanl_banking_cleaning.ipynb      # DE/TA column validation + Google Translate fix
					   └── banking_chatbotdataset_translator.ipynb           # Greeting dataset enhancement
					
					
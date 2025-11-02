# OpenSpec: Add Spam Email Classifier

## Summary
This proposal adds a spam classifier module for SMS messages using logistic regression and TF-IDF. It includes preprocessing, model training, evaluation, and a Streamlit-based UI.

## Motivation
Users need a lightweight, interpretable spam detection tool for short messages. Existing solutions are either too complex or lack transparency.

## Design
- **Input**: CSV file with `label` and `text` columns
- **Preprocessing**: Regex-based normalization (URLs, emails, phones, numbers)
- **Model**: Logistic regression with TF-IDF vectorization
- **Output**: Spam probability and predicted label
- **Interface**: Streamlit app with live input, batch prediction, and visualizations

## API
- `preprocess_emails.py`: Cleans raw text
- `train_spam_classifier.py`: Trains and saves model
- `predict_spam.py`: Applies model to new data
- `streamlit_app.py`: Interactive dashboard

## Extensibility
- Can support multilingual datasets
- Easily replace model with other classifiers
- UI supports additional metrics and examples

## Impact
- Improves spam detection accuracy
- Provides interpretable results
- Enables real-time classification

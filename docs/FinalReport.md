# Final Report: Spam/Ham Classifier

## Overview
This project builds a logistic regression classifier to detect spam messages in SMS data. It includes preprocessing, model training, evaluation, visualization, and an interactive web app.

## Workflow Summary
1. **Preprocessing**: Cleaned raw messages using regex-based normalization.
2. **Training**: Used TF-IDF vectorization and logistic regression. Model saved as `spam_logreg_model.joblib`.
3. **Evaluation**: Visualized confusion matrix, ROC curve, and precision-recall curve.
4. **Web App**: Built with Streamlit for live inference and interactive analysis.
5. **Batch Prediction**: Applied model to full dataset and saved predictions.

## Model Performance
- Accuracy: ~97%
- Precision: ~96%
- Recall: ~95%
- F1 Score: ~95%
- ROC AUC: ~0.98

## Visual Insights
- Spam messages contain frequent tokens like `<PHONE>`, `<URL>`, and `<NUM>`
- Ham messages contain more natural conversational phrases
- Threshold sweep shows trade-off between precision and recall

## App Features
- Live message classification
- Token frequency visualization
- Threshold adjustment slider
- Preloaded spam/ham examples

## Future Work
- Deploy to Streamlit Cloud
- Extend to multilingual datasets
- Add ensemble models for comparison

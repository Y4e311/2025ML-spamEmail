# Preprocessing Summary

This document outlines the preprocessing steps applied to the SMS spam dataset.

## Input
- Original file: `datasets/sms_spam.csv`
- Output file: `datasets/processed/sms_spam_clean.csv`

## Steps
1. **Lowercasing**: All text converted to lowercase for normalization.
2. **URL Replacement**: URLs replaced with `<URL>` using regex: `https?://\S+|www\.\S+`
3. **Email Replacement**: Email addresses replaced with `<EMAIL>` using regex: `\b[\w\.-]+@[\w\.-]+\.[a-zA-Z]{2,}\b`
4. **Phone Replacement**: Phone numbers replaced with `<PHONE>` using regex: `\b(?:\+?\d[\d\-\s]{7,}\d)\b`
5. **Number Replacement**: All digit sequences replaced with `<NUM>` unless `--keep-numbers` is specified.
6. **Punctuation Removal**: Non-word characters removed, preserving `<...>` tokens.
7. **Whitespace Normalization**: Multiple spaces collapsed into single space.

## Result
- Cleaned text stored in `text_clean` column
- Label preserved in `col_0` column

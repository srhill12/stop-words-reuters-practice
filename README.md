# Text Processing with NLTK: Reuters Corpus Analysis

This project demonstrates how to preprocess a text corpus from the Reuters database using Natural Language Processing (NLP) techniques provided by the Natural Language Toolkit (NLTK). Specifically, the project focuses on cleaning and tokenizing an article related to the 'crude' category in the Reuters dataset. The project includes functions for basic text preprocessing, including removing stopwords, applying regular expressions, and tokenizing text.

## Project Structure

- **Main Script**: The script imports the necessary libraries, retrieves an article from the Reuters corpus, and processes the text using custom functions for cleaning and tokenizing.
- **Text Processing Techniques**:
  - **Stopword Removal**: Removing common English words that do not contribute meaningful information to the analysis.
  - **Regular Expressions**: Cleaning the text by removing non-alphabetic characters.
  - **Tokenization**: Breaking down the text into individual words.
  - **Custom Stopwords**: Adding additional stopwords specific to the analysis context.

## Requirements

- **Python 3.x**
- **NLTK**: The Natural Language Toolkit is required for text processing. Install it using pip:
  ```bash
  pip install nltk
  ```

## Setup

Before running the script, ensure that you have the required NLTK data packages. The script will download them if they are not already installed:

```python
import nltk
nltk.download('punkt')
```

## Usage

1. **Retrieve an Article**:
   - The script retrieves the second article from the 'crude' category in the Reuters corpus.
   - Example:
     ```python
     crude_article = reuters.raw(fileids=reuters.fileids(categories='crude')[2])
     print(crude_article)
     ```

2. **Text Cleaning and Tokenization**:
   - **Basic Cleaning**: The `clean_text` function removes stopwords, non-alphabet characters, and tokenizes the text.
   - **Custom Cleaning**: The `clean_text_again` function does the same but with additional custom stopwords.
   - Example:
     ```python
     def clean_text(article):
         # ... [Function implementation]
     
     result = clean_text(crude_article)
     print(set(result))
     ```

3. **Example of Processed Output**:
   - After cleaning the text, the script prints the unique words left in the article.
   - Example:
     ```python
     result = clean_text(crude_article)
     print(set(result))
     ```

4. **Custom Stopwords**:
   - The `clean_text_again` function introduces additional stopwords that may be specific to the content or context of the analysis.
   - Example:
     ```python
     def clean_text_again(article):
         # ... [Function implementation]
     
     result2 = clean_text_again(crude_article)
     print(set(result2))
     ```

## Example

The following snippet demonstrates how the script processes the text:

```python
# Retrieve and print the article from the Reuters 'crude' category
crude_article = reuters.raw(fileids=reuters.fileids(categories='crude')[2])
print(crude_article)

# Clean and tokenize the article using custom stopwords
result = clean_text(crude_article)
print(set(result))

# Clean and tokenize the article using an extended set of stopwords
result2 = clean_text_again(crude_article)
print(set(result2))
```

## Conclusion

This project provides a foundation for working with text data in Python using NLTK. By using stopword removal, regular expressions, and tokenization, it becomes easier to preprocess and analyze text corpora. The inclusion of custom stopwords demonstrates how the cleaning process can be tailored to specific needs.


# Embeddings_English_Hindi

## Overview

The detailed ananlysis of the Process can be found in the **Report.pdf file, which details the complete process.**

This notebook demonstrates the process of

- Installing necessary libraries.
- Downloading pre-trained FastText models for English and Hindi.
- Limiting the vocabulary size to 100,000 words for each language.
- Preparing for further analysis or translation tasks using these embeddings.

## Steps and Execution

## 1. **Installation of Libraries**

- The notebook begins by installing `fasttext` and `torch` using pip. This step ensures that all required dependencies are available for the subsequent operations

## 2. **Downloading Pre-trained Models**

- FastText models for English (`cc.en.300.bin`) and Hindi (`cc.hi.300.bin`) are downloaded. These models contain pre-trained word vectors which are
  useful for various NLP tasks like translation, similarity analysis, etc.

## 3. **Loading Models**

- The downloaded models are loaded into memory. This step prepares the environment for accessing word vectors for both languages

## 4. **Limiting Vocabulary**

- To manage computational resources and focus on the most
  common words, the vocabulary for both English and Hindi is limited to
  100,000 words. This involves:
  - Retrieving the list of words from each model.
  - Slicing the list to include only the first 100,000 words.
  - Creating dictionaries where keys are words and values are their corresponding vector embeddings

## 5. **Preparation for Further Analysis**

- The notebook sets the stage for extracting word
  translation pairs from the MUSE dataset, which would be used for
  bilingual lexicon induction or translation tasks. However, the actual
  extraction process is not shown in the provided snippet

## Key Points

- **FastText** : Utilized for its efficiency
  in handling out-of-vocabulary words through subword information, which
  is particularly useful for languages with rich morphology like Hindi.
- **Model Limitation** : Limiting the vocabulary size helps in reducing memory usage and focusing on the most relevant words for the task at hand.
- **Bilingual Lexicon** : The mention of using the MUSE dataset suggests an intent to perform cross-lingual word embedding mapping or translation.

## Usage

This notebook can be used for:

- **Word Translation** : By mapping embeddings from English to Hindi or vice versa.
- **Cross-lingual Information Retrieval** : Finding similar words or documents across languages.
- **Language Model Training** : As a starting point for training models that require bilingual or multilingual embeddings.

## Limitations

- The vocabulary limitation might exclude less common but potentially important words for specific contexts or domains.
- The notebook does not show the actual application of the
  embeddings for translation or other tasks, which would be the next
  logical step.

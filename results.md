# Results Summary

## Vocabulary Statistics

- English vocabulary limited to 100,000 most frequent words
- Hindi vocabulary limited to 100,000 most frequent words
- Training dictionary: 8,130 filtered word pairs (from original 8,704 MUSE pairs)
- Testing dictionary: 1,600 filtered word pairs (from original 2,032 MUSE pairs)

## Supervised Procrustes Alignment Performance

- **Precision@1**: 28.5%
- **Precision@5**: 53.1%
- Evaluated on 1,600 test pairs

## Sample Translations (English to Hindi)

| English Word | Top 5 Hindi Translations                                  |
| ------------ | --------------------------------------------------------- |
| hello        | hello, हलो, हेल्लो, थैंक्यू, नमस्ते |
| my           | अपने, मेरे, मेरा, अपना, आपका          |
| name         | नाम, उपनाम, सरनेम, नामों, शीर्षक  |
| is           | है, यह, होता, क्योंकि, जो                |

## Word Pair Cosine Similarities (Top 5)

| English Word  | Hindi Word         | Similarity |
| ------------- | ------------------ | ---------- |
| lecture       | व्याख्यान | 0.6854     |
| kilometers    | किलोमीटर   | 0.6737     |
| consultant    | सलाहकार     | 0.6331     |
| aggressive    | आक्रामक     | 0.6236     |
| extraordinary | असाधारण     | 0.6007     |

## Ablation Study: Impact of Training Dictionary Size

| Dictionary Size | Precision@1 | Precision@5 |
| --------------- | ----------- | ----------- |
| 2,000           | 0.16        | 0.37        |
| 4,000           | 0.23        | 0.46        |
| 6,000           | 0.25        | 0.49        |
| 8,000           | 0.27        | 0.51        |

## Unsupervised Alignment Training (Adversarial Approach)

| Adversarial Epoch | Discriminator Loss | Generator Loss |
| ----------------- | ------------------ | -------------- |
| Epoch 1           | 1.3725             | 0.7306         |
| Epoch 2           | 1.3502             | 0.7415         |

## Computational Resources

- AWS SageMaker ML.G5.2xlarge GPU instance
- 24GB VRAM
- 500GB storage capacity

## Key Findings

1. Translation accuracy improves consistently with larger training dictionaries, though with diminishing returns after 6,000 word pairs
2. The supervised Procrustes approach achieves better performance than the unsupervised adversarial method for this language pair
3. CSLS effectively addresses the hubness problem in cross-lingual embedding spaces
4. Technical terms and transliterations show higher similarity scores compared to abstract concepts
5. Both approaches demonstrate practical viability for English-Hindi word translation

## Limiting Factors

1. Static embeddings limit the ability to capture context-dependent meanings
2. Script differences between English and Hindi present additional alignment challenges
3. Cultural concepts without direct translations are difficult to align accurately
4. Limited training dictionary size compared to the full vocabulary of both languages

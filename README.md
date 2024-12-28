# Text Processing and Tokenization Analysis: Alice in Wonderland

## Overview

This project explores various text processing and tokenization techniques applied to the text *Alice in Wonderland*. The methods span stopword removal, stemming, lemmatization, part-of-speech (POS) tagging, and Named Entity Recognition (NER). By comparing results from processing steps implemented using **NLTK** and **SpaCy**, the study identifies the most efficient and informative tokenization strategies.

---

## Results Summary

### Section 1: NLTK Processing

#### 1(C): Token Reduction and Informative Dictionary Creation
- **Processing Path A:**
  - Steps include stopword removal and stemming.
  - Token Count:
    - **1A.2:** 2650 unique tokens.
  - Observation: Stemming often obscures part-of-speech information, leading to less informative tokens.
- **Processing Path B:**
  - Steps include POS tagging and lemmatization.
  - Token Count:
    - **1B.3:** 3244 unique tokens.
    - Final Step (1B): 1888 unique tokens (nouns, adjectives, adverbs, verbs).
  - Observation: POS tagging and lemmatization create a more concise and informative token list compared to Path A.

#### 1(D): Additional Processing Steps
- **Path A:** Removed tokens with a length of 2 or fewer characters (e.g., "a", "is").
  - Impact: Minimal reduction in unique tokens but resulted in a more meaningful list.
- **Path B:** Removed tuples with frequency ≤ 2.
  - Final Count: 645 tuples.
  - Observation: Resulted in a concise and highly relevant list of terms with associated POS tags.

---

### Section 2: SpaCy Processing

#### 2(B): Efficiency and Results
- **Comparison to NLTK:**
  - SpaCy's built-in functions (e.g., `is_stop`, `is_punct`) streamlined processing steps.
  - Token Count:
    - SpaCy: 1750 unique tokens (almost 100 fewer than NLTK).
  - Observation: SpaCy produced a shorter, more informative token list.

#### 2(C): Named Entity Recognition (NER)
- **Additional Processing Step:**
  - Extracted named entities (e.g., people, places) and retained nouns, adjectives, verbs, and adverbs.
- **Results:**
  - Shorter and more informative token list.
  - Enhanced focus on key entities and terms relevant to *Alice in Wonderland*.

---

## Observations

1. **NLTK Processing:**
   - Path B (POS tagging + lemmatization) outperformed Path A (stemming) in producing concise and meaningful tokens.
   - Frequency-based filtering further improved relevance.

2. **SpaCy Processing:**
   - Significantly more efficient due to built-in functionalities.
   - Shorter token lists with greater informativeness compared to NLTK.
   - NER highlighted critical entities, enhancing the understanding of the text.

3. **Optimal Approach:**
   - SpaCy with NER and selective retention of important POS tags produced the most concise and informative list.

---

## Conclusion

The comparison between NLTK and SpaCy reveals that:
- **SpaCy** is superior for text processing tasks due to its efficiency and advanced features like NER.
- Retaining key POS tags (nouns, adjectives, verbs, adverbs) and named entities results in a highly relevant token list.
- Future processing steps can integrate advanced SpaCy features for further refinement.

---

## Code and Results

Detailed implementations and outputs are available in the accompanying notebook `HW_1.ipynb`.

---

## Questions?

Feel free to reach out for further information or collaboration opportunities.

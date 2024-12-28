1(C) - As I added more processing steps to the dictionary of words from the Alice in Wonderland text, the number of unique tokens goes down for when I went from A.1 to A.6 and B.1 to B.6. Immediately, the steps through 1B end up giving a more informative dictionary, since it gives the part of speech of the word on top of the word frequency in the text. In 1A.2, I had 2650 unique tokens and in 1B.3 I had 3244 unique tokens, and although the number of tokens does decrease by a great amount, the steps through 1.B help lead to a better list of words that is shorter and much more informative than doing the steps through 1.A. This is due to the fact that the stop words removal with stemming ends up making some words hard for identifying what part of speech they are, thus making it harder to identify the word in general, whereas the POS removal with lemmatization is much more efficient since the final count of unique tokens is 1888 for 1.B which is less than the count in 1.A and it also contains more important terms since its only the nouns, adjectives, adverbs, and verbs from the text.

1(D) - For steps A, I implemented an additional processing step that removes short tokens from the list of tokens, in which if the token only has a length of 2 characters then it will be removed. I did this since tokens that only have 1-2 characters are terms such as "a" or "is" and ultimately they are not that informative on the overall subject matter of the text "Alice in Wonderland". Once I implemented this, even though the count of unique tokens did not go down by that much, it still resulted in a more informative list of terms. For steps B, I implemented an additional processing step that removes tuples that have a very small frequency, in which it is a term that only shows up 1-2 times in the text. I did this since a term that only shows up 1-2 times in the text is most definitely not necessary to understand the overall subject matter. Once I implemented this, I got a very concise list of tuples where there were only 645 tuples, all with their respective parts of speech, so its a very short but informative list on the subject matter.

2(B) - Each processing step goes much faster and much more efficiently through using spacy, in which the code that is required to get the processing steps done is very concise sue to the fact that spacy has built in functions such as is_stop and is_punct to check if a word is a stopword or a punctuation mark. Compared to the results that I got from part 1 with nltk processing, spacy proved that it ends up making a shorter and informative list since it almost has 100 less tokens than both parts A and B with a count of 1750 unique tokens through spacy, and it definitely could be more informative if it was given more processing steps.

2(C) - After reading more about spacy and the features that it has I decided to implement NER as the additional processing step since by using NER, it can extract important entities such as names of people and places in the text "Alice in Wonderland" and these entities will end up making the list much more informative. Thus, I decided to keep only named entities and terms that are nouns, adjectives, verbs, and adverbs, since I believe will make a list that contains most words that are important to the subject matter of "Alice in Wonderland". After implementing this, I saw that the results were a shorter and much more informative list that can help identify what the text is much faster than the other lists through part 1.

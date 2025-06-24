## Output Comparison

* for all 3 docs for 'the' value of manual tf-idf  is very low(i.e 0), CountVectorizer is high (i.e. 1), Sklearn TF-IDFis low (i.e. 0.373)

* Words like "sun" and "moon" receive moderate scores in all three methods

* Words such as "star", "satellite", "celestial", and "bodies" appear only once across the corpus and are therefore given low scores by CountVectorizer, but high scores in both Manual TF-IDF and TfidfVectorizer

* Words like "and", "is", "are", and "a" got low scores

### Words like **"the"** appear in every document, making them **less informative**. In the TF-IDF formula, this leads to: IDF("the") = log(N / df("the")) ≈ log(3 / 3) = log(1) = 0  So their **TF-IDF score becomes 0**, even if the word occurs frequently. This is in contrast to CountVectorizer, which simply counts occurrences without evaluating informativeness.

## Conclusion
* Manual implementation closely matches Scikit-learn's TF-IDF output.

* TfidfVectorizer intelligently reduces the influence of common words.

* TF-IDF is superior when word importance needs to be captured, not just frequency.
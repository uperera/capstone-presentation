
Capstone Data Science Poject Presentation
========================================================
author: Uthpala Perera
date:   04/16/2016

Description : -  This presentation describes an application which Predicts the next expected word of a phrase typed by a user.    

URL:    https://uperera.shinyapps.io/capstone-project/

User Instructions: Access the [Application link](https://uperera.shinyapps.io/capstone-project/), type a phrase in the text box and hit submit to view the predicted word

Introduction
========================================================

- What it does: 
        -  Predicts the next expected word of a phrase using N-gram Modelling.
- Implementation:
        - Implemented in R as a Shiny Application
- Prediction Model:
        - N-gram Modelling with Natural Language Processing (NLP)
- Modelling Data:
        - Based on Samples from Blogs, News, Twitter data




Pre-Processing of Modelling Data
========================================================

1. Data is first randomly sampled into two sets,training and test.
2. Using Packages tm, RWeka and SnowballC training data is stripped of
        - non ascii characters,numercs and punctuation 
        - all characters are converted to lower case
        - stop words are removed using a custom list mystopwords
        - stemmed to strip suffixes and retain the basic word lemma
        - combined into one corpus of clean text data        
3. Next the corpus is tokenized into 1,2,3,4 and 5 grams  which are saved in a dataframe with their respective counts.
4. These data frames are loaded by the shiny application to calculate probabilites of occurence of a given word sequence.

Description of the Prediction Algorithm 
========================================================

1. The input phrase typed is cleaned with the same steps applied to training data and the last 4,3,2 and 1 word sequnces are saved into varibles.
2. These word sequences are searched in the next higher level ngram model created from training data for matches.

     eg: bigram "who-loves" is searched in trigram model to find matches such as "who-loves-me", "who-loves-cats" etc

3. The probability of each match is calculated using Kneser-Ney smoothing per references given in the last slide using the counts from the model.
4. The last word of the match with the highest probability is predicted as the next expected word.



Conclusion
=========================================================

1. The final model showed an accuracy of 20% with the test set.
2. Better accuracy can be attained by increased training data, but performance slows down.
3. Performance can be greatly improved by using Markov chains though for this application it was not possible due to the 1G memory constraint on the shinyapp server.

Sincere Thanks to Johns Hopkins Panel of lecturers and fellow students of the datascience course.

References: https://class.coursera.org/nlp/lecture/preview,
https://cran.r-project.org/web/packages/tm/vignettes/tm.pdf.
https://cran.r-project.org/web/packages/markovchain/vignettes/an_introduction_to_markovchain_package.pdf,
https://cran.r-project.org/web/packages/markovchain/vignettes/markovchainCrashIntro.pdf


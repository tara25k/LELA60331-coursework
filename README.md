# SENTIMENT CLASSIFIER FOR PRODUCT REVIEWS

# CONTENTS OF REPOSITORY
This repository contains the following files:
1. one_layer.ipynb: the one-layer model with all experimentation
2. final_one_layer.ipynb: the final one-layer model
3. two_layer.ipynb: the 2-layer model
4. Compiled_Reviews.txt: the product reviews
5. embeddings.npy: word2vec embeddings 
6. M.npy: bag of words embeddings
7. Data
    - popular.txt: english dictionary words for the vocabulary
    - positive-words.txt: positive words for the vocabulary
    - negative-words.txt: negative words for the vocabulary
    - stopwords.txt: a text file of stopwords

# RUNNING THE FINAL MODEL
In order to run the final model:
1. Open final_one_layer.ipynb
2. Run all cells

The final two cells show evaluation metrics and the outputs of the weight analysis.

# RUNNING THE EXPERIMENTATION
All experimentation is included in the file one_layer.ipynb. The cell outputs show the results of the base model.

The first 4 cells in this file have to be run in order for the model to run successfuly. After, the cells are split into:

- Defining the vocabulary
- Creating embeddings
- Running models
- Evaluation

There are 5 cells for defining the vocabulary the model uses. 
- VOCABULARY - BASE MODEL is the basic top 5000 words
- VOCABULARY - DOWNLOADED VOCAB either uses an English dictionary of popular words as the vocab or positive and negative sentiment words, depending on which part is uncommented
- VOCABULARY - REMOVED STOPWORDS removes stopwords and lowercases all tokens
- VOCABULARY - STEM WORDS runs a stemming algorithm on all the tokens to remove suffixes
- VOCABULARY - BIGRAMS includes bigrams as well as unigrams

These cannot be run together - only one can be run at a time.

The CREATE AN EMBEDDING MATRIX cell is for creating either a one-hot or bag of words embedding for each review.
In this cell, there are comments for whichever vocabulary of the above is used. One should be uncommented based on the vocabulary used above.

After this, you can either run the:
- BASE MODEL cell
- MODEL WITH L2 REGULARISATION cell
- MODEL WITH BATCH TRAINING cell

Once the model has finished running, running the final 2 cells will present performance metrics and weights analysis.

If, for example, you wanted to run the model with bigrams, one-hot embeddings and L2 regularisation, you would run:
- The first 4 cells
- The VOCABULARY - BIGRAMS cell
- The CREATE AN EMBEDDINGS MATRIX cell with the code below FOR BIGRAMS and FOR ONE HOT uncommented
- The MODE WITH L2 REGULARISATION cell
- The final two cells for evaluation


# RUNNING THE TWO LAYER MODEL
In order to run the two layer model:
1. Open two_layer.ipynb
2. Run all cells

However, this can take hours to run without a GPU. I would include the files of the weights of the trained two-layer model to show results, but github doesn't allow large files to be commited. 



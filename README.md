# Text-Mining-N-Gram-Analysis

# Overview

This program is designed to generate bigrams for a specific corpora.

# Process

The function I wrote in the program file has notes within each step but I will quickly summarise the program. I begin by importing the packages I need, and then jump right into the function build. To generate Bi Grams we want to basically glue two words together based on the probability of the 2nd word following the first within a specific corpora.

My generate bigram function has three input parameters, text, length, and start (startword). To begin the function, the input text is folded to lower case and checked for alpha numerics. The next lines assess what the start word will be. If one is provided in the function input, that will be used. Otherwise a random word from the input text will be chosen.

Next the function assigns NLTK's bigrams for the input text to bigram, and prints the start word. Now I am ready to start building bigrams. First I initialize an empty list called results and append the start word into it. Then I initialize an empty list bg_list which will hold the bigrams in the text that start with the start word and I iterate over all bigrams in the the bigram text list.

Now to begin the next bigram, I chose a random bigram from the bg_list we just built in the above paragraph and assign it to next_bigram. I then clear the bg_list in preparation for the next iteration of bigrams, and append the second word from next_bigram to my results list. This word will serve as my new start word for iterating over the texts bigrams.

Finally I create a while loop to repeat the above steps until the length of the results list is equal to length input into the function parameter or the default length of 10.

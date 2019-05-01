# AWESOM-O-4000-Chatbot

This repository contains code for a chatbot that uses lines from South Park's Cartman.

## Data

For my data, I took a look at South Park dialogue across seasons 1 through 18.
Cartman's lines consist of 14% of the script, making him the character with the most lines.
I got the data from Kaggle at the following link: https://www.kaggle.com/tovarischsukhov/southparklines

## Methodology

I first created a dictionary with Cartman's lines as values and the lines previous as the index.
Then, I created a corpus of the previous lines and turned it into a list of sentence tokens, 
which I then lemmatized and used TF IDF to create a sparse matrix of the lines.
For each user input the chatbot finds the previous line with the most cosine similiarty
and outputs the corresponding Cartman line using the dictionary.
User inputs that have a low cosine similairty cause the chatbot to output that it doesnt understand.
To visualize the results, i created a Flask app so users can actually talk to the chatbot.

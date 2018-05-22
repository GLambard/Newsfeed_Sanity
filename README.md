# Newsfeed_Sanity
A simple and sane newsfeed for m.phys.org - or how to quickly recommend the best topics

## Requirements
* pandas
* numpy
* bs4
* cython
* gensim
* scipy
* webbrowser
* jupyterlab
* https://code.google.com/archive/p/word2vec/ (download: GoogleNews-vectors-negative300.bin)

## Goal
During the last few years, I was spending much time to read once per week the newsfeed from http://m.phys.org. That's a good exercise for keeping touch with the latest advancements in Science. But with the drawback that it's taking time, a lot of time, and mainly because I had to go through a long list of different topics that I didn't need. Also, I needed a newsfeeder (recommander) which respects my tastes without having to go through undesired proposals.

## Solution
Compress my reading habits using word2vec from gensim in order to automatically extract the relevant science subjects to me. Also, as I was manually scrapping the news through the http://m.phys.org website, I was of course tempted to open this or this article according to its title. This is fairly simple I know, but this is generally what we do, right? So let's start. 

## The notebook
The notebook **newsfeed_sanity.ipynb** above performs the following tasks: 

* Check your browsing history from Google Chrome for the last three months
* Extract the browsed webpages from http://m.phys.org
* Use gensim to vectorize the articles' topic with word2vec
* Compute the score = (1-distance) (higher is better here) between past and new topics 
* Rank the new topics by score
* Display the new topics as hyperlinks in a html page.

# Feel free to fork it, copy it, change it and improve it for your tastes and targeted websites. 
## This was an individual excercice, not a tutorial. 

Coursera Data Science Capstone: Final Project Submission
========================================================
author: Cesar Fernandez
date: Mon Mar 09 00:00:42 2020


![header](C:/Users/Usuario/Documents/headers.png)

Predict the Next Word

Introduction
========================================================
type: sub-section
<span style="color:blue; font-weight:bold; font-size:0.7em">This presentation is created as Final Project Submission for the Coursera Data Science Capstone Course. </span>

<font size="5">
To try the apps, you can go to [HERE]- [https://cfernandez.shinyapps.io/coursera-final-submission/]. The app is build as a predictive text model combined with a shiny app UI. It can predict the next word as user types a sentence similar to the way most smart phone keyboards that we have today. *It using technology from Swiftkey*. 

</font>

Getting & Cleaning the Data
========================================================
type: sub-section

<span style="color:blue; font-weight:bold; font-size:0.7em">Before building the word prediction algorithm, data are first processed and cleaned as steps below:</span>

<font size="5">

- A subset of the original data was sampled from the three sources (blogs,twitter and news) which is then merged into one.
- Next, data cleaning is done by conversion to lowercase, strip white space, and removing punctuation and numbers.
- The corresponding n-grams are then created (Quadgram,Trigram and Bigram).
- Next, the term-count tables are extracted from the N-Grams and sorted according to the frequency in descending order.
- Lastly, the n-gram objects are saved as R-Compressed files (.RData files).

</font>

Description of the algorithm to make the prediction
========================================================
type: sub-section

<span style="color:blue; font-weight:bold;font-size:0.7em">The prediction model for next word is using n-gram and backoff models. Explanation how it work is as below:</span>

<font size="5">

1. It loaded a compressed data sets containing descending frequency sorted n-grams.
2. Before the prediction of the next word it will clean the user input words.
3. Algorithma that this app use is first it used Quadgram and if no Quadgram is found, back off to Trigram and If no Trigram is found, back off to Bigram and If no Bigram is found, back off to the most common word with highest frequency 'the' is returned.


</font>


Shiny Application
========================================================
type: sub-section

<span style="color:blue; font-weight:bold;font-size:0.7em">A Shiny application was developed based on the next word prediction model described previously as shown below. </span><img src="C:/Users/Usuario/Documents/step.png"></img>

![header](C:/Users/Usuario/Documents/step.png)

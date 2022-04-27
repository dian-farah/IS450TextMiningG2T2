# IS450TextMiningG2T2
Text Mining Project IS450 (Legal Text Summarization and Topic Modelling)

## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Setup](#setup)
* [Additional Files](#additional-files)
* [Troubleshooting](#troubleshooting)

## General info
Document review in law is the last stage before production. It is important to help lawyers understand the cases and formulate theories for trial. It can also be used for a broader purpose, such as carrying out due diligence assessments [10]. It is considered the most intensive and costly stage, taking up 70% to 80% of the cost of ediscovery [24]. To control costs, reviewers have to ensure they narrow their scope in order to minimize the number of documents needed to be reviewed.

To improve the process, we decided to perform topic modelling and extractive summarization so that lawyers can have a brief overview on the legal documents. The results of various models will be compared against each other to determine the best performing models.
	
## Technologies
Project is created with:
* Python
* NLTK
* Gensim
* Sumy
* ROUGE
* Scikit-learn
* Spacy
	
## Analysis
We used 9 extractive summarization algorithms and analysed their Rouge scores. Out of all the models, Edmundson (Cue) method and BERT-Extractive method are the best performing ones (Table 1). Overall, extractive summarization does not have higher performance, with Rouge scores below 50%. This could be because our reference summary in our dataset contains a lot of paraphrasing. An improvement would be to explore abstractive summarization techniques or combined summarization, where we shorten the sentences in the predicted summary.
<img width="602" alt="image" src="https://user-images.githubusercontent.com/66090549/165486991-9560722c-0df4-4f21-8e3e-0e1a088ee581.png">
 

## Additional Files
* [Round 1: Proposal Submission [PDF file]](https://github.com/dian-farah/Predicting-Traffic-Congestion-Application/files/6967225/Code.for.cities_.Prediction.of.road.congestion.by.Bzbz.pdf)
* [Round 2: Prototype Pitch Submission [PDF file]](https://github.com/dian-farah/Predicting-Traffic-Congestion-Application/files/6967232/Prediction.of.Traffic.Congestion.Phase.2._.Team.Bzbz.pdf)

## Troubleshooting
If you are unable to run the .py files, it may be due to certain python packages that you have not installed. You can follow [this link](https://www.youtube.com/watch?v=paRXeLurjE4) on how to install python packages into VSCode.

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
 
From our topic modelling implementation, we found an overlap in topics relating to transportation and security, as well as wildlife and emvironmental conservation (Image 1 and 2). We realised that LDA's results focuses heavily on employment, government, grants and taxes compared to BERTopic, which focuses on education, technology and immigration.

<img width="605" alt="image" src="https://user-images.githubusercontent.com/66090549/165490315-97083fdb-4977-46d1-8c42-bd129a92a402.png">
Image 1

<img width="605" alt="image" src="https://user-images.githubusercontent.com/66090549/165490394-79bc4283-587e-475a-af24-2fa79d6aff89.png">
Image 2

When analysing the coherence score, BERTopic performed better with a higher coherence score of 0.61276, compared to LDA of 0.48869. This could be because LDA ignores semantic relationshipd among words due to its Bag-of-Words representation. On the other hand, BERTopic can be fitted to embedding models which are used to cluster sematically similar documents. However, BERTopic uses a soft clustering method where documents which are not assigned to any clusters will form a -1 topic which could also be another reason for its high coherence score. We can propose human evaluation to better assess the 2 models' performance.

## Additional Files
* [Proposal Submission [Slides]](https://docs.google.com/presentation/d/1HtYLQXL2B5GU2LGNN40ITpX5a1bmooRI/edit?usp=sharing&ouid=104202635850447302819&rtpof=true&sd=true)
* [Final Presentation [Slides]](https://docs.google.com/presentation/d/1qqctPbCriEGc_yJ0SXMxjq1V49od74zG/edit?usp=sharing&ouid=104202635850447302819&rtpof=true&sd=true)
* [Final Report [PDF file]](https://drive.google.com/file/d/1iCser65mqzliJt1W0dlAqNejsknO4YVx/view?usp=sharing)

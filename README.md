# Jigsaw-Toxic-Severity-Challenge
This is my work in reference to the NLP competition hosted on Kaggle (https://www.kaggle.com/c/jigsaw-toxic-severity). 

Competition Details :
In this competition, we have to estimate toxicity scores for a set of about fourteen thousand comments.
Pairs of comments were presented to expert raters, who marked one of two comments more harmful — each according to their own notion of toxicity.
In this contest, when we provide scores for comments, they will be compared with several hundred thousand rankings. 
Our average agreement with the raters will determine our individual score.

Training Data:
No training data was provided for this competition. Only a validation data which  gives pair rankings (less-toxic -- more-toxic) for pair of comments is provided.
I have utilized the training data from previous Jigsaw competitions, namely:
  1) Toxic Comment Classification Challenge
  2) Jigsaw Unintended Bias in Toxicity Classification
  3) Jigsaw Ruddit Data
  
  along with the validation data for training .
  
  Methodology:
  The validation data provided for this competition is augmented by creating additional "Less-Toxic" & "More-Toxic" pairs from datasets from previous competitions.
  The text is then cleaned for HTML TAGS, IP addresses, emojis, punctuations, special characters etc. 
  The ROBERTA model is then finetuned using the training data and MarginRankingLoss is used as loss function.
  

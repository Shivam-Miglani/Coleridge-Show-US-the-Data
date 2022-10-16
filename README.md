# Coleridge Initiative - Show US the Data
[Competition link](https://www.kaggle.com/code/shivammiglani/spacy-3-0-transformer-custom-ner/data) | [Kaggle notebook](https://www.kaggle.com/code/shivammiglani/spacy-3-0-transformer-custom-ner)

The repo contains copy of the Kaggle notebook.

### Approach
Since research papers are large texts, I first created heuristics to find paragraphs which might contain dataset mentions using spacy's text matching/regex. On those paragraphs, I applied fine-tuned RoBERTa to extract custom dataset entity. 

The work involved 

- converting the annotations to CoNLL-U format, and 
- training the transformer for multiple epochs. 

To avoid overfitting only a subset of randomly selected labels was used along with randomly selected negative examples. 

The results of this approach were capable of achieving a top 100 rank. The winning solution trained another model instead of applying heuristics for the first step of filtering paragraphs

### Trained model inference example:

<img width="752" alt="image" src="https://user-images.githubusercontent.com/13565604/196010267-e6b8f69c-8a82-40ba-b6bf-621557d67be4.png">


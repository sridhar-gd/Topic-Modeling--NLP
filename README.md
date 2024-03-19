<p align="center"><img width=100% src="https://github.com/sridhar-gd/sridhar-gd/blob/main/Banner.png"></p>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
![Python](https://img.shields.io/badge/python-v3.11+-blue.svg)
![Dependencies](https://img.shields.io/badge/dependencies-up%20to%20date-brightgreen.svg)
![Contributions welcome](https://img.shields.io/badge/contributions-welcome-orange.svg)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)


# TOPIC MODELLING

Topic modeling is a text mining technique that identifies patterns of word co-occurrence in a large corpus of documents. These patterns are conceptualized as "topics," which can help discover latent structures in the corpus, group similar documents together, or serve as the basis of information retrieval. The objective of a topic modeling project is to analyze various topic models and make recommendations for the best practices in building a topic model. This includes making preliminary decisions about corpus preparation and setting parameters and hyper-parameters for the model.

In a topic modeling project, you may construct several topic models based on a single dataset to compare how the properties of a topic model change based on various parameters. For example, you can analyze the effects of different numbers of topics, alpha values, and parts of speech on a model. Each model can be tested in three different ways: a topic coherence test, a clustering test, and an information retrieval test. These tests are related to different use cases for topic models, such as analyzing a large corpus of documents, grouping documents based on similar content, and information retrieval.

In a topic coherence test, you can examine the words in each topic and label them as "coherent," "mixed," or "junk" based on whether at least 8 of the top 10 words come from the same semantic or contextual range. In a clustering test, you can identify what percentage of the corpus the model is able to assign one topic, to multiple topics, or to no topics at all. For the information retrieval test, you can use a module from gensim to build an index based on each model and evaluate its ability to return similar documents and on the similarity score it provides for those documents.


## Table of Contents

1. LDA - Latent Dirichlet Allocation
2. Step-by-step Procedure
3. Deployment
4. License


## LDA - Latent Dirichlet Allocation

Latent Dirichlet Allocation (LDA) is a generative probabilistic model used for topic modeling. It assumes that documents are generated from a mixture of topics, where each topic is a probability distribution over words. LDA models the joint probability of the words in a document and the topics that generate them.

In LDA, each document is represented as a bag-of-words, and the topics are represented as distributions over words. The model estimates the topic distribution for each document and the word distribution for each topic.


## Step-by-step Procedure

- Read the document using the *docx* library and stores it in the variable *doc*.
- Iterate through each paragraph in the document and prints the text of each paragraph using doc.paragraphs.
- Concatenate all the text from the paragraphs into a single string text.
- Tokenize the text into sentences using periods (".") as sentence delimiters and then tokenized into words using the NLTK library's *word_tokenize* function.
- Stop words (commonly used words like "the", "is", "and", etc.) are removed from the tokenized sentences.
- Construct a dictionary mapping unique words to integer IDs using the *corpora.Dictionary* class from the Gensim library.
- Convert each tokenized sentence into a bag-of-words representation using the dictionary. The resulting corpus is a list of bag-of-words representations of each sentence.
- The LDA model is trained on the corpus with specified parameters such as the number of topics *num_topics=5* and the number of passes *passes=50*.
- Print the top words for each topic using *lda_model.print_topics(num_words=5)*.
- Visualize the topics using the pyLDAvis library. The *pyLDAvis.gensim.prepare* function prepares the data for visualization, and *pyLDAvis.display* displays the visualization in the notebook..


## Deployment

Taking the model from development to deployment, Flask - a powerful web framework for Python - was utilized.


## License

MIT License

Copyright (c) 2024 Sridhar GD

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

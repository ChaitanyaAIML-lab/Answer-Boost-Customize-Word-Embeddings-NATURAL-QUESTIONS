## Customize-Word-Embeddings-for-LLMs

This Project uses dataset from the Google. This project aims to find weak negatives, and hard negatives first. Then calculate word embeddings using OpenAI's text-embedding-ada-002 word embedding model to compare the accuracy and performance with customized word embeddings. 

## Performance of Default Embeddings vs Customized Word Embeddings:
* To get a visual representation of the 'behaviour' or performance of the default embeddings, plot a distribution of cosine similarity.

* The graphs show how much the overlap there is between the distribution of cosine similarities for similar and dissimilar pairs. If there is a high amount of overlap, that means there are some dissimilar pairs with greater cosine similarity than some similar pairs.

* The accuracy computed here is the accuracy of a simple rule that predicts 'similar (1)' if the cosine similarity is above some threshold X and otherwise predicts 'dissimilar (0)'.


## **Data:**
The Natural Questions corpus represents a question-answering dataset, comprising 307,373 training examples, 7,830 development examples, and 7,842 test examples. Each instance consists of a query originating from google.com and an associated Wikipedia page. Within each Wikipedia page, there is an annotated passage, often referred to as the "long answer," which serves as a potential response to the query. Additionally, one or more short spans from this annotated passage contain the actual answer to the query. However, it is important to note that the long and short answer annotations may be left empty. When both the long and short answer annotations are empty, it indicates that no answer is available on the page. If the long answer annotation is non-empty but the short answer annotation remains empty, it suggests that the annotated passage provides a response to the question, yet no explicit short answer can be identified. Lastly, approximately 1% of the documents include a passage annotated with a short answer of "yes" or "no" instead of a list of short spans.

## Required Installation

**Dependencies:**

* openai: 0.28.1
* torch: 1.13.1+cpu
* numpy: 1.18.1
* pandas: 1.0.1
* plotly: 5.17.0
* tqdm: 4.42.1
* bs4: 4.8.2
* sklearn: 0.22.1
* re: 2.2.1
* matplotlib: 3.5.3
* sentence_transformers: 2.2.2
* tiktoken
* functools
  

## **Steps involved:**
 Following are the steps involved in our experiment. You can run notebook on your own to get more details on the experiment.

* 1. Data prep
    * transforming prepared data
      * negative sampling
        * i. Weak Negatives
        * ii. Hard Negatives

* 2. Word Embeddings:
    * How to get embeddings
    * Visualizing Embeddings
      * Queries and Passages in Latent Space

* 3. Model Training:
  * motivating example
  * performance before training
    * training
      * Training setup explanation
      * Explaining the 'Model' being trained
        
* 4. Model performance after training
  * visualizing before/after
    * Queries and Passages in Latent Space
      


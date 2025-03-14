# Precog - Language Representations
Precog Recruitment Task 
\n
# **Project Description**
This project explores word embeddings using co-occurrence matrices and pre-trained neural embeddings like Word2Vec and GloVe. We have further investigated the cross-lingual alignment, mapping pre-trained Hindi embeddings into pre-trained English embedding space using multivariate variables relating methods like Procrustes analysis.<br>
# **Datasets Used**
eng_news_tar.gz - The English news corpus <br>
**IITB Cross Language Corpus** <br>
test.en - Testing sentences in English   
test.hi - Testing sentences in Hindi   
dev.en - development sentences in English   
dev.hi - - development sentences in Hindi

# **Dependencies Used**   
nginx   
gensim   
numpy   
pandas   
matplotlib   
sckit-learn   
scipy   
umap-learn   
   
# **Method Followed**   
**Task-1**   
**Preprocessing**   
I have loaded the 300k English corpus. After loading it, I preprocessed the corpus after loading the corpus completely. Then, a co-occurrence matrix was built and it was, then converted to a sparse matrix for better efficiency.   
<br>
**Generating Word embeddings**   
We create word embeddings through co-occurrence-based embedding methods like SVD. This method was tried with different window sizes and visualizing it with the help of PCA to get the optimal window size. I then used pre-trained neural embeddings like Word2Vec and GloVe on the same corpus
<br>
**Evaluating Word Embeddings**   
We computed cosine similarity using SimLex-999 for the optimal window size and we have visualized the embeddings using UMAP & PCA.   
<br>
**Task 2**   
**Preprocessing**
We loaded the pre-trained neural embedding method of FastText by Wikipedia for both English and Hindi language. We did this task using two methods, one an inefficient one using a self-made dictionary and the other from English-Hindi parallel sentences from IIT Bombay English-Hindi Corpus. The second method involved the usage of a large amount of data which helped the model to cause underfitting. We tokenized the sentences of this corpus and built a bilingual dictionary. The Hindi and English word vectors were extracted for aligned words which we got from the corpus. 
<br>
**Hindi Embeddings to English & Evaluation**   
We used Procrustes analysis for the process of aligning Hindi embeddings to English. Procrustes analysis method computes an optimal transformation matrix which will transform Hindi embeddings to English embeddings.    
Finally, cosine similarity was measured for the words before & after alignment. The final embeddings were plotted using PCA to visualize alignment effectiveness. 

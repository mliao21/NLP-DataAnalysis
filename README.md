# NLP-DataAnalysis

There are three files with 150,000 questions that are asked about three programming languages in Stack Overflow, java, python, and javascript. The files aren't available in this repository due to the size limit.
* SO-Java contains 50,000 questions from Stack Overflow that are tagged as `java’.
* SO-Python contains 50,000 questions that are tagged as `python’.
* SO-Javascript contains 50,000 questions that are tagged as `javascript’.
* The posts are collected from Stack Overflow posts table. Details about Stack Overflow posts table can be found here: https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede

## Exercise 1
Instructions are contained inside [this jupyter notebook file](NLP-Exercise1.ipynb)

## Exercise 2 
Instructions and code are inside [this jupyter notebook file](NLP-Exercise2.ipynb)

**Question 1 is included in the file**

**Question 2**

For each programming language, the task is to find the most similar question with an accepted answer to the highest scored question in the language that does not have any accepted answer. Suppose, for Java, you had four questions with score (Q1: 3, Q2: 4, Q3: 5, Q4:3). Suppose Q3 and Q4 do not have any accepted answer. Then Q3 is the highest scored question without any accepted answer. Suppose Q1 and Q2 have accepted answer. You will then see how similar Q1 and Q2 are to Q3. Suppose Q1 has similarity value of 0.8 with Q2 has a similarity value of 0.2 with Q3. Then you will return Q1 as the output. Such approaches are normally used to recommend solutions to an unanswered question in Stack Overflow.

For each programming language, I wrote the function in python and returned the top three most similar questions. For similarity analysis, I used cosine similarity. I used standard preprocessing of the texts before computing similarity:
1. Tokenization into words
2. Stop words removal
3. Noise reduction (e.g., removal of punctuation)
4. Stemming

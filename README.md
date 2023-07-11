# Analysis-of-Research-Database
Subject: Big Data Analytics 	
Project: Analysis of Research Database
Group Size: 2

# Part 1: Information Fusion across two databases. 
We had 2 databases. The first one (D1) is a data table(1 lakh rows) consisting of paperid and title. The second one (D2) is a collection of pdf files of 10k research papers (20 GB Data). We had to find the common research articles in the two databases and represent them in a particular format. That is, For every Paper (Title) in D1, if it exists in D2 (access title and references from pdf), then create a list containing the papers(should be present in D1) it has cited. The pertinent information that we are looking for in a document in D2 is the title and the references. Then, add this (title: list of cited papers) as a (key: value) pair in a dictionary. The goal is to create such a dictionary of citation relationships amongst papers in D1 by taking the help of documents in D2. There was no exact match between the paper titles in D1 and D2. We have used similarity algorithms to deal with this issue. We also represented the above result with the help of a directed networkx graph. 

# Part2: Find all the candidate document pairs
With the help of data obtained in Part 1, Using LSH, we obtained all the candidate document pairs. We varied the similarity threshold and the shingling parameter to observe changes in the result.

# Part 3: Number of unique authors for each publication venue
We have used the Flajolet Martin algorithm for this task and Implemented a data analytics pipeline using Apache Kafka. We created a topic for each publication venue. Depending on the venue of the articles in the bibliography, the author's list was streamed to the corresponding topic. The extracted authors were then processed using the algorithm.







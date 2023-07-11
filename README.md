# Analysis-of-Research-Database
Subject: Big Data Analytics 	

Project: Analysis of Research Database

Group Size: 2

# Part 1: Information Fusion across two databases. 
We had two databases. The first database (D1) comprised a data table with 100,000 rows, containing paper IDs and titles. The second database (D2) consisted of a collection of 10,000 research papers in PDF format, totaling 20 GB of data. Our objective was to identify the research articles that were common to both databases and present them in a specific format.

To accomplish this, we followed a process: For each paper (title) in D1, we checked if it existed in D2. If it did, we accessed the corresponding title and references from the PDF file. Next, we created a list that included the papers (which should be present in D1) cited by the current paper. The crucial information we sought in the documents of D2 were the title and references.

We then constructed a dictionary, where each entry was in the form of a (title: list of cited papers) key-value pair. This dictionary captured the citation relationships among the papers in D1, with the assistance of the documents in D2. It is important to note that there were no exact matches between the paper titles in D1 and D2. To address this challenge, we utilized similarity algorithms.

Furthermore, we visualized the obtained results by utilizing a directed networkx graph, representing the citation relationships between the papers.


# Part2: Find all the candidate document pairs
With the help of data obtained in Part 1, Using LSH, we obtained all the candidate document pairs. We varied the similarity threshold and the shingling parameter to observe changes in the result.

# Part 3: Number of unique authors for each publication venue
We have used the Flajolet Martin algorithm for this task and Implemented a data analytics pipeline using Apache Kafka. We created a topic for each publication venue. Depending on the venue of the articles in the bibliography, the author's list was streamed to the corresponding topic. The extracted authors were then processed using the algorithm.







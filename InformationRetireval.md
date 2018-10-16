# Simple Search Engine with Apache Lucene

## Abstract
This tutorial focuses on building a search engine with apache lucene and we discuss the concepts of precision and recall. Lucene is a open source information retrieval library, in this tutorial we will be using lucene with java.

### Prerequisites
Instructions for using lucene
In this tutorial I'm using eclipse IDE
```
Make sure you have java installed on your system and path are configured
You can download java jdk from [here](https://www.java.com/en/download/)
You can download eclipse from [here](https://www.eclipse.org/downloads/packages/release/neon/2/eclipse-ide-java-developers)
You can download apache Lucene from [here](https://lucene.apache.org/core/downloads.html)
Unzip and store the folder in your desired directory
```

### Import JARs to your project folder
```
Create a JAVA project in eclipse
Right click on the project folder and select cofigure build path from the build path drop down
Click on Add External JARs
* from (lucene_directory/analysis/common) add lucene-analysers-common-(version).jar
* from (lucene_directory/core) add lucene-core-(version).jar
* from (lucene_directory/queryparser) add lucene-queryparser-(version).jar
```
Now we are good to start the implementation

### Important Terms
* Positives - Whatever our system retrieves from the data it has are refered to as positives
* Negatives - All the documenst which are not retrieved are called negatives
* True positives(tp) - Documents which satisfy the query and are retrieved by our system
* Fasle positives(fp) - Documents which do not satisfy the query but are retrieved by our system
* True negatives(tn) - Documents which satisfy the query but are not retrieved by our system
* False negatives(fn) - Documents which do not satisfy the query and are not retrieved by our system

Before we jump into the implementation of the search engine we need to know how to evaluate our system. Any search engine is evaluated with the precision and recall metrics.

Precision is defined fraction of retrieved docs that are relevant 
Recall is defined as fraction of relevant docs that are retrieved 
* Precision P = tp/(tp + fp) 
* Recall  R = tp/(tp + fn)

### Dataset
The data that we will be working with for this tutorial is Game of Thrones, the dataset contains a total of 67 documents. The data in each document is scraped from the wiki page of each episode of Game of Thrones



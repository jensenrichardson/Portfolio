# Portfolio
Hello! Here is where I keep my data science portfolio.

My name is Jensen Richardson and I am a recent graduate and aspiring data scientist with experience integrating data and disparate
tools to provide insights. I am searching for a place to continue my ambition to discover, learn, and solve
unfamiliar problems.

## 1. Regression — [Kaggle's Ames Iowa House Price Challenge](https://www.kaggle.com/code/jensenrichardson/house-prices-prediction)
In the following notebook, I go through several different models to predict house prices for homes in Ames, Iowa.
After a lengthy exploratory data analysis, I develop models using traditional linear methods, gradient boosted trees, and a deep learning neural network.
I use tools from pandas, scikit-learn, and keras most intensively.

## 2. Classification — [Kaggle's Space Titanic Disaster Challenge](https://www.kaggle.com/code/jensenrichardson/space-titanic-model)
The problem is to predict whether or not passengers on the Space Titanic are transported into another dimension.
This is a classification problem and has many missing entries (we get the information from a damaged computer core).
I use tools from pandas, scikit-learn, XGBoost, and keras most intensively.

## 3. Data Structure — [Data Ingest Script](https://github.com/jensenrichardson/dna-preprocess/blob/main/parse_samples.py)
The data ingest script I wrote while a part of the Big Data in Biology lab at UT was used to start an intensive data pipeline (available in the same repository).
The specific script available here comprehends a complex data structure, and not only
verifies that structure, but makes the structure available for other commands in the pipeline.

The structure is that of a single sample of genetic information, ie one person. Within that sample are readgroups, which would be a specific run of a sequencing machine. Finally, each readgroup is made of two individual read files (read one and read two) which is a byproduct of the sequencing process.
Each level of the structure is used in different stages of the end pipeline, so different tools may require different sorts of outputs. For example, a tool that aligns the individual reads to a reference genome may operate only at the read file level (it only refers to the two read files) and one that calls genetic mutations would operate on a whole sample so it would need information on all the readgroups that a single sample has.

The script is well commented, well structured, and flexible code that I used to extend other parts of the pipeline over the course of a year and a half (the git history is fairly blank because almost all of my work was completed on a headless cluster at [TACC](https://www.tacc.utexas.edu).

# Portfolio
Hello! Here is where I keep my data science portfolio.

My name is Jensen Richardson and I am a recent graduate and aspiring data scientist with experience integrating data and disparate
tools to provide insights. I am searching for a place to continue my ambition to discover, learn, and solve
unfamiliar problems.

## Nutrition Facts for my Projects
1. Regression — [Kaggle's House Price Challenge](https://www.kaggle.com/code/jensenrichardson/house-prices-prediction)
   * Goal: Predict home prices in Ames, Iowa.
   * Data: Observations are houses with features that include sale price, age, quality, rooms, etc.
   * Tools: pandas, scikit-learn, keras
3. Classification — [Kaggle's Space Titanic Disaster Challenge](https://www.kaggle.com/code/jensenrichardson/space-titanic-model)
   * Goal: Predict whether passengers on the "space titanic" would be saved from a space anomaly.
   * Data: Observations are passengers with features of whether they were saved, cabin location, age, name, etc.
   * Tools: pandas, scikit-learn, XGBoost, keras
5. Data Structure — [Data Ingest Script](https://github.com/jensenrichardson/dna-preprocess/blob/main/parse_samples.py)
   * Goal: Parse the structure of genomic sample names to be fed into an analysis pipeline.
   * Data: Folder of samples of genomic data which gets split into a nested data structure.
   * Tools: pandas, regex, core python

## 1. Regression — [Kaggle's Ames Iowa House Price Challenge](https://www.kaggle.com/code/jensenrichardson/house-prices-prediction)
In the following notebook, I go through several different models to predict house prices for homes in Ames, Iowa.
After an exploratory data analysis, I develop models using traditional linear methods, gradient boosted trees, and a deep learning neural network.
I use tools from pandas, scikit-learn, and keras most intensively.

The parts of which I am most proud are
  * the exploratory data analysis which incorporates many ,
  * the Ordinal Data Encoder which (ever so slightly) outperforms the default scikit-learn version (though it does require quite a bit of legwork), and
  * the extensive use of flexible scikit-learn pipelines which enabled the quick testing of many different models and processing features.

## 2. Classification — [Kaggle's Space Titanic Disaster Challenge](https://www.kaggle.com/code/jensenrichardson/space-titanic-model)
The problem is to predict whether or not passengers on the Space Titanic are transported safely off the ship or are lost to a space anomaly.
This is a classification problem and has many missing entries (we get the information from a damaged computer core).
I use tools from pandas, scikit-learn, XGBoost, and keras most intensively.

I want to highlight the way that I
  * evaluated each feature to see which of them merited the most focus before my lengthy EDA,
  * tried using multiple models with a simpler data set before settling on the model to use with the whole data set,
  * used a keras FeatureSpace to simplify and speed up the process of imputing and dealing with the missing variables.

## 3. Data Structure — [Data Ingest Script](https://github.com/jensenrichardson/dna-preprocess/blob/main/parse_samples.py)
The data ingest script I wrote while a part of the Big Data in Biology lab at UT was used to start an intensive data pipeline (available in the same repository).
The specific script available here comprehends a complex data structure, and not only
verifies that structure, but makes the structure available for other commands in the pipeline.

Some background information not meant for the script itself:
  * The structure is that of a single sample of genetic information, ie one person. Within that sample are readgroups, which would be a specific run of a sequencing machine. Finally, each readgroup is made of two individual read files (read one and read two) which is a byproduct of the sequencing process
  * Each level of the structure is used in different stages of the end pipeline, so different tools may require different sorts of outputs. For example, a tool that aligns the individual reads to a reference genome may operate only at the read file level (it only refers to the two read files) and one that calls genetic mutations would operate on a whole sample so it would need information on all the readgroups that a single sample has.
  * The script is well commented, well structured, and flexible code that I used to extend other parts of the pipeline over the course of a year and a half (the git history is fairly blank because almost all of my work was completed on a headless cluster at [TACC](https://www.tacc.utexas.edu).

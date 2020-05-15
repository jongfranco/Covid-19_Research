# Covid-19_Research
Analysis of Covid-19 research papers using NLP

## Part 1: Unsupervised learning using LDA.

I used Google's Colab to put together this Jupyter Notebook. I have a separate Notebook for data cleanup which I will commit later.

### Motivation for this project:
It's fair to say that this analysis is not complete. There is a lot to do in order to extract meaningful information from the research papers. Having said that this is a good starting point. I personally wanted to apply an unsupervised NLP technique and figure out if I could classify documents in a meaningful way. Obviously, the Covid-19 topic itself is a huge motivation.

### Files in the repository:
Covid-19_Research.ipnyb is a Jupyter Notebook build using Google Colab.
The data in the Notebook was parsed in a separate Notebook which I will commit later. I currently load the data from 'ai2_research_data.db' which I saved as SQLite table after extracting data from PDFs encoded as JSON.

#### Sections in the Jupyter Notebook:
- Load data: loads data from SQList db file.
- Feature Exploration: Initial data exploration of the dataframe.
- Data cleanup: All the necessary clean up steps before LDA can be applied.
- Visualize cleansed data: Visualization of cleansed data.
- LDA training: Applying LDA to the data.
- Data Exploration using LDA: Interpretation of the results.

### Libraries used:
- Standard libraries pandas, numpy
- sqlalchemy for loading SQLite db
- re for applying regex
- gensim for dictionary and LDA
- matplotlib, seaborn & counter for visualizations
- nltk for tokenization, lemmatization, stemming

### Interpretation of results
![GitHub Logo](/top4topics.png)

The above figure gives the best summary of results. It provides a view of 4 topics with their most prominent words. Topics can be used for classifying documents. Obviously the general context of each topic is subjective and dependent upon words within each topic. To further illustrate the point, take a look at the titles within Topic 0.

- ‘Dromedary camels in northern Mali have high seropositivity to MERS-CoV-NC-ND license (http://creativecommons.org/licenses/by-nc-nd/4.0/)',
- ‘Communicable Diseases and Outbreak Control REVIEW 20’,
- ‘An Appropriate Lower Respiratory Tract Specimen Is Essential for Diagnosis of Middle East Respiratory Syndrome (MERS)’,
- ‘Article history: Cross-Country Comparison of Case Fatality Rates of COVID-19/SARS-COV-2’,
- ‘COVID-19 in the Shadows of MERS-CoV in the Kingdom of Saudi Arabia’,
- ‘The outbreak of COVID-19: An overview’,
- ‘The Middle East Respiratory Syndrome-How Worried Should We Be? A NOVEL VIRUS IS IDENTIFIED IN SAUDI ARABIA’, ‘Cardiac problem and MERS’,
- ‘A Case Report of a Middle East Respiratory Syndrome Survivor with Kidney Biopsy Results’, ‘
- ‘MERS Vaccine Candidate Offers Promise, but Questions Remain’

By looking at the titles of the research paper you can make out there are similarities between the research papers. The results from this analysis is articulated in a post here:
- https://medium.com/@nikhilnarayan.11/unsupervised-learning-on-covid-19-research-papers-using-lda-7011d8a1411b

### References
- https://www.machinelearningplus.com/nlp/topic-modeling-visualization-how-to-present-results-lda-models/
- https://www.kaggle.com/vukglisovic/classification-combining-lda-and-word2vec
- http://videolectures.net/mlss09uk_blei_tm/
- Data Source: https://www.semanticscholar.org/cord19/download

----------------------------------------------------------------------------------------------------------------------------------------

## Part 2: Extracting insights from Covid-19 Research Papers

### Files in the repository:
Besides the research papers data mentioned above, I have used NDC drug data to create a list of drug names that I want to search in the research papers. NDC drug database is available here:
https://www.fda.gov/drugs/drug-approvals-and-databases/national-drug-code-directory

#### Sections in the Jupyter Notebook:
- Research Paper data: set of activities that help me filter out Covid-19 related research papers.
- NDC drug data clean up: set of activities to clean up drug data, extract Non-proprietary name and add a few missing drug names.
- Research Data - Add matching Drug data: set of activities to identify occurrence of drug names in the research paper.
- Analyze Drug Data - Extract meaningful insights through analysis.

### Interpretation of Results
A detailed explanation of the results is available in the post here:


### References
- https://www.kaggle.com/vukglisovic/classification-combining-lda-and-word2vec


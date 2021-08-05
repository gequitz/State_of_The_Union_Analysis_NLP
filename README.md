# State_of_The_Union_Analysis_NLP
Metis Project 4: Unsupervised Learning and Natural Language Processing (NLP)

By: Gabriel Equitz
____________________________________________________________________________

## Problem Statement
- The State of the Union (SOTU) is an annual address by the President of the United States to congress. Every year, the President discusses the previous year and lays out his agenda for the coming year.
- My goal is to see how Topics in the State of the Union addresses have changed over more than 200 years of American history using Natural Language Processing
- Find historical insights with Topic Modeling and Unsupervised Learning.
- Additionally, I want to see what speeches are most similar to one another based on the Topics gained from Unsupervised Learning
- State of the Union speeches from 1790-2018 were chosen to be analyzed.

## Data Sources
https://www.kaggle.com/rtatman/state-of-the-union-corpus-1989-2017 (Kaggle notebook containing 228 .txt files of State of the Union speeches from 1790 to 2018)
- I originally tried using State of the Union speeches contained within Natural Language Toolkit (NLTK), but it only includes less than half of all SOTU speeches, and was therefore not viable for me

## Methodology
- Get .txt files of all SOTU speeches, clean them, sort by year (not alphabetically), and put in a dataframe.
- Count Vectorize words (into vectors) using TF-IDF. Remove common stop words, max_df = 0.42, min_df = 0.01.
- Compare how similar speeches are to one another (df_similarity), finding which president's speeches are most alike.
- Topic Modeling using NMF: Plot top 15 words for each of 8 components (Unsupervised Learning).
- Plots of Components over Time (Nicer Visualizations made with Tableau are in the Presentation Slides).
- Clustering the components using KMeans (this and next step use pickle file of 'main')
- Make Scatter Plot and Histogram of Speech Clusters over Year
- Prepare slides and give 5 minute presentation in Zoom meeting

## Files
- 'state_of_union_main.ipynb' contains all SOTU files (which are put in a dataframe), data cleaning, Speech similarity comparisons, all files related to Topic Modeling, and a Word Cloud in Jupyter Notebook
- 'state_of_union_clusters.ipynb' uses pickle file from Main and contains Clustering of components using KMeans, and Scatter Plot and Histogram of Speech Clusters over Year (Jupyter Notebook file)
- 'Project 4_ SoTU Unsupervised Learning.pptx' contains Powerpoint file of Presentation slides
- 'Project_4_ SoTU Unsupervised_Learning_presentation.pdf' contains PDF file of Presentation slides 

## Findings
- Some Topics appear to share similarities
- Topics 1 & 2 relate to Economics, with Topic 1 having language that was common in the 19th century, while Topic 2 show Economic language since the 1960s. It is apparent how presidents' State of the Union addresses have in regards to economics have changed: Terms such as 'Silver' and 'Gold' are used less, while 'Jobs' and 'Budgets' are more prevalent now. Additionally, terms like 'Families', 'Child', and 'Parents' have replaced terms like 'Cents', 'Bonds', and 'Notes'
- Topics 3 & 5 show how language on industry and government institutions have evolved with the industrial revolution and increased size of the US government. Topic 5 represents the time period from 1900-1930, the Progressive Era & Roaring 20s (interestingly, this also seems to be the period of time with the least war based on our analysis). Terms like 'Interstate', 'Industrial', 'Tariff', and 'Corporations' dominated. Topic 3 shows the creation and expansion of federal welfare programs from FDR in the 1930s to Ronald Reagan in the 1980s. Terms like  'Programs', 'Farm', 'Budget', 'Housing', 'Assistance' are prevalent.
- Topics 4, 6, 7, 8 show how war and US foreign policy has changed: Who is fighting, what are the technologies, and more. Topic 4 represents the early period from 1790-1830, focusing on 'French', 'Spain', and 'Tribes' as they represent foreign policy adversaries in this time period. Topic 6 represents the period from 1830-1880, showing Andrew Jackson, the peak of the Mexican American War, U.S. Civil War and Reconstruction (Topic 6 basically ends wtih Reconstruction's conclusion). Topic 6 has top words including 'Mexico', 'Texas', 'Territorial', and 'Consequence'. Topic 7 represends the World Wars and Cold War (1915-1990), highlighting words such as 'Soviet', 'Communist', 'Fighting', 'Japanese', and "Aggression', as well as technologies such as 'Atomic' and 'Planes'. It peaks from 1951-1953, the first years of Soviet Nuclear Weapons and the Korean War. Topic 8 represents the Iraq War and Terrorism. This topic was clearly highest during George W Bush's SOTUs following 9/11 (2002-2008). Terms include  'Iraqi', 'Terrorists', 'Qaeda', 'Saddam', and 'Fight'
- The most similar speeches, when not by the same president, are typically those of their immediate predecessors and successors.


## Libraries, Packages, and Notebook used
- [Python OS](https://docs.python.org/3/library/os.html)
- [Python Pickle](https://docs.python.org/3/library/pickle.html)
- [NLTK](https://www.nltk.org/)
- [Pandas](https://pandas.pydata.org/)
- [Scikit-learn](https://scikit-learn.org/stable/)
- [Matplotlib](https://matplotlib.org/)
- [Tableau](https://www.tableau.com/)
- [Jupyter](https://jupyter.org/)

## Blog link
https://equitzcode.wordpress.com/2021/03/26/metis-project-4-blog-state-of-the-union-nlp-analysis/

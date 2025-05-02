# PPOL6801_TextAsData_FinalProject
Repository for "Context of evaluation and data in 21st century Federal Policy: A Text Analysis Approach" Project

Completed for the Text as Data Course at Georgetown University, Spring 2025 Semester

# Directory:



## Code:

- **FinalProject_APIsearch_clean.Rmd**: The code used to query and compile documents from the Federal Register and collect the full text that is the corpus for analysis.
- **FinalProject_KeyWordsAnalysis_clean.Rmd**: The code that examines the frequency of specific tokens within the corpus and applies the Key Words in Context Technique on the corpus
- **FinalProject_WordEmbeddings_clean.Rmd**: The code that implements a Global Vectors for Word Representation (GloVe) model on the subsets of the corpus



## Data

- **TAD_finalproject_corpus_sample.csv**: A small subset of the compiled corpus and documents as an example of what the overall dataset looked like. Please reach out to author for a copy of the entire dataset.
-  **token_files**: set of the 6 presidential administration token files (.Rds) used for the word embedding models. Include padding after removal of stopwords and other highly frequent words (>99 percent) from model. Please reach out to author for copies of the Democrat and Republican token files.


## Results

- **Word_embedding_results**: Files that contain the identified 20 Nearest Neighbors to specific target words (based on cosine similarity). File names indicate whether the are at the presidential administration (pterm) level or presidential party (party) level, and whether results were based on a weighted count or not. 

-**Figures**: 

  * **KWIC**: example key words in context (KWIC) results that identify the most common words around specific target tokens
  * **Annual_Trends**: line graphs that portray the annual usage of specific unigrams and bigrams between 2021-2025. The y-axis for these graphs is a pseudo log of the count
  * **Presidential_Term**: bar graphs that portray the frequency of specific unigram and bigrams by presidential administration, from Bush first administration through Trump second administration




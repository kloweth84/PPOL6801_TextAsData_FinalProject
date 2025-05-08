# PPOL6801_TextAsData_FinalProject
Repository for "Context of evaluation and data in 21st century Federal Policy: A Text Analysis Approach" Project

Completed for the Text as Data Course at Georgetown University, Spring 2025 Semester

# Abstract


This study explores how the use of evaluation and data terminology has changed in the federal government during the 21st century. Analyzing a corpus of federal agency rules and presidential documents from the Federal Register (2001-2025), the research investigates the frequency of terms such as "evaluation," "data analysis," and "artificial intelligence," and employs GloVe word embedding models to analyze changes in their contextual usage. The findings reveal fluctuations in term usage over time and presidential administrations and differences in usage between agency rules and presidential documents.  Additionally, the results from the word embedding models highlight variations in the contextualization of terms across presidential administrations and political parties.

# Methodology


- **Count Frequency of Specific Terms**:  With the tokenized corpus, compare particular token frequency across documents. Using the corpus variables like publication date of the documents and presidential administration, I also compare how the frequency changes based on subgroups.

- **Key Words in Context (KWIC)**: The KWIC technique allows for closer examination of the words surrounding a particular target token. It extracts the target token from the corpus and provides the context window (the tokens directly before and after the target) to show how the term is getting used.

- **Global Vectors for Word Representation (GloVe) word embedding model**:  GloVe is an unsupervised learning algorithm that captures information about tokens through a multi-dimensional vector representation (Pennington et al., 2014). It utilizes feature co-occurrence to measure the linguistic or semantic similarity of words in a corpus (Pennington et al., 2014). The model also uses an optimized cost function to learn and improve embeddings iteratively. More information on this type of model can be found here: https://nlp.stanford.edu/projects/glove/ 


# Repo Directory:

- **TAD_ProjectProposal_Loweth**: Initial project proposal submitted for assignment as part of the Text as Data Class
- **TAD_finalpaper_Loweth**: Final report documenting project findings 
- **TAD_finalproject_Loweth_slidedeck**: Slide deck providing an overview of results

## Code:

- **FinalProject_APIsearch_clean.Rmd**: The code used to query and compile documents from the Federal Register and collect the full text that is the corpus for analysis.
	* **Input**: None
	* **Output**: A csv file containing information on official federal government documents that met certain search criteria. Each row represents a unique observation. Includes the field of analysis, body_text, that contains the entire document's complete text. 
	
- **FinalProject_KeyWordsAnalysis_clean.Rmd**: The code that examines the frequency of specific tokens within the corpus and applies the Key Words in Context Technique on the corpus
	* **Input**: The csv file created using the APIsearch code file
	* **Output**: Figures on term frequency over time and presidential administrations. Example figures found in the Figures folder. 
- **FinalProject_WordEmbeddings_clean.Rmd**: The code that implements a Global Vectors for Word Representation (GloVe) model on the subsets of the corpus
	* **Input**: The csv file created using the APIsearch code file or the token .Rds files found in the data folder. 
	* **Output**:  The csv files in the Word_embedding_results folder.



## Data

- **TAD_finalproject_corpus_sample.csv**: A small subset of the compiled corpus and documents as an example of what the overall dataset looked like. Please reach out to author for a copy of the entire dataset.
-  **token_files**: set of the 6 presidential administration token files (.Rds) used for the word embedding models. Include padding after removal of stopwords and other highly frequent words (>99 percent) from model. Please reach out to author for copies of the Democrat and Republican token files.


## Results

- **Word_embedding_results**: Files that contain the identified 20 Nearest Neighbors to specific target words (based on cosine similarity). File names indicate whether the are at the presidential administration (pterm) level or presidential party (party) level, and whether results were based on a weighted count or not. 

-**Figures**: 

  * **KWIC**: example key words in context (KWIC) results that identify the most common words around specific target tokens
  * **Annual_Trends**: line graphs that portray the annual usage of specific unigrams and bigrams between 2001-2025. The y-axis for these graphs is a pseudo log of the count
  * **Presidential_Term**: bar graphs that portray the frequency of specific unigram and bigrams by presidential administration, from Bush first administration through Trump second administration




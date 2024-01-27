<h1>GAYATRI FRAUD DETECTION RESEARCH PAPER PLAN LAYOUT</h1>

## Phase 1: Preparation and Definition

1. #### Review Existing Fraud Data Dictionary:
   Searching for an existing fraud detection data dictionary published by established authors on the internet.
2. #### Evaluate Suitability:
   Evaluating whether or not and to what extent the extracted data dictionary is suitable for this research paper and its proposed methodologies.
3. #### Customize dictionary for required data sets:
   Customising the existing fraud data dictionary to suit objectives for the paper and identifying whether any additional terms or definitions need to be included.
4. #### Compile the dictionary:
   Compiling the finalized fraud data dictionary in a document or
   database.

## Phase 2: Data Preprocessing and Feature Engineering

1.  #### Data Collection:
    Obtain the annual financial reports of companies of suitable domains/categories expected by the methodology to be used.
2.  #### Extracting Data from Annual Reports using text processing (possibly OCR software)
    Use the (OCR) software to extract data in textual form from the scanned images of annual reports. Apply text processing techniques such as tokenization, NER,
    and POS tagging to analyze and extract structured data from the
    OCR results.
3.  #### Cross-referencing with Fraud Data Dictionary:
    Match the extracted financial data fields with the terms and definitions provided in the fraud data dictionary.
4.  #### Data Cleansing:
    ##### Deduplication -
    Python libraries such as pandas provide functions like drop_duplicates() to identify and remove duplicates based on specified columns or SQL queries can be used to deduplicate data in relational databases by selecting distinct records or using aggregation functions
5.  #### Feature Selection:

    Apply feature selection methods such as Correlation-based
    Feature Selection (CFS) and Firefly Optimization Algorithm to identify the most
    relevant financial features for fraud detection. These techniques help in selecting
    features that have a significant impact on fraud detection while reducing dimensionality and computational complexity. Refer to the fraud data dictionary to guide the selection of financial features. Prioritize features that align with the terms and definitions outlined in the fraud data dictionary, as they are more likely to contribute to accurate fraud detection.
    (i) Use libraries like scikit-learn in Python to implement CFS.
    (ii) Calculate the correlation between each feature and the target variable (fraud/non-fraud) and the intercorrelation among features.
    (ii) Select features that have high correlation with the target variable and low intercorrelation with each other.

    - ##### CFS:
      It evaluates the individual merit of each feature and the correlation between features to select a subset of features that are highly correlated with the target variable but uncorrelated with each other.
    - ##### The Firefly Optimization Algorithm:
      can be applied to feature selection by optimizing a fitness function that evaluates the importance of features based on their contribution to the classification task.
    - ##### Prioritize Dictionary-aligned Features

    #### Note:

    OCR software scans and processes images of text from documents, such as scanned copies of annual reports. It can extract specific types of information, such as financial figures from tables or key metrics from textual descriptions. It also analyses the layout and structure of documents to identify sections, paragraphs, and headings which helps in preserving the hierarchical structure of the text and maintaining the context during the extraction process.

    #### Note:

    a. In the context of annual reports, tokenization can be used to segment the text into
    individual sections such as financial statements, footnotes, and management discussions.
    b. NER(Named entity recogniser) can help extract key information from annual
    reports, such as company names, financial metrics, and dates of financial events.

## Phase 3: Model Development and Algorithm Selection - Hybrid Neural Network with Textual Analysis

### Implementation:

1.  #### Programming Language: Python
2.  #### Libraries to be Used:
    - TensorFlow or Keras for building neural networks.
    - Pandas for data manipulation and preprocessing.
    - Scikit-learn for model evaluation and metrics.
3.  #### Converting text into numerical representations suitable for neural network processing using word embeddings and padding & truncating sentences:
    - Word2Vec and GloVe are popular word embedding techniques used to represent words as dense vectors in a continuous vector space. These techniques capture semantic relationships between words by learning representations based on the context in which they appear.
    - TF-IDF is a statistical measure used to evaluate the importance of a word in a document relative to a collection of documents. It represents words as numerical vectors, where each dimension corresponds to a unique word in the vocabulary, and the value indicates the importance of the word in the document.
    - Padding involves adding zeros (or other placeholders) to sequences that are shorter than a specified length. This ensures that all sequences have the same length, which is necessary for feeding data into neural networks that expect fixed-size inputs.
    - Truncating involves removing tokens from sequences that exceed a specified length. This is necessary to ensure that sequences are not too long, as excessively long sequences can lead to memory issues and computational inefficiency.
    #### Note:
         - The hybrid model can incorporate structured financial features aligned with the fraud data dictionary while also analyzing textual data from MD&A sections.
         - Neural networks can automatically learn relevant features from the data, including linguistic cues mapped to terms in the fraud data dictionary.

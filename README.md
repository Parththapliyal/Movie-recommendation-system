
# **Movie Recommendation System**

## 📄 **Overview**
This project implements a **Movie Recommendation System** using **Content-Based Filtering**. It recommends similar movies based on a selected movie title by analyzing various attributes such as **genres**, **keywords**, **cast**, and **crew**. The system uses **cosine similarity** to measure the similarity between movies, leveraging natural language processing techniques for text vectorization.

---

## 🛠️ **Workflow**

### 1. **Data Preprocessing**
- **Loaded datasets**:
  - `tmdb_5000_movies.csv`
  - `tmdb_5000_credits.csv`
- **Merged datasets** on the movie title.
- Retained the following key columns for analysis:
  - **movie_id**: Unique identifier for movies.
  - **title**: Name of the movie.
  - **overview**: Brief description of the movie.
  - **genres**, **keywords**, **cast**, and **crew**.

### 2. **Data Cleaning**
- Checked for missing values and dropped rows with null `overview` values.
- Removed duplicate rows.
- Processed JSON-like strings in **genres**, **keywords**, **cast**, and **crew** columns to extract relevant attributes:
  - Extracted **top 3 actors** from the cast.
  - Extracted **director** from the crew.

### 3. **Feature Engineering**
- **Generated tags**:
  - Combined **overview**, **genres**, **keywords**, **cast**, and **crew** into a single text column called `tags`.
  - Converted text to lowercase and removed spaces from the tags for consistency.
- Applied **Stemming** using the **Porter Stemmer** to reduce words to their root form.

### 4. **Text Vectorization**
- Converted the `tags` column into numerical vectors using the **Bag of Words (BOW)** model:
  - Used `CountVectorizer` with a maximum of **5000 features**.
  - Removed stopwords (e.g., "the", "is", etc.).
- Generated a sparse matrix representing movie vectors.

### 5. **Similarity Calculation**
- Calculated pairwise similarity scores between movie vectors using **cosine similarity**.
- Cosine similarity measures the angle between vectors:
  - **Smaller angle = Higher similarity**.

### 6. **Recommendation System**
- Implemented a function to recommend **top 5 movies** similar to a selected movie.
- Example output:
  - Input: **Spectre**
  - Recommendations:
    1. Skyfall
    2. Quantum of Solace
    3. Never Say Never Again
    4. From Russia with Love
    5. Octopussy

### 7. **Serialization**
- Saved the processed data and similarity matrix for deployment using **pickle**:
  - `movies.pkl`: Contains movie metadata.
  - `similarity.pkl`: Contains the similarity matrix.

---

## 🧰 **Technologies Used**
- **Programming Language:** Python
- **Key Libraries:**
  - `pandas` and `numpy` for data manipulation.
  - `ast` for parsing JSON-like strings.
  - `nltk` for natural language processing.
  - `sklearn` for vectorization and similarity calculation.
  - `pickle` for model serialization.

---

## 📊 **Results**
- **Content-Based Filtering** accurately recommends similar movies based on genres, keywords, and cast/crew attributes.
- Successfully processed and vectorized **4806 movies** from the dataset.
- Recommendations are highly relevant, as shown by example outputs.

---

## 🔍 **Key Insights**
- **Bag of Words (BOW)** model effectively converts text data into numerical representations for similarity calculations.
- **Cosine similarity** is an efficient metric for finding related movies, outperforming Euclidean distance in text vectorization tasks.
- The system can be extended to include collaborative filtering for enhanced recommendations.

---

## 📁 **Project Files**
- 📂 **pdf:**
  - 
-
- 📂 **Jupyter Notebook:** # **Movie Recommendation System**

## 📄 **Overview**
This project implements a **Movie Recommendation System** using **Content-Based Filtering**. It recommends similar movies based on a selected movie title by analyzing various attributes such as **genres**, **keywords**, **cast**, and **crew**. The system uses **cosine similarity** to measure the similarity between movies, leveraging natural language processing techniques for text vectorization.

---

## 🛠️ **Workflow**

### 1. **Data Preprocessing**
- **Loaded datasets**:
  - `tmdb_5000_movies.csv`
  - `tmdb_5000_credits.csv`
- **Merged datasets** on the movie title.
- Retained the following key columns for analysis:
  - **movie_id**: Unique identifier for movies.
  - **title**: Name of the movie.
  - **overview**: Brief description of the movie.
  - **genres**, **keywords**, **cast**, and **crew**.

### 2. **Data Cleaning**
- Checked for missing values and dropped rows with null `overview` values.
- Removed duplicate rows.
- Processed JSON-like strings in **genres**, **keywords**, **cast**, and **crew** columns to extract relevant attributes:
  - Extracted **top 3 actors** from the cast.
  - Extracted **director** from the crew.

### 3. **Feature Engineering**
- **Generated tags**:
  - Combined **overview**, **genres**, **keywords**, **cast**, and **crew** into a single text column called `tags`.
  - Converted text to lowercase and removed spaces from the tags for consistency.
- Applied **Stemming** using the **Porter Stemmer** to reduce words to their root form.

### 4. **Text Vectorization**
- Converted the `tags` column into numerical vectors using the **Bag of Words (BOW)** model:
  - Used `CountVectorizer` with a maximum of **5000 features**.
  - Removed stopwords (e.g., "the", "is", etc.).
- Generated a sparse matrix representing movie vectors.

### 5. **Similarity Calculation**
- Calculated pairwise similarity scores between movie vectors using **cosine similarity**.
- Cosine similarity measures the angle between vectors:
  - **Smaller angle = Higher similarity**.

### 6. **Recommendation System**
- Implemented a function to recommend **top 5 movies** similar to a selected movie.
- Example output:
  - Input: **Spectre**
  - Recommendations:
    1. Skyfall
    2. Quantum of Solace
    3. Never Say Never Again
    4. From Russia with Love
    5. Octopussy

### 7. **Serialization**
- Saved the processed data and similarity matrix for deployment using **pickle**:
  - `movies.pkl`: Contains movie metadata.
  - `similarity.pkl`: Contains the similarity matrix.

---

## 🧰 **Technologies Used**
- **Programming Language:** Python
- **Key Libraries:**
  - `pandas` and `numpy` for data manipulation.
  - `ast` for parsing JSON-like strings.
  - `nltk` for natural language processing.
  - `sklearn` for vectorization and similarity calculation.
  - `pickle` for model serialization.

---

## 📊 **Results**
- **Content-Based Filtering** accurately recommends similar movies based on genres, keywords, and cast/crew attributes.
- Successfully processed and vectorized **4806 movies** from the dataset.
- Recommendations are highly relevant, as shown by example outputs.

---

## 🔍 **Key Insights**
- **Bag of Words (BOW)** model effectively converts text data into numerical representations for similarity calculations.
- **Cosine similarity** is an efficient metric for finding related movies, outperforming Euclidean distance in text vectorization tasks.
- The system can be extended to include collaborative filtering for enhanced recommendations.

---

## 📁 **Project Files**
- 📂 **pdf:**-https://github.com/Parththapliyal/Movie-recommendation-system/blob/main/Movie%20recommendation%20system.pdf
- **jupyter notebook** - https://github.com/Parththapliyal/Movie-recommendation-system/blob/main/movie%20recommendation%20system.ipynb
  - 
---

## ⚙️ **Future Enhancements**
- Incorporate **Collaborative Filtering** to consider user preferences.
- Add features like ratings and reviews to improve recommendations.
- Deploy the system as a web application using **Flask** or **Streamlit**.

---


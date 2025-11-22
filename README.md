# imdb-nlp-movie-recommender
Interactive IMDb movie recommendation system using NLP, TF-IDF, regression, classification, and clustering models. As well as a simple age/genre filtering based on user input.
# 🎬 IMDb NLP Movie Recommender System

This project is an **interactive movie recommendation system** built using NLP techniques, TF-IDF similarity, clustering, classification/regression models, and a simple age/genre filtering engine. The goal is to help users find movies that match their **mood**, **preferences**, or **demographic restrictions** using both structured and unstructured data from the IMDb dataset.

Users can interact with the system through an easy **Gradio web interface**, allowing free-text mood search, genre filtering, and browsing the dataset.

---

##  **Key Features**

### 1. **Age-Based Filtering**
Restricts movies according to the user’s age using certificates such as:
- G, PG, PG-13, R, TV-14, TV-MA, etc.

### 2. **Genre Filtering**
Users can filter movies by genre selections, such as:
- Action, Drama, Thriller, Romance, Animation, Horror, Comedy, and more.

### 3. **NLP Mood-Based Movie Search**
Users can enter any text describing what they feel like watching, such as:
- “dark psychological thriller about obsession”
- “light feel-good comedy for the weekend”
- “crime movie with mystery and plot twists”

Two search engines are supported:
- **TF-IDF Vectorizer (unigrams + bigrams)**
- **SentenceTransformer embeddings (semantic)**

### 4. **Machine Learning Models**
The notebook includes:
- **Regression models** to predict IMDb rating
- **Classification models**
- **Clustering** (e.g., KMeans) for thematic grouping
- **Dimensionality reduction** (PCA/SVD)

### 5. **Interactive Web Interface (Gradio)**
The app provides:
- Age filtering  
- Genre selection  
- Keyword/mood search  
- ML-based recommendations  
- Ranking by rating or similarity  

---

##  **Project Structure**
imdb-nlp-movie-recommender/
│
├── README.md # Project documentation
├── requirements.txt # Dependencies
├── project1.ipynb # Main notebook
│
├── data/
│ └── imdb_top_1000.csv # Dataset 
│ └── extra_description.xlsx # Dataset 

---

## **Dataset Information**

The project uses the **IMDb Top 1000 Movies Dataset** from Kaggle.

Key columns used:
- `Series_Title`
- `Genre`
- `IMDB_Rating`
- `Meta_score`
- `No_of_Votes`
- `Gross`
- `Certificate`
- `Released_Year`
- `Overview`
- `Full_text` (main text used for NLP)

## **Installation**

### 1. Clone the repository
git clone https://github.com/<your-username>/imdb-nlp-movie-recommender.git
cd imdb-nlp-movie-recommender

### 2. Install dependencies
pip install -r requirements.txt

### 3. Add the dataset
data/imdb_top_1000.csv

data/extra_description.xlsx

## **How to Run the Project**

### **Run through Jupyter Notebook**
1. Open **project1.ipynb**
2. Run all cells sequentially  
3. The Gradio app will launch at a link 

## **Methods Used**

### **1. Data Cleaning & Preparation**
- Handling missing values  
- Converting numerical columns  
- Extracting main genre  
- Building combined text (`Full_Text`)  

### **2. NLP Processing**
- **TF-IDF Vectorizer**:  
  - unigrams + bigrams  
  - max_features = 15000  
- **SentenceTransformer embeddings**:
  - `all-MiniLM-L6-v2` (or similar)

### **3. Feature Engineering**
- Runtime in minutes  
- Year grouping  
- Normalized text fields  

### **4. ML Models**
- Random Forest  
- Logistic Regression  
- KMeans clustering  
- PCA/SVD dimensionality reduction  

### **5. Recommender Function**
The core mood-based recommender:
- Vectorizes user mood input  
- Calculates cosine similarity  
- Returns top-k similar movies  

---

## **Gradio Interface**

The interface includes:

### ✔ Mood text input  
### ✔ Age slider  
### ✔ Genre selection  
### ✔ Choice of NLP model (TF-IDF or Embeddings)  
### ✔ Number of recommendations  
### ✔ Minimum rating filter  
### ✔ Clean and simple movie table output  

---

## **Future Enhancements**

- Add TMDB API for live posters and more metadata  
- Deploy the app online (HuggingFace Spaces / Gradio Cloud)  
- Implement collaborative filtering  
- Fine-tune transformer models  
- Expand dataset to 50K+ movies  

---

## **License**
This project is released under the **MIT License**.

---

## **Authors**
Developed by Tala Alothaim, Norah Abanumay, Hanadi Alrajhi, Nouf Aloraier as an academic project to explore NLP, machine learning, and recommender systems.


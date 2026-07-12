# 🎬 Movie Recommendation System

A **Content-Based Movie Recommendation System** built using **Python**, **Scikit-learn**, and **Streamlit**. The application recommends movies based on their content by analyzing genres, overview, keywords, cast, and director. Movie posters are dynamically fetched using the **OMDb API**.

---

## 🚀 Features

- 🎥 Content-Based Movie Recommendations
- 🔍 Search movies by title
- 🧠 TF-IDF based feature extraction
- 📊 Cosine similarity for recommendation
- ⚡ On-demand similarity computation (memory efficient)
- 🖼️ Movie posters fetched using OMDb API
- 🌐 Interactive web interface with Streamlit
- 📱 Responsive and modern UI

---

## 🌐 Live Demo

**Streamlit App:** *(Add your deployment link here)*

---

## 📂 Project Structure

```
Movie-Recommender/
│
├── app.py
├── requirements.txt
├── README.md
├── .gitignore
│
├── model/
│   ├── movies.pkl
│   └── vectors.pkl
│
└── .streamlit/
    └── secrets.toml
```

---

## 🛠️ Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- Streamlit
- Requests
- OMDb API

---

## 📊 Dataset

**TMDB 5000 Movies Dataset**

The dataset contains movie metadata including:

- Title
- Overview
- Genres
- Keywords
- Cast
- Crew
- Movie ID

---

## 🧠 Recommendation Pipeline

The recommendation system follows a content-based filtering approach.

### Data Preprocessing

- Removed duplicate records
- Handled missing values
- Extracted genres, keywords, cast, and director
- Combined selected features into a single **tags** column

### Feature Engineering

The following movie features are combined:

- Overview
- Genres
- Keywords
- Cast
- Director

### Vectorization

The combined tags are transformed into numerical vectors using **TF-IDF Vectorizer**.

### Recommendation

When a user selects a movie:

1. The movie's TF-IDF vector is retrieved.
2. Cosine similarity is computed between the selected movie and all other movies.
3. The Top 5 most similar movies are recommended.
4. Posters are fetched dynamically from the OMDb API.

---

## 📈 Workflow

```
TMDB Dataset
      │
      ▼
Data Cleaning
      │
      ▼
Feature Engineering
(Overview + Genres + Keywords + Cast + Director)
      │
      ▼
TF-IDF Vectorizer
      │
      ▼
Sparse Feature Matrix
      │
      ▼
User selects a movie
      │
      ▼
Cosine Similarity
(on-demand)
      │
      ▼
Top 5 Recommendations
      │
      ▼
Fetch Posters (OMDb API)
```

---

## 💡 Why On-Demand Cosine Similarity?

Instead of storing a large similarity matrix (≈176 MB), the application computes similarity only for the selected movie at runtime.

### Advantages

- Lower memory usage
- Faster deployment
- No large similarity file required
- Better scalability

---

## ⚙️ Installation

Clone the repository

```bash
git clone https://github.com/Madhubalakumar07/Movie-Recommender.git
```

Navigate into the project

```bash
cd Movie-Recommender
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## 🔑 OMDb API Setup

Create a `.streamlit/secrets.toml` file

```toml
OMDB_API_KEY = "YOUR_API_KEY"
```

For Streamlit Community Cloud, add the same key under **App Settings → Secrets**.

---

## ▶️ Run the Application

```bash
streamlit run app.py
```

---

## 🔮 Future Enhancements

- Hybrid Recommendation System
- User Authentication
- Movie Filtering by Genre
- Search Autocomplete
- Personalized Recommendations
- Watchlist Feature
- User Ratings
- Movie Details Page
- Trailer Integration
- Collaborative Filtering

---

## 👨‍💻 Author

**MADHUBALAKUMAR S**

- GitHub: https://github.com/Madhubalakumar07

---

## ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub.

---

## 📄 License

This project is licensed under the MIT License.

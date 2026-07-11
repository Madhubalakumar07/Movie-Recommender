# 🎬 Movie Recommendation System

A **Content-Based Movie Recommendation System** built using **Python**, **Scikit-learn**, and **Streamlit**. The application recommends movies based on their content by analyzing features such as genres, overview, keywords, cast, and director. Movie posters are dynamically fetched using the **OMDb API**.

---

## 📌 Features

- 🎥 Recommend movies based on content similarity
- 🔍 Search and select any movie from the dataset
- 🖼️ Display movie posters using the OMDb API
- ⚡ Fast recommendations using cosine similarity
- 🌐 Interactive web interface built with Streamlit
- 🎨 Modern and responsive user interface

---

## 🚀 Demo

**Live Demo:** *(Add your Streamlit link here after deployment)*

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
│   └── similarity.pkl
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

Dataset used:

**TMDB 5000 Movies Dataset**

The dataset contains information such as:

- Movie Title
- Overview
- Genres
- Keywords
- Cast
- Crew
- Movie ID

---

## ⚙️ How It Works

1. Load the TMDB 5000 movie dataset.
2. Clean and preprocess the data.
3. Combine the following features:
   - Overview
   - Genres
   - Keywords
   - Cast
   - Director
4. Convert the combined text into vectors using **CountVectorizer**.
5. Calculate cosine similarity between movie vectors.
6. Recommend the top 5 most similar movies.
7. Fetch movie posters using the **OMDb API**.

---

## 🧠 Machine Learning Workflow

```
Dataset
    │
    ▼
Data Cleaning
    │
    ▼
Feature Engineering
(Overview + Genres + Keywords + Cast + Director)
    │
    ▼
CountVectorizer
    │
    ▼
Feature Vectors
    │
    ▼
Cosine Similarity
    │
    ▼
Top 5 Similar Movies
```

---

## 📦 Installation

Clone the repository

```bash
git clone https://github.com/Madhubalakumar07/Movie-Recommender.git
```

Move into the project directory

```bash
cd Movie-Recommender
```

Install the required packages

```bash
pip install -r requirements.txt
```

---

## 🔑 OMDb API Setup

Create a `.streamlit/secrets.toml` file

```toml
OMDB_API_KEY = "YOUR_API_KEY"
```

Or add the secret in **Streamlit Community Cloud**:

```
OMDB_API_KEY="YOUR_API_KEY"
```

---

## ▶️ Run the Application

```bash
streamlit run app.py
```



## 📈 Future Improvements

- Hybrid Recommendation System
- User Authentication
- Search Autocomplete
- Movie Filtering by Genre
- Movie Details Page
- Watchlist Feature
- User Ratings
- Deploy using Docker

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository.
2. Create a feature branch.
3. Commit your changes.
4. Open a Pull Request.

---

## 👨‍💻 Author

**MADHUBALAKUMAR S**

- GitHub: https://github.com/Madhubalakumar07
- LinkedIn: www.linkedin.com/in/madhubalakumar-s-9a4b00329

---

## ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub!

---

## 📄 License

This project is licensed under the MIT License.

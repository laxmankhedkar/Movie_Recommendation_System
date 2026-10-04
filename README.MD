# 🎬 Movie Recommender System

A **Content-Based Movie Recommender System** built using Python and the **TMDB 5000 Movie Dataset**.

The application recommends movies that are similar to the movie selected by the user. The recommendation system uses movie information such as **genres, keywords, cast, crew, and other movie-related features** to identify similar movies.

The project is deployed using **Streamlit** and provides a simple web interface where users can search for a movie and get recommendations.

### 🌐 Live Demo

[Movie Recommender System – Streamlit App](https://u-rex13-movie-recommender-system-app-2ap1dd.streamlit.app/)

---

## 📌 Project Overview

The main goal of this project is to understand how a **Content-Based Recommendation System** works and implement it as a working web application.

The overall workflow is:

```text
TMDB Movie Dataset
        ↓
Data Cleaning & Preprocessing
        ↓
Feature Selection
        ↓
Combine Movie Features
        ↓
Text Vectorization
        ↓
Similarity Calculation
        ↓
Movie Recommendations
        ↓
Streamlit Web Application
```

For example, if a user selects **Iron Man**, the system analyzes the movie's features and recommends other movies with similar characteristics.

---

## 🎯 Features

- Search for movies from the available dataset
- Content-based movie recommendations
- Uses movie metadata to find similar movies
- Simple Streamlit user interface
- Pre-computed recommendation data using pickle files
- Deployed as a web application
- Uses TMDB 5000 Movie Dataset

---

## 🧠 What is Content-Based Recommendation?

A **Content-Based Recommendation System** recommends items that are similar to the item selected or previously liked by the user.

Instead of comparing users with other users, it looks at the **features of the items**.

For movies, features can include:

- Genre
- Keywords
- Cast
- Director
- Movie overview
- Other movie metadata

For example:

```text
User selects:
Iron Man

        ↓

System analyzes:
Genre
Keywords
Cast
Crew
Movie information

        ↓

Similarity calculation

        ↓

Recommended Movies:
Movies with similar features
```

So, if a user likes a particular movie, the system recommends other movies that have similar content.

---

## 🔍 How the Recommendation System Works

### 1. Dataset

The project uses the **TMDB 5000 Movie Dataset**.

Two datasets are used:

```text
tmdb_5000_movies.csv
tmdb_5000_credits.csv
```

These datasets contain information about movies, including:

- Movie ID
- Title
- Genres
- Keywords
- Cast
- Crew
- Overview
- Other movie metadata

---

### 2. Data Preprocessing

The datasets are loaded and processed using Python.

The required movie features are selected and combined to create useful information for the recommendation model.

---

### 3. Feature Creation

Important movie features are combined into a single representation.

For example:

```text
Genres + Keywords + Cast + Crew + Overview
```

This combined information is then used to determine movie similarity.

---

### 4. Similarity Calculation

The system calculates how similar one movie is to other movies.

Movies with higher similarity scores are considered better recommendations.

The resulting similarity information is stored in:

```text
similarity.pkl
```

---

### 5. Recommendation

When the user selects a movie, the application:

```text
Selected Movie
      ↓
Find Movie Index
      ↓
Compare Similarity Scores
      ↓
Select Most Similar Movies
      ↓
Display Recommendations
```

---

## 📂 Project Structure

```text
Movie-Recommender-System/
│
├── .git/
├── .gitattributes
├── .gitignore
│
├── app.py
│
├── movie-recommender-system.ipynb
│
├── movie_dict.pkl
├── movies.pkl
├── similarity.pkl
│
├── tmdb_5000_credits.csv
├── tmdb_5000_movies.csv
│
├── Procfile
├── requirements.txt
├── setup.sh
│
└── README.md
```

---

## 📄 Role of Each File

### `app.py`

The main Python file used to create and run the Streamlit application.

It contains the application interface and recommendation logic used to display movie recommendations.

Run the application using:

```bash
streamlit run app.py
```

---

### `movie-recommender-system.ipynb`

Jupyter Notebook used for building the movie recommendation system.

It contains the data processing and model development steps used to prepare the movie data for recommendation.

---

### `movie_dict.pkl`

A serialized Python object containing processed movie information in dictionary format.

It is used by the application to work with the processed movie data.

---

### `movies.pkl`

A processed version of the movie data used by the Streamlit application.

The data is stored in pickle format so that it can be loaded efficiently by the application.

---

### `similarity.pkl`

Contains the pre-computed similarity information between movies.

The Streamlit application uses this information to find movies similar to the movie selected by the user.

---

### `tmdb_5000_movies.csv`

Movie metadata dataset containing information such as:

- Movie ID
- Title
- Genres
- Keywords
- Overview
- Other movie details

---

### `tmdb_5000_credits.csv`

Contains credits-related information such as:

- Cast
- Crew
- Movie ID
- Movie title

---

### `.gitignore`

Specifies files and folders that should not be tracked by Git.

---

### `.gitattributes`

Contains Git-related configuration.

In this project, it can also contain configuration related to **Git LFS (Large File Storage)** for tracking large files.

---

### `.git/`

The `.git` directory is automatically created when Git is initialized for a local project.

It contains Git's internal repository information.

> This folder is normally not required to be manually modified.

---

### `Procfile`

A deployment configuration file that specifies the command used to start the application on platforms that support Procfile-based deployment.

---

### `requirements.txt`

Contains the Python libraries required to run the project.

For example:

```text
streamlit
pandas
requests
pickle-mixin
```

The exact packages should match the requirements used by the project.

---

### `setup.sh`

A shell script used for deployment configuration.

Its exact requirements depend on the hosting platform and deployment setup.

---

### `README.md`

This file contains information about the project, including:

- Project overview
- Installation instructions
- Project structure
- Recommendation approach
- Dataset information
- Usage instructions

It is documentation for the project and is not part of the recommendation model itself.

---

## 🛠️ Technologies Used

- **Python**
- **Pandas**
- **NumPy**
- **Scikit-learn**
- **Streamlit**
- **Jupyter Notebook**
- **Pickle**
- **TMDB 5000 Movie Dataset**

---

## ⚙️ How to Run the Project Locally

### Step 1: Download the Project

Download or clone this repository.

Using Git:

```bash
git clone https://github.com/laxmankhedkar/Movie-Recommender-System.git
```

Then open the project folder.

---

### Step 2: Install Python

Make sure Python is installed on your system.

Check the installation:

```bash
python --version
```

---

### Step 3: Open the Project

Open the project folder in **Visual Studio Code** or another code editor.

---

### Step 4: Install Required Libraries

Open the terminal inside the project folder and run:

```bash
pip install -r requirements.txt
```

You can also install the main packages individually:

```bash
pip install streamlit
pip install pandas
pip install requests
pip install pickle-mixin
```

---

### Step 5: Run the Streamlit Application

Run:

```bash
streamlit run app.py
```

Streamlit will start a local server and provide a localhost address, usually similar to:

```text
http://localhost:8501
```

Open the address in your browser.

---

## 🖥️ Using the Application

After launching the application:

1. Open the Streamlit application in your browser.
2. Select or search for a movie.
3. Submit the movie selection.
4. The recommendation system finds similar movies.
5. Recommended movies are displayed on the screen.

Example:

```text
Select Movie
     ↓
Iron Man
     ↓
Get Recommendations
     ↓
Similar Movies
```

---

## 📊 Dataset

This project uses the **TMDB 5000 Movie Dataset**.

Dataset:

[TMDB 5000 Movie Dataset – Kaggle](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)

You can also explore other datasets on Kaggle:

[Kaggle Datasets](https://www.kaggle.com/datasets)

---

## 🚀 Live Application

Try the deployed application:

**[Movie Recommender System](https://u-rex13-movie-recommender-system-app-2ap1dd.streamlit.app/)**

The application allows users to select a movie and receive recommendations based on movie similarity.

---

## 🎓 What I Learned From This Project

This project helped me understand and practice:

- Data preprocessing
- Feature selection
- Feature engineering
- Content-based recommendation
- Text-based similarity
- Similarity calculation
- Working with Pandas
- Saving processed data using Pickle
- Building a Streamlit application
- Connecting a machine learning workflow with a web application
- Deploying a Python-based application

---

## 🔮 Future Improvements

Some possible improvements for this project are:

- Add movie posters using the TMDB API
- Improve the recommendation algorithm
- Add more movie features
- Add user ratings and preferences
- Build a hybrid recommendation system
- Improve the Streamlit user interface
- Add filtering by genre, language, or rating
- Add personalized recommendations

---

## 👨‍💻 Author

**Laxman Khedkar**

Data Scientist & ML Engineer | Python | SQL | Machine Learning | NLP | LLMs | RAG | Generative AI

GitHub: [@laxmankhedkar](https://github.com/laxmankhedkar)

---

## ⭐ If You Find This Project Useful

If you find this project useful for learning about **Recommendation Systems, Machine Learning, or Streamlit**, consider giving the repository a ⭐.

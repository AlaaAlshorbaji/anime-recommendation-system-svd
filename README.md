# 🎌 Anime Recommendation System using SVD

This project builds a **Recommendation System** for anime shows using the **Singular Value Decomposition (SVD)** algorithm. The goal is to suggest new anime titles to users based on their past ratings and behavior.

---

## 🎯 Objective

To create a personalized recommendation engine that:
- Learns from user-anime interactions
- Predicts ratings for unseen anime
- Recommends top anime to individual users

---

## 📊 Dataset Description

The dataset contains:
- `user_id`: unique identifier of the user
- `anime_id`: unique identifier of the anime
- `rating`: the score the user gave to the anime
- `name`: title of the anime

The project uses a user-item matrix where rows are users and columns are anime titles, and the cells are ratings.

---

## 🧠 Algorithms & Techniques Used

- **SVD (Singular Value Decomposition)**:  
  A matrix factorization technique to reduce the user-item rating matrix into lower dimensions and uncover latent features of users and anime.
- **Collaborative Filtering**:  
  Recommendations are made based on patterns from similar users or items, without using any content-based features.

---

## 🧰 Libraries Used

- `pandas` – Data loading and manipulation
- `surprise` – Building and training recommendation models (SVD)
- `google.colab` – For file handling in Google Colab

---

## 🔍 Workflow Overview

### 1. 📥 Data Loading
- Used `pandas.read_csv()` to load anime ratings and anime metadata
- Merged datasets to include anime names with user ratings

### 2. 🧹 Data Cleaning
- Removed entries with missing or zero ratings
- Merged datasets on `anime_id` to include anime titles

### 3. 🧪 Preparing Data for Surprise Library
- Created a `Reader` object to define rating scale
- Loaded data into `Dataset` format compatible with Surprise

### 4. 🔄 Train/Test Split
- Split data into training and testing sets using `train_test_split`

### 5. ⚙️ Model Training
- Used `SVD` from `surprise` to build the recommendation model
- Trained on user-anime ratings to learn latent patterns

### 6. 📐 Model Evaluation
- Calculated metrics such as:
  - RMSE (Root Mean Squared Error)
  - MAE (Mean Absolute Error)

### 7. 🤝 Generating Recommendations
- Selected a user ID
- Predicted ratings for anime not rated by this user
- Recommended top-rated anime based on predicted scores

---

## 💡 Sample Output

The model recommends a ranked list of anime that the user hasn’t rated yet but is likely to enjoy, such as:

- Attack on Titan
- One Punch Man
- Death Note  
*(based on learned user preferences)*

---

## 🚀 How to Run

1. Open the notebook `Anime_Recommendation_System.ipynb` in [Google Colab](https://colab.research.google.com/)
2. Run all cells in order.
3. Upload your dataset if prompted.
4. Modify the user ID to get personalized recommendations.

---

## 📌 Future Enhancements

- Add content-based filtering using genres or synopsis
- Use hybrid models combining SVD with metadata
- Add a Streamlit web interface for interactive recommendations
- Implement KNN or deep learning-based recommenders

---

## 👤 Author

**Alaa Shorbaji**  
Artificial Intelligence Instructor – Armed Forces  
Machine Learning & Recommendation Systems Specialist  
GitHub: [your_username]  
LinkedIn: [your_link]

---

## 📜 License

This project is intended for educational purposes. Attribution required if reused or modified.

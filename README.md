📚 Book Recommendation Engine using KNN
This project is a content-based book recommendation system built with Python and the K-Nearest Neighbors (KNN) algorithm. It uses user ratings and book metadata to suggest similar books based on a given title.

📂 Dataset
The project utilizes the Book-Crossing dataset, which includes:

BX-Books.csv: Book metadata (ISBN, title, author)
BX-Book-Ratings.csv: User ratings for books (scale 0–10)

🔍 Steps Performed
1. Data Cleaning & Preprocessing
-Selected relevant columns: ISBN, title, author, user, rating
-Removed missing and duplicate entries
-Optimized memory usage by converting data types

2. Filtering
-To enhance recommendation quality:
-Removed users with fewer than 200 ratings
-Removed books with fewer than 100 ratings

3. Merging Datasets
-Merged book and rating data on ISBN to include book titles and authors

4. Creating the User-Book Matrix
-Built a pivot table with book titles as rows, user IDs as columns, and ratings as values
-Filled missing values with 0

5. KNN Model
-Used sklearn.neighbors.NearestNeighbors with cosine similarity
-Trained the model on the rating matrix
Retrieved the top 5 most similar books for a given title

🚀 How to Run
Clone the Repository:
git clone https://github.com/serayustun/Book-Recommendation-Engine-using-KNN.git

Open the Notebook:
Use Google Colab (recommended) or Jupyter Notebook locally

Load the Dataset:
In Colab: upload dataset files manually when prompted
Locally: place the dataset files in the same directory as the notebook

Run the Notebook:
Execute all cells sequentially
To get book recommendations, run:
get_recommends("Book Title Here")

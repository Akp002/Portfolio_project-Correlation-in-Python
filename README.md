# Movie Recommendation System


## Overview

This project is a movie recommendation system that uses the TF-IDF (Term Frequency-Inverse Document Frequency) vectorizer and cosine similarity to recommend movies based on their plot descriptions. Given the title of a movie, the system provides a list of similar movies based on their plot summaries.

### Table of Contents
* Project Structure
* Installation
* Usage
* Data Sources
* Methodology
* Example
* Contributing
* License
* Acknowledgments

  
## Project Structure
  
movie-recommendation-system/
│

├── data/

│   ├── tmdb_5000_movies.csv

│   ├── tmdb_5000_credits.csv

│

├── notebook/

│   ├── movie_recommendation.ipynb

│

├── README.md

│

└── requirements.txt

* data/: Contains the movie datasets (tmdb_5000_movies.csv, tmdb_5000_credits.csv).
* notebook/: Contains the Jupyter notebook (movie_recommendation.ipynb) where the analysis and model development are done.
* README.md: The documentation file you are currently reading.
* requirements.txt: List of dependencies required to run the project.
  
## Installation
To run this project, you need to have Python installed. Follow the steps below to set up your environment.

* Clone the Repository

git clone https://github.com/Akp002/movie-recommendation-system.git
cd movie-recommendation-system

* Install the Required Libraries
* 
pip install -r requirements.txt
Dependencies
numpy
pandas
scikit-learn
Jupyter (if you want to run the notebook interactively)
All dependencies are listed in the requirements.txt file.


## How to Use the Recommendation System

* Load the datasets (tmdb_5000_movies.csv and tmdb_5000_credits.csv).
* Preprocess the data by filling missing values.
* Use TfidfVectorizer to convert the movie overviews into numerical data.
* Compute cosine similarity between movies.
* Define a function get_recommendations(title) to fetch the top 10 most similar movies based on a given movie title.
* Call the function with any movie title to get recommendations.
  
#### Example

get_recommendations('The Dark Knight Rises')
This will return a list of movies similar to "The Dark Knight Rises."

## Data Sources
The datasets used in this project were obtained from Kaggle:
TMDb 5000 Movie Dataset
Dataset Descriptions:
tmdb_5000_movies.csv: Contains information about 5000 movies, including titles, budget, genres, and overviews.
tmdb_5000_credits.csv: Contains information about the cast and crew of these movies.

## Methodology
* TF-IDF Vectorization
We use the TF-IDF vectorizer to convert the text data (movie overviews) into a matrix of TF-IDF features. 
This helps in transforming the text data into numerical data that can be used to compute similarity scores.

* Cosine Similarity
Cosine similarity is used to measure the similarity between two non-zero vectors. In this project,
 it is used to find similarities between different movies based on their TF-IDF vectors.

## Recommendation Process
* For a given movie, find its TF-IDF vector.
* Calculate the cosine similarity between this vector and all other movie vectors.
* Sort the movies based on similarity scores.
* Return the top N similar movies.
  
#### Example Output
For the movie title "The Dark Knight Rises," the recommendation system may output:

d
1. The Dark Knight
2. Batman Begins
3. Batman
4. Batman Returns
5. Batman Forever
...   

## Contributing
Contributions are welcome! If you find any issues or want to enhance the project, feel free to submit a pull request.

Steps to Contribute:
Fork the repository.
Create a new branch (git checkout -b feature-branch).
Make your changes.
Commit and push (git commit -m "Your commit message" and git push origin feature-branch).
Open a pull request.

## License
This project is licensed under the MIT License 

Acknowledgments
Thanks to Kaggle for providing the datasets.
Inspiration for this project came from various online tutorials and courses on machine learning and natural language processing.

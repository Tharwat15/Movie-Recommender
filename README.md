<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Movie Recommender</title>
</head>
<body>
    <h1>Movie Recommender</h1>

<p>This is a movie recommender system that detects the similarity between movies based on their descriptions. It utilizes TF-IDF (Term Frequency-Inverse Document Frequency) to represent each movie's description as a numerical vector, and then calculates the cosine similarity between these vectors to identify similar movies.</p>

<h2>How it works</h2>

 <ol>
        <li><strong>Data Loading:</strong> The movie dataset (<code>tmdb_5000_movies.csv</code>) is loaded into a Pandas DataFrame.</li>
        <li><strong>Data Preprocessing:</strong> The movie descriptions are cleaned and preprocessed to remove noise and irrelevant information. Null values in the "overview" column are filled with empty strings.</li>
        <li><strong>TF-IDF Vectorization:</strong> Each movie description is transformed into a TF-IDF vector representation using <code>TfidfVectorizer</code> from scikit-learn.</li>
        <li><strong>Cosine Similarity Calculation:</strong> Cosine similarity is computed between the TF-IDF vectors of all pairs of movies using <code>linear_kernel</code> from scikit-learn. This measures the cosine of the angle between the vectors and determines how similar they are.</li>
        <li><strong>Recommendation Generation:</strong> The <code>get_recommendation</code> function takes a movie title as input, finds its index in the DataFrame, and prints movies with a cosine similarity score higher than 0.1 (adjustable) as recommendations.</li>
    </ol>

   <h2>Dataset</h2>
    <p>The movie dataset used in this project (<code>tmdb_5000_movies.csv</code>) can be found at <a href="https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata?select=tmdb_5000_movies.csv">link to dataset</a>.</p>
    <h2>Credits</h2>
    <p>This project was developed by [Your Name]. Feel free to reach out with any questions or feedback!</p>
</body>
</html>

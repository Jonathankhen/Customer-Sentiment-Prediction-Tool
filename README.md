# Customer-Sentiment-Prediction-Tool
This project aims to analyze the sentiment of IMDb movie reviews using Natural Language Processing (NLP) and machine learning techniques. The primary goal is to classify the reviews as positive or negative based on the text content.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <h2>Detailed Description</h2>
    <p>
        This project is a demonstration of Natural Language Processing (NLP) and machine learning techniques applied to sentiment analysis of movie reviews from the IMDB dataset. The goal is to classify each review as positive or negative based on the text content, leveraging various data processing, modeling, and visualization methods.
<h4>Here are some word clouds to show some of the prominent words in the movie reviews:</h4>
<img src="https://github.com/user-attachments/assets/156266b1-43a2-4197-9298-086905160a9a">
<img src="https://github.com/user-attachments/assets/2f2fb065-03cd-47d6-9a64-37e8a7aae87c">
    </p>
    <h3>Key Steps and Features:</h3>
    <ol>
        <li>
            <strong>Data Loading and Initial Exploration:</strong>
            <ul>
                <li><strong>Loading Data:</strong> The project begins with loading the IMDB movie review dataset using pandas. The dataset includes two columns: 'review' (text of the review) and 'sentiment' (label: positive or negative).</li>
                <li><strong>Exploratory Data Analysis (EDA):</strong> Initial exploration involves displaying the first few rows and generating descriptive statistics to understand the data distribution. This includes count, unique entries, top entries, and frequency of the top entries for each column.</li>
            </ul>
        </li>
        <li>
            <strong>Data Cleaning and Preprocessing:</strong>
            <ul>
                <li><strong>HTML Tag Removal:</strong> The BeautifulSoup library is used to strip HTML tags from the text reviews, ensuring that only plain text is analyzed.</li>
                <li><strong>Square Brackets Removal:</strong> A regular expression is applied to remove any text within square brackets.</li>
                <li><strong>Special Characters Removal:</strong> Another regular expression cleanses the text of any special characters, leaving only alphanumeric characters.</li>
                <li><strong>Binary Label Conversion:</strong> Sentiment labels are converted to binary values (0 for negative and 1 for positive) using LabelBinarizer from sklearn.</li>
            </ul>
        </li>
        <li>
            <strong>Text Vectorization:</strong>
            <ul>
                <li><strong>TF-IDF Vectorization:</strong> The text data is transformed into numerical features using the TF-IDF (Term Frequency-Inverse Document Frequency) vectorizer. This method converts the text into a matrix of TF-IDF features, which represent the importance of words in the reviews. Parameters like <code>min_df</code>, <code>max_df</code>, and <code>ngram_range</code> are tuned to improve the model’s performance.</li>
            </ul>
        </li>
        <li>
            <strong>Model Training and Evaluation:</strong>
            <ul>
                <li><strong>Model Selection:</strong> Logistic Regression is chosen for its simplicity and efficiency in binary classification tasks. The model is trained on the vectorized training data.</li>
                <li><strong>Performance Evaluation:</strong> The model’s performance is evaluated using metrics such as confusion matrix, accuracy score, and detailed classification report (precision, recall, F1-score, support). These metrics provide insights into the model's effectiveness in classifying sentiments correctly.</li>
            </ul>
        </li>
        <li>
            <strong>Feature Importance Analysis:</strong>
            <ul>
                <li><strong>Word Impact Analysis:</strong> The logistic regression model’s coefficients are analyzed to identify the words with the highest positive and negative impact on sentiment. This helps in understanding which words are most indicative of positive or negative reviews.</li>
                <li><strong>Word Cloud Generation:</strong> Word clouds are generated for the most influential positive and negative words, providing a visual representation of key terms.</li>
            </ul>
        </li>
        <li>
            <strong>Data Visualization:</strong>
            <ul>
                <li><strong>Review Length Distribution:</strong> Interactive histograms are created using Plotly to visualize the distribution of review lengths, showing how the length varies across different sentiments.</li>
                <li><strong>Box Plot of Review Lengths:</strong> Box plots illustrate the distribution of review lengths by sentiment category, highlighting differences between positive and negative reviews.</li>
                <li><strong>Top Words Impact Scatter Plot:</strong> An interactive scatter plot visualizes the top 50 words influencing sentiment, with point size and color indicating the magnitude of their coefficients.</li>
<img src="https://github.com/user-attachments/assets/824cd1e3-7d6a-4629-96f8-466671abab79">
<img src="https://github.com/user-attachments/assets/dc987d5d-9a65-46df-a994-de5c61f8f9b8">
<img src="https://github.com/user-attachments/assets/88bc9b30-95ac-48aa-8532-5ae4eb65be13">
            </ul>
        </li>
        <li>
            <strong>Sentiment Prediction Function:</strong>
            <ul>
                <li><strong>User Input Prediction:</strong> A function allows users to input their own movie reviews and receive sentiment predictions. The text is cleaned, vectorized, and classified using the trained logistic regression model, providing a binary sentiment output.</li>
            </ul>
        </li>
    </ol>
    <h3>Installation and Usage:</h3>
    <ol>
        <li>
            <strong>Clone the Repository:</strong>
            <pre><code>git clone https://github.com/Jonathankhen/Customer-Sentiment-Prediction-Tool.git
cd Customer-Sentiment-Prediction-Tool</code></pre>
        </li>
        <li>
            <strong>Install Dependencies:</strong>
            <pre><code>pip install numpy pandas beautifulsoup4 scikit-learn matplotlib wordcloud plotly</code></pre>
        </li>
        <li>
            <strong>Predict Review Sentiment:</strong>
            <p>Input a review when prompted:</p>
            <pre><code>Enter a review to analyze its sentiment: That movie wasn't good
The predicted sentiment of the review is: Negative</code></pre>
<img src="https://github.com/user-attachments/assets/0e1d1af4-d5e1-4a50-b556-75e18eeeba25">
        </li>
    </ol>
    <h3>Conclusion:</h3>
    <p>
        This project showcases a full pipeline for sentiment analysis of text data, from data cleaning and preprocessing to model training and evaluation, concluding with interactive visualizations and a user-friendly prediction function. It serves as a valuable example of applying NLP and machine learning to real-world data for actionable insights. Contributions and improvements to the project are welcome to enhance its functionality and accuracy further.
    </p>
</body>
</html>

# TwitterSentimentAnalysis
1. Importing necessary libraries:
   - `pandas` and `numpy` are libraries for data manipulation and analysis.
   - `CountVectorizer` is used for converting text data into numerical features.
   - `train_test_split` is used to split the data into training and testing sets.
   - `DecisionTreeClassifier` is a machine learning algorithm for classification.
   - `re` is a library for working with regular expressions.
   - `nltk` is the Natural Language Toolkit library for text processing.
   - `matplotlib` is a plotting library for creating visualizations.

2. Reading the data:
   - The code reads a CSV file called "twitter.csv" using `pd.read_csv` and stores it in the variable `data`.
   - The `print(data.head())` statement displays the first few rows of the data to check its contents.

3. Text preprocessing:
   - The code defines a function called `clean` to clean and preprocess the text data.
   - The function performs various operations like converting text to lowercase, removing URLs, removing punctuation, removing stopwords (common words like "the," "is," etc.), and stemming (reducing words to their base form).
   - The `data["tweet"].apply(clean)` line applies the `clean` function to each tweet in the "tweet" column of the data.

4. Sentiment analysis:
   - The code uses the VADER (Valence Aware Dictionary and sEntiment Reasoner) sentiment analysis tool from NLTK.
   - It calculates the positive, negative, and neutral sentiment scores for each cleaned tweet using the `SentimentIntensityAnalyzer` class.
   - The scores are added as new columns ("Positive," "Negative," "Neutral") to the `data` DataFrame.

5. Summing up sentiment scores:
   - The code sums up the positive, negative, and neutral sentiment scores using the `sum` function and stores them in variables `x`, `y`, and `z`, respectively.

6. Determining overall sentiment:
   - The code defines a function called `sentiment_score` to determine the overall sentiment based on the sum of positive, negative, and neutral scores.
   - It compares the scores and prints a corresponding sentiment label ("Positive," "Negative," or "Neutral").

7. Displaying sentiment scores:
   - The code prints the values of `x`, `y`, and `z`, which represent the total positive, negative, and neutral sentiment scores, respectively.

8. Creating a pie chart:
   - The code creates a pie chart using the `plt.pie` function from the `matplotlib.pyplot` module.
   - The chart displays the proportions of positive, negative, and neutral sentiments using the `sizes` list.
   - The `labels` list provides labels for each sentiment category.
   - The `colors` list specifies colors for each category.
   - The `explode` tuple is used to offset the largest slice of the pie for emphasis.

9. Styling the pie chart:
   - The code adds additional styling options to the pie chart.
   - The `shadow=True` parameter adds a shadow effect to the chart.
   - The `wedgeprops={'edgecolor': 'black'}` parameter adds black edges to each wedge of the chart.

10. Adding title and legend:
    - The code adds a title to the pie chart using the `ax.set_title` function.
    - The `ax.legend` function adds a legend to the chart, providing labels for each sentiment category.
11. Setting aspect ratio and displaying the chart:

    - The code sets the aspect ratio of the pie chart to make it circular using ax.axis('equal').
    - Finally, the plt.show() function displays the chart on the screen.




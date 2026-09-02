# Mandatory Assignment 2: Machine Learning

#### **You <u>must</u> work in groups of 2-4.**
You have 14 days to work on a machine-learning algorithm.
Pick one of the following use cases and make a prediction algorithm using either regression or classification algorithms.

Do the following:
1. Pick one use case (defined below).
2. Explore and research which algorithm would work best for this use case (regression or classification)
3. Document your findings in a markdown cell (3-5 lines) on why you chose this algorithm.
4. Train the algorithm using Python
5. Keep the solution as simple as possible. We are not looking for the best machine-learning algorithm. We are interested in seeing that you know how to work with machine learning.
6. Turn in a **JUPYTER NOTEBOOK** on canvas.


You can pick one of the following use cases:

### 1. Predict stock market price for GameStop.

https://www.kaggle.com/datasets/hananxx/gamestop-historical-stock-prices
Make a prediction algorithm which predicts the price of this stock on a specific date. Input will be date and output should be price of that stock (close value in the data file).
You should also show the prediction percentage score.
Data file: GME_stock.csv

### 2. Predict passenger data for Ruter. 

Use Ruter-data.csv dataset (in data folder). I want you to make a prediction algorithm which predicts the number of passengers on a specific date for a specific bus (pick any one). Input should be date and output will be number of passengers You should also show the prediction percentage score. 
Data file: Ruter_data.csv

### 3. Bysykkel Station Popularity Classification

https://oslobysykkel.no/apne-data/historisk
Using the Oslo Bysykkel dataset, create a algorithm that predicts whether a bike station is **High**, **Medium**, or **Low** popularity based on usage patterns.
Task Details:
Example input features: Station location, total trips started from station, total trips ended at station, average trip duration, day of week patterns
Example output: Popularity category (High/Medium/Low usage)
Data file: `Bysykkel_09.csv` (September 2025 data with about 138,000 trip records)

Suggested steps:
Data processing: Group trips by stations and calculate total metrics for each station (feel free to use a small subset of the stations to simplify the processing if needed). Create features like total_trips_started, total_trips_ended, avg_duration and station id.
Create a target variable: Calculate total station usage (trips ended + trips started). Classify stations into 3 categories based on usage. High: top 33%, medium middle 33% and low: bottom 33%.

Train the model using these features or others to predict popularity category.

Show accuracy scores and confusion matrix.


### 4. Find your own dataset online, for example on: https://www.kaggle.com/datasets

Make a prediction algorithm using regression or classification. You should also show the prediction accuracy score and confusion matrix.

**IMPORTANT, you must  upload the dataset in your submission if you choose to pick your own dataset.**

Remember, we are **not** looking for a 30-page submission. Do not make it too complicated. 
<u>Keep it simple and to the point.</u>

Feel free to ask us for help in the labs if you are stuck or need help.

# Restaurant-Recommendation System
Objective: Create a restaurant recommendation system based on user preferences.

## Project Overview

This project implements a content-based restaurant recommendation system using data from a CSV file. The system considers user preferences such as cuisine, price range, and minimum rating to provide personalized recommendations.

## Features

- **Data Preprocessing:** Handles missing values and encodes categorical variables (one-hot encoding).
- **Content-Based Filtering:** Recommends restaurants similar to user preferences based on cuisine, price, and rating.
- **Recommendation Function:** Provides a function to generate recommendations based on user input.
- **Recommendation Evaluation:** Includes test cases with sample user preferences to evaluate recommendation quality.
- **Visualization:** Uses bar plots to visualize the similarity scores of recommended restaurants and their corresponding attributes.


## How to Use

1. **Install Dependencies:** Make sure you have the necessary libraries installed: pandas, scikit-learn, and matplotlib. You can install them using `pip install pandas scikit-learn matplotlib`.
2. **Upload Dataset:** Use the `google.colab` library to upload the restaurant data CSV file.
3. **Run Code:** Execute the provided code in a Google Colab notebook.
4. **Provide Preferences:** Input your desired preferences for cuisine, price range, and minimum rating using the `content_based_recommendation` function.
5. **View Recommendations:** The system will output the top recommended restaurants along with their similarity scores.

## Example Usage

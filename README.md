# Restaurant-Recommendation System
Objective: Create a restaurant recommendation system based on user preferences.

## Overview

This project implements a content-based restaurant recommendation system using data from kaggle. The system suggests restaurants based on user preferences, such as cuisine, price range, and minimum rating.

## Dataset

The dataset used for this project is the `kaggle.csv` file, containing information about various restaurants, including their name, location, cuisine, price range, ratings, and more. This dataset can be uploaded to your Colab environment for using with this project.

## Methodology

1. **Data Preprocessing**:
    - Handling missing values in the dataset (e.g., filling missing cuisines with "Not Specified").
    - Encoding categorical variables:
        - Binary columns like 'Has Table booking', 'Has Online delivery', 'Is delivering now' are encoded as 0 and 1.
        - Multi-category columns like 'City', 'Cuisines', and 'Rating text' are one-hot encoded.

2. **Recommendation Criteria**:
    - The system allows users to specify their preferences based on the following criteria:
        - `cuisine`: Preferred type of cuisine (e.g., Italian, Chinese).
        - `max_price`: Maximum price range for two people.
        - `min_rating`: Minimum aggregate rating of the restaurant.
        - `city`: City where the user is looking for recommendations.
        - `table_booking`: Whether table booking is required.
        - `online_delivery`: Whether online delivery is preferred.
        - `delivering_now`: Whether the restaurant should be delivering now.

3. **Content-Based Filtering**:
    - The core of the recommendation system is a content-based filtering approach.
    - It calculates the similarity between user preferences and restaurant features using cosine similarity.
    - Restaurants with higher similarity scores are recommended to the user.

## Usage

1. **Upload the `zomato.csv` dataset to your Colab environment.**
2. **Run the code cells to preprocess the data and define the recommendation functions.**
3. **Call the `content_based_recommendation` function with your desired preferences.**
4. **The function returns a Pandas DataFrame with the top-recommended restaurants.**

**Example Usage:**

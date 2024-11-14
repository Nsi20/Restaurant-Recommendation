# Restaurant-Recommendation System
Objective: Create a restaurant recommendation system based on user preferences.

---

This project implements a content-based recommendation system that suggests restaurants based on user-defined criteria, such as preferred cuisine, price range, and minimum rating. The goal is to provide relevant restaurant recommendations that align with user preferences by analyzing the dataset and filtering options using similarity metrics.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Dataset](#dataset)
3. [Project Structure](#project-structure)
4. [Methodology](#methodology)
5. [Installation and Setup](#installation-and-setup)
6. [Usage](#usage)
7. [Evaluation](#evaluation)
8. [Future Improvements](#future-improvements)
9. [License](#license)

## Project Overview
In this project, I implemented a recommendation system that helps users discover restaurants based on their preferences. By using a content-based filtering approach, the system considers individual restaurant features such as cuisine, cost, and user ratings. The recommendation algorithm identifies restaurants with similar characteristics to those specified by the user, allowing for personalized and relevant suggestions.

## Dataset
The dataset used in this project contains various details about restaurants, including:
- **Restaurant ID**: Unique identifier for each restaurant.
- **Restaurant Name**: Name of the restaurant.
- **Country Code, City, and Address**: Geolocation details.
- **Cuisines**: Types of cuisine offered by each restaurant.
- **Average Cost for Two**: Cost estimate for two people dining.
- **Currency**: Currency used for restaurant pricing.
- **Booking Options**: Availability of table booking and online delivery.
- **Aggregate Rating**: Overall rating based on user votes.
- **Rating Color and Text**: Categorical representation of the rating.
- **Votes**: Number of user ratings for each restaurant.

I applied one-hot encoding to categorical variables, including cuisines and ratings, to enable more nuanced filtering based on user preferences.

## Project Structure
The project is organized as follows:
- **Data Preprocessing**: Handled missing values and performed one-hot encoding on categorical variables to make the dataset suitable for similarity calculations.
- **Recommendation System Implementation**: Built a content-based filtering system that takes user preferences and finds the most similar restaurants based on cosine similarity.
- **Evaluation**: Tested the recommendation system with different user preferences to ensure the quality and relevance of recommendations.
- **Visualization**: Used Matplotlib to display recommended restaurants and their similarity scores visually.

## Methodology
### 1. Data Preprocessing
   - **Handling Missing Values**: Filled any missing entries in the dataset, especially in critical columns like cuisine, to avoid errors during processing.
   - **Encoding Categorical Variables**: Applied one-hot encoding to the **Cuisines** and **Rating Text** columns to enable better similarity matching based on user preferences.

### 2. Content-Based Filtering
   - **Feature Vector Creation**: Constructed a feature vector for each restaurant based on encoded features, average cost, and aggregate rating.
   - **User Preference Vector**: Created a vector representing the user’s preferences, including preferred cuisine, maximum price, and minimum rating.
   - **Similarity Calculation**: Used cosine similarity to calculate the similarity between the user preference vector and each restaurant’s feature vector. Restaurants with higher similarity scores are recommended first.

### 3. Evaluation and Visualization
   - **Testing**: Ran multiple test cases with different user preferences and reviewed the quality of recommendations to ensure the system’s relevance.
   - **Visualization**: Generated bar charts to show the similarity scores of recommended restaurants, along with their average cost and ratings, for an easily interpretable overview of recommendations.

## Installation and Setup
### Requirements
- **Python 3.x**
- **Libraries**:
  - pandas
  - numpy
  - scikit-learn
  - matplotlib

To install the required libraries, run:
```bash
pip install pandas numpy scikit-learn matplotlib
```

### Running the Project
1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/restaurant-recommendation-system.git
   cd restaurant-recommendation-system
   ```

2. **Load the Dataset**: Place the dataset (e.g., `dataset.csv`) in the project directory or specify its path in the code.

3. **Run the Code**: Execute the Python script or notebook to preprocess the data, run the recommendation system, and visualize the results.

## Usage
### Sample Code
To use the recommendation system, you can specify the following parameters:
- **preferred_cuisine**: Cuisine type preferred by the user (e.g., "Italian").
- **max_price**: Maximum budget for two people.
- **min_rating**: Minimum aggregate rating.
- **top_n**: Number of recommendations to return.

Here’s an example code snippet:

```python
# Run the recommendation system with user-defined preferences
recommendations = content_based_recommendation(
    df,
    preferred_cuisine="Italian",
    max_price=500,
    min_rating=4.0,
    top_n=5
)

# Display the recommendations
print(recommendations)
```

### Visualization
After generating recommendations, visualize them with similarity scores, average cost, and ratings using Matplotlib:

```python
plot_recommendations(recommendations, test_case_num=1)
```

This produces a bar chart where each recommended restaurant's similarity score is shown, with labels for cost and rating.

## Evaluation
The recommendation system was tested with different user preferences to ensure the quality of recommendations. For each test case:
- **Cuisine Match**: Confirmed that the recommended restaurants matched the user’s specified cuisine.
- **Cost and Rating Compliance**: Verified that the prices and ratings of the recommendations fell within the specified ranges.
- **Similarity Scores**: Reviewed similarity scores to ensure recommendations were close matches to user preferences.

## Future Improvements
Some ideas for enhancing this system include:
1. **Adding Collaborative Filtering**: Incorporate collaborative filtering to recommend popular or highly-rated restaurants among similar users.
2. **Location-Based Filtering**: Integrate location-based recommendations using city or locality details to prioritize nearby restaurants.
3. **Enhanced Visualization**: Create more interactive visualizations (e.g., maps) to show recommendations relative to user location.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

# Twitter Human vs Bot Classification Project

This project involves the analysis and classification of Twitter accounts into two categories: **human** and **bot**. Using a variety of features, including account activity, follower counts, and profile settings, the goal is to distinguish between human-operated and automated (bot) accounts.

## Dataset

The dataset used in this project is a collection of Twitter account profiles, consisting of both human and bot accounts. The dataset includes the following columns:

- `created_at`: Account creation timestamp.
- `default_profile`: Whether the account has the default Twitter profile.
- `default_profile_image`: Whether the account uses the default Twitter profile image.
- `description`: Profile description of the user.
- `favourites_count`: Number of tweets liked by the user.
- `followers_count`: Number of followers the account has.
- `friends_count`: Number of accounts the user follows.
- `geo_enabled`: Whether the user has geolocation enabled.
- `id`: Unique identifier of the Twitter account.
- `lang`: Language of the account.
- `location`: Geographical location of the user.
- `profile_background_image_url`: URL of the profile background image.
- `profile_image_url`: URL of the profile image.
- `screen_name`: Username of the account.
- `statuses_count`: Number of tweets posted by the user.
- `verified`: Whether the account is verified by Twitter.
- `average_tweets_per_day`: Average number of tweets posted per day.
- `account_age_days`: Age of the account in days.
- `account_type`: The label of the account, either "human" or "bot".

## Project Goals

- **Preprocessing the Data**: Convert boolean columns to integer values for better machine learning model compatibility.
- **Feature Engineering**: Create new features, such as a "popularity" metric, which takes into account followers and friends count, to assess the account's influence.
- **Exploratory Data Analysis (EDA)**: Analyze the distribution of key features and compare human vs. bot accounts using visualizations.
- **Classification**: Build models that can accurately classify an account as human or bot based on various features.

## Preprocessing and Feature Engineering

### Converting Boolean Columns
The project first converts boolean columns into integers (`0` for False and `1` for True). The relevant boolean columns include:

- `default_profile`
- `default_profile_image`
- `geo_enabled`
- `verified`

### Popularity Metric
A custom "popularity" metric is introduced to quantify the influence of each account. This metric is calculated as the logarithm of the number of followers and friends.

## Exploratory Data Analysis (EDA)

The EDA includes several key tasks:

1. **Histograms**: Display distributions of the "popularity" metric for human and bot accounts.
2. **Box Plots**: Visualize the spread of the "popularity" metric across human and bot accounts.

### Key Visualizations

- **Histograms**: These show the distribution of the "popularity" metric, which is calculated based on the number of followers and friends. This allows for a comparison of the activity levels between human and bot accounts.
  
- **Boxplots**: Provide a more granular view of how popularity varies within each group (human or bot), including metrics like the mean and standard deviation.

## Dependencies

The following Python libraries are used in this project:

- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`

These libraries are used for data manipulation, visualization, and statistical analysis.

## Getting Started

To run this project:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/twitter_bot_detection/twitter-human-bot-classification.git
   cd twitter-human-bot-classification
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Jupyter notebook or Python script**:
   - If you prefer Jupyter Notebook:
     ```bash
     jupyter notebook
     ```
   - Or run the Python script directly:
     ```bash
     python classify_accounts.py
     ```



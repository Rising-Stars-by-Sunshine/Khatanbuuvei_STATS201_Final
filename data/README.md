# README.md - Data Folder

## Dataset Description
This project utilizes the **Netflix vs Disney** dataset, which provides insights into the subscriber growth, content offerings, and pricing strategies of Netflix and Disney+ from 2018 to 2024. The dataset aims to help analyze the relationship between content strategies (such as original programming, genre diversity, and franchise presence) and subscriber behavior across different demographic groups (age, region, income). The data is sourced from Kaggle, and it includes key variables related to pricing strategies, content offerings, and subscriber growth patterns for both platforms. The dataset serves as a foundation for investigating the influence of content and pricing on user engagement and retention.

**Origin of the data**: 
The dataset was curated by Pratham Jyotsingh and is available through Kaggle, a platform for open datasets and data science competitions.

## Data Dictionary

| **Variable**         | **Type**   | **Description**                                                                                                                                 |
|----------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `Date`               | Date      | The date when the data was recorded.                                                                                                              |
| `Platform`           | Categorical| The streaming platform (Netflix or Disney+) for which the data is recorded.                                                                      |
| `Country`            | Categorical| The country where the data point is recorded, indicating the regional aspect of the subscriber's behavior.                                       |
| `Price`              | Numeric   | The subscription price for the platform on the given date.                                                                                       |
| `Subscribers`        | Numeric   | The total number of subscribers for the respective platform on the given date.                                                                  |
| `Revenue`            | Numeric   | The total revenue generated from subscriptions for the respective platform on the given date.                                                    |
| `Content_Type`       | Categorical| The type of content offered by the platform (e.g., original programming, licensed content).                                                      |
| `Genre`              | Categorical| The genre(s) of the content available on the platform (e.g., drama, action, comedy).                                                             |
| `Franchise`          | Categorical| Indicates whether the content is part of a larger franchise (e.g., Marvel, Star Wars for Disney).                                                 |
| `Demographics_Age`   | Categorical| Age group of the subscribers (e.g., 18-24, 25-34, etc.).                                                                                         |
| `Demographics_Income`| Categorical| Income group of the subscribers (e.g., Low, Medium, High).                                                                                       |
| `Region`             | Categorical| The specific region or continent where the data is observed (e.g., North America, Europe, Asia).                                                 |

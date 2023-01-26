# Analysis with Hive

## Data
This project utilizes a dataset containing classified records of used cars from various Eastern European countries spanning multiple years. The dataset, consisting of approximately 3.5 million rows and 16 columns, required cleaning and processing to provide data-driven insights for stakeholders interested in investing in the used car industry.

Source: https://www.kaggle.com/datasets/mirosval/personal-cars-classifieds

## Tools used
Due to the size of the dataset, I utilized **Hadoop** and **Apache Hive** to write queries on the Google Cloud Platform.

## Tasks
After creating the table in the GCP terminal, I cleaned the dataset in a number of ways:
- Dropped columns with more than 50% null records
* Set the *manufacture year* to a range between 2000 and 2017
+ Ensured the *model* and *maker* columns had no null records
- Implemented a *price* range between 3000 and 2000000
* Dropped any single *price* which was repeated multiple times across the ads.

Afterward, I determined the top cars in the terms of highest average *price* and lowest average *price*. Furthermore, I created three segment of customers, viz.,
- **Economic segment**: This represents customers willing to spend 3000 to 20,000 on a car.
+ **Intermediate segment**: This represents customers willing to spend 20,000 to 300,000 on a car.
* **Luxury segment**: This category of customers are open to spending 300,000 to 2,000,000 on a car.


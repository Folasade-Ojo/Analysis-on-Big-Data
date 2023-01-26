# Used Cars Business

## Dataset
This project utilizes a dataset containing classified records of used cars from various Eastern European countries spanning multiple years. The dataset, consisting of approximately 3.5 million rows and 16 columns, required cleaning and processing to provide data-driven insights for stakeholders interested in investing in the used car industry.

Source: https://www.kaggle.com/datasets/mirosval/personal-cars-classifieds

## Tools used
To handle the large dataset, I utilized Hadoop and Apache Hive to perform querying on Google Cloud Platform (GCP)

## Tasks
After creating the table in GCP terminal, the dataset was cleaned using several methods, including:
- Dropped columns with more than 50% null records.
* Set the *manufacture year* to a range between 2000 and 2017.
+ Ensured the *model* and *maker* columns had no null records.
- Implemented a *price* range between 3000 and 2,000,000 euros.
* Dropped any single *price* which was repeated multiple times across the ads.

Subsequently, I determined the top cars in terms of highest and lowest average price. Additionally, I segmented the customer base into three groups:
- **Economic segment**: This represents customers willing to spend 3000 to 20,000 on a car.
+ **Intermediate segment**: This represents customers willing to spend 20,000 to 300,000 on a car.
* **Luxury segment**: This customer segment is willing to invest between 300,000 and 2,000,000 on a car.


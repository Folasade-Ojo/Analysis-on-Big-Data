# Used Cars Business

## Dataset
This project focuses on an analysis on a dataset containing classified records of used cars from various Eastern European countries spanning multiple years. The dataset, consisting of approximately 3.5 million rows and 16 columns, required cleaning and processing to answer some questions stakeholders interested in investing in the used car industry might want to know.

Source: https://www.kaggle.com/datasets/mirosval/personal-cars-classifieds

## Tools
To handle the large dataset, I utilized **Hadoop** and **Apache Hive** to perform querying on **Google Cloud Platform (GCP)**.

## Exploration and Cleaning 

**Table creation in GCP**

![image](https://user-images.githubusercontent.com/121362860/226034424-b4fd0b26-7c3c-4301-8918-187dc78724fd.png)

**Missing Values**

*Color Slug* and *Fuel Type* had more than 50% null records.

![image](https://user-images.githubusercontent.com/121362860/226034274-ea2750db-d2a7-41c0-8d31-55dc5ca3fed3.png)

**Single Price Occurence**

The price of '1295.34' was found 673,623 times, which is significantly higher than the maximum number of times that any other price was repeated (6609). This suggests that there may have been an error during the scraping process specifically related to the price of 1295.34 euros.

![image](https://user-images.githubusercontent.com/121362860/226035962-0c3cf009-3235-4b28-9107-a0833c78df10.png)

**Clean Table**

This was achieved by
- Dropping columns with more than 50% null records (*color slug* and *fuel type*).
* Setting the *manufacture year* to a range between 2000 and 2017.
+ Ensuring the *model* and *maker* columns had no null records.
- Implementing a *price* range between 3000 and 2,000,000 euros.
* Dropping any single *price* which was repeated multiple times across the ads (1295.34).

![image](https://user-images.githubusercontent.com/121362860/226039277-9656a8b6-44c0-4c57-9688-d66313168af7.png)

## Business Questions
**TOP 10 CAR MAKERS AND MODELS BY AVERAGE PRICE**

![image](https://user-images.githubusercontent.com/121362860/226040981-9a8057bb-99d9-40b8-9592-5905f0f0efa1.png)

**TOP 10 CHEAPEST CAR MODELS**

![image](https://user-images.githubusercontent.com/121362860/226041582-1fcee8ac-2155-43b1-b9b0-592ba8e28011.png)

**TOP 5 CARS IN EACH CUSTOMER SEGMENT**

This will be done by segmenting the customer base into three groups:

***Economic Segment***

*This represents customers willing to spend 3000 to 20,000 on a car.*

![image](https://user-images.githubusercontent.com/121362860/226042711-0ba086ec-1b80-475a-a537-26349728cacb.png)

***Intermediate Segment***

*This represents customers willing to spend 20,000 to 300,000 on a car.*

![image](https://user-images.githubusercontent.com/121362860/226043708-2d8f05b2-2c93-47e3-b8a6-974792f1fa6f.png)

***Luxury Segment***

*This customer segment is willing to invest between 300,000 and 2,000,000 on a car.*

![image](https://user-images.githubusercontent.com/121362860/226043835-03f685f7-c170-4eb4-bc97-53b1675a1516.png)



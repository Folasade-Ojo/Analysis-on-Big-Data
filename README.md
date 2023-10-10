# Used Cars Business

The used car business is highly competitive as there are ways to make a lot of money with low capital. Selling secondhand cars has proven to be more lucrative than selling new ones. According to National Automobile Dealerships Association, the average gross profit of a new car is $1,200, whereas that of a used car is $2,000. This line of work necessitates expertise in dealing with both people and cars.

## Dataset
This project focuses on an analysis on a dataset containing classified records of used cars from various Eastern European countries spanning multiple years. The dataset, consisting of approximately 3.5 million rows and 16 columns, required cleaning and processing to answer some questions stakeholders interested in investing in the used car industry might want to know.

Source: https://www.kaggle.com/datasets/mirosval/personal-cars-classifieds

## Tools
To handle the large dataset, I utilized **Hadoop** and **Apache Hive** to perform querying on **Google Cloud Platform (GCP)**.

## Exploration and Cleaning 

**Table creation in GCP**

![image](https://user-images.githubusercontent.com/121362860/226034424-b4fd0b26-7c3c-4301-8918-187dc78724fd.png)

**Missing Values**

![image](https://user-images.githubusercontent.com/121362860/226034274-ea2750db-d2a7-41c0-8d31-55dc5ca3fed3.png)

*Color Slug* and *Fuel Type* had more than 50% null records.

**Duplicates**

*Checking for multiple price occurence*

![image](https://user-images.githubusercontent.com/121362860/226035962-0c3cf009-3235-4b28-9107-a0833c78df10.png)

*The price of '1295.34' was found 673,623 times, which is significantly higher than the maximum number of times that any other price was repeated (6609). This suggests that there may have been an error during the scraping process specifically related to the price of 1295.34 euros.*

**Data Cleaning**

This was achieved by creating a new table by implementing the following
- Dropping columns with more than 50% null records (*color slug* and *fuel type*).
* Setting the *manufacture year* to a range between 2000 and 2017.
+ Ensuring the *model* and *maker* columns had no null records.
- Implementing a *price* range between 3000 and 2,000,000 euros.
* Dropping any single *price* which was repeated multiple times across the ads (1295.34).

![image](https://user-images.githubusercontent.com/121362860/226039277-9656a8b6-44c0-4c57-9688-d66313168af7.png)

## Business Questions

To obtain a bird’s eye view of the entire dataset, the top cars based on average price and cars with the least average price were identified. Lamborghini, Porsche, BMW, and Tesla were the top carmakers among the cars manufactured within the 17-year period, with Aventador, Carrera-gt, and z8 being the top 3 models in terms of average price. On the other hand, Kia Retona, Rover Streetwise, and Skoda Galaxy had the least average sales price. 

**TOP 10 CAR MAKERS AND MODELS BY AVERAGE PRICE**

![image](https://user-images.githubusercontent.com/121362860/226040981-9a8057bb-99d9-40b8-9592-5905f0f0efa1.png)

![image](https://github.com/Folasade-Ojo/Used-Cars-Business/assets/121362860/6738436f-0006-4d18-b72f-f4212ad45190)

**TOP 10 CHEAPEST CAR MODELS**

![image](https://user-images.githubusercontent.com/121362860/226041582-1fcee8ac-2155-43b1-b9b0-592ba8e28011.png)

![image](https://github.com/Folasade-Ojo/Used-Cars-Business/assets/121362860/38325b9e-922d-4633-81f3-704baaec158a)

**TOP 5 MANUFACTURERS IN EACH CUSTOMER SEGMENT**

One of the key factors to consider is the top manufacturer in each customer segment. 

***Economic Segment***

Cars ranging from 3000€ to 19999€ are typically purchased by customers in the economic segment. The top car manufacturer in this segment in terms of average price is the Volvo v40. The least-performing manufacturer in this segment is the Skoda Galaxy.

![image](https://user-images.githubusercontent.com/121362860/226042711-0ba086ec-1b80-475a-a537-26349728cacb.png)

***Intermediate Segment***

For customers in the intermediate category, cars within the price range of 20,000€ and 300,000€ were analyzed. From the information gathered, the BMW z8 has had the highest average sales over the years at proximately 245000€. 

![image](https://user-images.githubusercontent.com/121362860/226043708-2d8f05b2-2c93-47e3-b8a6-974792f1fa6f.png)

***Luxury Segment***

Finally, Lamborghini Aventador and Porsche Carrera-gt are the only cars in the luxury segment (300,000€-2,000,000€). They are sold at an average price of approximately 366000€ and 302000€ respectively.

![image](https://user-images.githubusercontent.com/121362860/226043835-03f685f7-c170-4eb4-bc97-53b1675a1516.png)



![image](https://github.com/Folasade-Ojo/Used-Cars-Business/assets/121362860/1642e5e0-c52e-4bc7-9898-155c10d21b42)

**TOTAL AMOUNT REALISED IN EACH CATEGORY**

Further findings showed that the higher the average price, the fewer the number of buyers. Consequently, more customers purchased cars in the economic segment which translated to more sales in that segment. On the other hand, the cars in the luxury segment were the least purchased cars. This reflects the state of the economy in general. 

![image](https://github.com/Folasade-Ojo/Used-Cars-Business/assets/121362860/2a3128de-4476-42b8-afab-1502bf618e34)


## Recommendation

Due to inflation, the purchasing power of consumers tends to drop, and they typically buy based on their needs. *The top 1%*, however, can afford luxury goods more often than others. However, to maximize profit, working with some of the high-achieving manufacturers will attribute to more profitability for the firm. From the result gathered, investing heavily in the **Economic segment**, and not as much in the Intermediate or Luxury segment will yield more profit for the firm in the long run.

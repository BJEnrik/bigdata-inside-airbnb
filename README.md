![cover_photo.png](resources/cover_photo.png)

# <center> Understanding Supply, Demand, and Pricing Dynamics </center>

***
<h1 style="color: #FF5A60"><b>I. Executive Summary</b></h1>

In the recent years, the rental economy [1] experienced a significant transformation influenced by dynamic factors like the COVID-19 pandemic, evolving travel patterns and customer preference, and shifting economic conditions. Understanding the trends of this ever-changing market is crucial for stakeholders in the short- and long-term rental market [2]. Through a comprehensive analysis of the `Inside Airbnb` data, this project aims to uncover valuable insights into trends on pricing, availability, and demand. By delving into these key factors, the project seeks to enable travelers, hosts, and other industry stakeholders with the necessary information to make informed decisions.

The project consists of three phases: data preprocessing, data transformation, and Exploratory Data Analysis (EDA). The data preprocessing phase address various data quality issues, including handling malformed files, correcting data types, and reformatting the dataset to ensure reliability for analysis. Parquet files were utilized for more efficient processing given its columnar storage format. In the data transformation phase, data was aggregated and transformed to generate the necessary statistics for analysis. Finally, the EDA focused on analyzing global trends and conducting cross-country comparisons on pricing, availability, and demand of listings in Airbnb.

Results show insightful temporal trends affected by the COVID-19 pandemic and travel restrictions. Following the pandemic, a gradual recovery is observed, characterized by price increases and improved availability. Country-specific analysis highlights variations in pricing and popularity. The United States emerges as a high-demand market with correspondingly higher prices. South Africa exhibits higher prices but lower popularity, while Switzerland, Ireland, Japan, and Belgium show promise as emerging travel destinations with lower prices and moderate popularity. Spain, the United Kingdom, Italy, and France stand out with a combination of high popularity and relatively lower prices, making them attractive options for budget-conscious travelers.

Ultimately, this project uncovers the shifting dynamics of the rental market by providing an understanding into supply, demand, and pricing dynamics. The findings highlight the impact of external factors such as the pandemic and travel restrictions on pricing and availability trends. By understanding these dynamics, stakeholders can make informed decisions, adapt to evolving market trends, and optimize their strategies in the hospitality industry.

***
<h1 style="color: #FF5A60"><b>II. Problem Statement</b></h1>

This study aims to analyze the changes in Airbnb prices, availability, and demand from 2019 to 2022 and explore variations in these metrics across different countries. The problems to solve are stated as follows:

1. How did Airbnb prices, availability, and demand change over the recent years?
2. How do prices, availability, and demand vary by country?

By addressing these questions, this analysis will provide insight into the temporal trends and cross-country variations of the Airbnb market dynamics, enabling a comprehensive understanding of the evolving rental economy.

***
<h1 style="color: #FF5A60"><b>III. Motivation</b></h1>

The rise of Airbnb has disrupted the traditional travel and hospitality industries, providing travelers with unique and affordable accommodations while enabling hosts to earn extra income by renting out their homes. However, as the number of listings on the platform continues to grow, both hosts and travelers face challenges in optimizing their listings and finding the best deals [3]. 

By analyzing the Inside Airbnb dataset, we can gain valuable insights into the factors that influence the success of Airbnb listings, such as pricing, availability, and demand. This information can help both hosts and travelers make more informed decisions about their listings and bookings, while also identifying trends and opportunities in the market.

Ultimately, this study aims to improve the Airbnb experience for both hosts and travelers, providing a valuable resource for anyone looking to maximize their returns on investment or find the perfect accommodations for their next trip.

***
<h1 style="color: #FF5A60"><b>IV. Data Source</b></h1>

![inside_airbnb.jpg](resources/inside_airbnb.jpg)

<center>Figure 1. Inside Airbnb Logo</center>

**Read Full Content in the included notebook**

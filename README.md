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

**Inside Airbnb Database**

This dataset is available in the jojie public dataset repository. It contains Listings. Below is a quick summary of the database contents.

Filepath: /mnt/data/public/insideairbnb

**Database Summary:**
- Listings data for various cities around the world on the Airbnb platform
- Includes information on location, property type, price, availability, and occupancy rates of Airbnb listings.
- Host data includes several properties managed, reviews, and response rates.
- Valuable resource for studying the impact of the sharing economy on urban housing markets and communities.
- Each City/State has its own detailed `Listings Data`, `Calendar Data`, `Review Data`, and `Neighborhood Data`.
- Created by Murray Cox to help understand the impact of Airbnb on local housing markets and communities.

**Original Data Source**

The dataset can be downloaded from the Inside Airbnb website: http://insideairbnb.com/get-the-data/

<h3>Calendar Dataset</h3>

Among the various datasets in the database, this project focuses on the calendar dataset which provides a detailed view of the availability and pricing for each Airbnb listing over time. It includes information on when each listing is available, how much it costs per night, and any minimum stay requirements.

</br>

<span style="font-size: 14px">
    <center><b>Table 1. Calendar Raw Data Description</b></center>
</span>

|<center>Variable Name</center>|<center>Data type</center>|<center>Variable Caterogy</center>|<center>Description</center>
|:--------------------|:------|:---|:---|
|listing_id           |integer |nominal    |Airbnb's unique identifier for the listing
|date                 |datetime|datetime   |The date in the listing's calendar
|available            |boolean |binary     |Whether the date is available for a booking
|price                |currency|continuous |The price listed for the day

</br>
To extract more meaningful insights, the raw data underwent a comprehensive processing phase where additional features were extracted from the listing data.


</br>
</br>

<span style="font-size: 14px">
    <center><b>Table 2. Calendar Final Data Description</b></center>
</span>

|<center>Variable Name</center>|<center>Data type</center>|<center>Variable Caterogy</center>|<center>Description</center>
|:--------------------|:------|:---|:---|
|listing_id           |integer |nominal    |Airbnb's unique identifier for the listing
|date                 |datetime|datetime   |The date in the listing's calendar
|available            |boolean |binary     |Whether the date is available for a booking
|price                |currency|continuous |The price listed for the day
|adjusted price       |currency|continuous |Reflects the true cost of each listing
|minimum_nights       |integer |continuous |Minimum number of night stay for the listing
|minimum_nights       |integer |continuous |Maximum number of night stays for the listing
|year                 |integer |ordinal    |The year corresponding to the date column.
|month                |string  |ordinal    |The month corresponding to the date column.
|dayofweek            |string  |ordinal    |The day of the week corresponding to the date column.
|country              |string  |nominal    |The country where the Airbnb is listed.

**Read Full Content in the included notebook**

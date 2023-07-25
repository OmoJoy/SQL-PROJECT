# Final-Project-Transforming-and-Analyzing-Data-with-SQL

## Project/Goals

Analyze Transactions: Our primary objective is to meticulously examine the transactions conducted on the company's website. This will involve studying the purchasing patterns, product preferences, and payment methods utilized by visitors from different geographical locations.

Identify Best-selling Products: We intend to determine which products have been most successful in driving sales on the website. By identifying these top-performing items, we can focus on optimizing marketing efforts and ensuring a steady supply to meet customer demand.

Understand Visitor Demographics: Through the analysis of transactions from multiple countries and cities, we seek to gain a comprehensive understanding of the demographics of website visitors. This will enable us to tailor marketing strategies and product offerings to suit the preferences of specific target audiences.

Highlight High-Visitation Countries: Another key goal is to identify the countries that contribute significantly to website traffic. By identifying regions with a high volume of visitors, we can explore opportunities for localized marketing and customer engagement strategies.

Assess Revenue from Different Countries: We aim to calculate and compare the revenues generated from various countries. This analysis will help us recognize the countries with the highest revenue contributions and focus on enhancing sales in these regions.

Generate Actionable Insights: By synthesizing the data gathered from our analysis, we will create actionable insights and recommendations. These insights will guide the company in optimizing its website, marketing campaigns, and product offerings to maximize overall performance.

Support Business Decision-Making: The ultimate goal of this project is to provide the company's management with valuable data-backed insights. These insights will empower them to make informed decisions that drive growth, increase revenue, and enhance the overall customer experience.

Through this comprehensive analysis, we envision assisting the company in strengthening its competitive edge, expanding its global reach, and achieving sustainable growth in the increasingly dynamic online marketplace.


## Process
I first tried to understand the data set and define the relationships between the tables. After that, I established those relationships by setting up primary and foreign keys. Once that was done, I conducted some exploratory analysis on the data set, ensuring I fixed any data type issues I found. Additionally, I performed cleaning tasks by identifying and deleting duplicate rows and unwanted data. Moving on, I identified the end goal and highlighted the columns necessary to answer the questions. This led to more cleaning tasks, such as updating column data, filtering out null or missing data, and modifying the data set to facilitate further transformations.

## Results
Based on my transformation, I believe this data can be used to highlight the following:

Countries/cities with the highest numbers of visitors on the site.
Countries/cities with the visitors making the most purchases on the site.
Countries/cities with the visitors not making purchases on the site.
Countries/cities where the company makes the most of its revenue.
Most selling product categories based on countries/cities.
Least selling product categories based on countries/cities.

## Challenges 
A biggest challenge I experienced was with establishing a relationship between the analytics and the all_sessions table. Those two tables contained important information regarding products sold, revenue generated, and information on the visitors, such as their countries and cities. There were multiple columns (fullvisitorid, visitid) that appeared in both tables, which could have been used for the purpose. However, I could not find any distinct column in either table, forcing me to use a many-to-many relationship to join both tables on the fullvisitorid column.


## Future Goals
The data provided was a bit hazy as there were no clear directives and some important columns were with null values that i initially gave up as i was not finding headway. Being able to access more details about data set and relationships between tables will be highly recommended in future considerations.

![Sales Performance Analysis](https://github.com/chigozie-i/Excel-Sales-Performance-Analysis/raw/main/Hero%20IMG.png)

## Introduction

This project analyzes sales performance to give insight into customers, products, and market dynamics. The insight gained enables stakeholders to make data-driven decisions to improve strategies, increase revenue, and enhance customer satisfaction. 
When sales data is analyzed, we harness the power of data to drive growth, innovation, and competitiveness. Businesses can confidently make informed decisions that align with their goals and objectives.

## Table of Contents
- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Technologies Used](#technologies-used)
- [Project Objective](#project-objective)
- [Key Steps](#key-steps)
- [Conclusion](#conclusion)
- [Recommendation](#recommendation)
- [Disclaimer](#disclaimer)

## Project Overview
The essence of this project is to show insights that can be drawn from a sales dataset to help address business concerns. In this project, I analyzed the sales data of a bicycle store using Microsoft Excel. 
Let’s call the store **Imaginary Inc.
The data set analyzed contains 113,037 rows of transactions carried out over 6-years across six countries.
#### Business Concerns:
The management of Imaginary Inc would like to allocate resources to support marketing efforts and improve revenue properly. They must understand their target demographic and tailor their marketing campaign and product offering accordingly.
They would also like to make informed data-driven decisions about what to stock, what to discontinue, inventory allocation, what to discount, product design, and the introduction of premium models.
The goal is to enable stakeholders to make data-driven decisions to optimize inventory, marketing strategies, pricing, and customer engagement, ultimately leading to improved business outcomes and growth.

## Data Source
https://www.kaggle.com/datasets/nikhilchandra78/bicyclestoredata
## Technologies Used
Microsoft Excel

## Project Objective:
At the core of this project are the business concerns articulated by the management of Imaginary Inc. This project focuses on creating informative reports to help Imaginary Inc’s stakeholders to make well-informed business decisions that address the concerns raised. 

1.	The year-over-year assessment of the comprehensive sales performance is intended to support stakeholders in evaluating the historical business growth trajectory spanning the last six years. Using this data, stakeholders can delve deeper, considering market dynamics and economic factors, to extract additional insights relevant to the growth objectives.

2.	The analysis of sales performance across different regions aims to aid stakeholders in discerning high-performing areas and those requiring heightened focus. This information empowers them to make resource allocation decisions, refine marketing strategies, and strategically target regions to foster growth.

3.	Product sales analysis aims to scrutinize the performance of diverse products, allowing stakeholders to pinpoint the most favoured items and adapt their inventory management and marketing endeavours accordingly. Moreover, they can strategically determine actions such as product promotions, discounts, or the discontinuation of underperforming products.

4.	When age groups are analysed, sales are categorized according to different age segments, facilitating comprehension of the intended demographic. This, in turn, allows for the customization of marketing initiatives and product assortments tailored to distinct age brackets. Such insights guide decisions concerning product design and strategies for engaging with customers.

5.	The Price Point Analysis entails an assessment of sales in relation to varying price categories. By gaining an understanding of the price ranges that yield the highest sales and revenue, stakeholders are empowered to formulate determinations concerning pricing strategies, including the potential introduction of premium models.

## Key Steps

- #### Data Sourcing:
The data utilized was downloaded from Kaggle to my local computer in .csv file format for the purpose of this project.

- #### Data Cleaning:
The dataset was accessed within an Excel workbook titled "Bicycle Dataset". The sheet housing this dataset has been labelled as "Source_Data".
A replication of the original dataset has been generated on a separate worksheet within the same "Bicycle Dataset" workbook. This duplication was accomplished by selecting the entire dataset (Ctrl + Shift + Right arrow, followed by Down arrow), copying it (Ctrl + C), and subsequently pasting it (Ctrl + V) into the new worksheet.
This new worksheet is designated as "Bicycle_Sales". The forthcoming steps in the project involve the cleansing and manipulation of data on the "Bicycle_Sales" worksheet.

![ ](https://github.com/chigozie-i/Excel-Sales-Performance-Analysis/blob/main/SP%20IMG%2001.png)

Employing conditional formatting, I executed a swift examination for vacant cells, given that the uploaded data had undergone substantial cleansing. Given the absence of distinctive identifiers in the sales data, redundant value assessments were unnecessary.
The columns labelled "Profit," "Cost," and "Revenue" were removed, with the objective of facilitating subsequent calculations solely relying on the provided data for order quantity, cost, and selling price.
Additionally, the price columns underwent formatting adjustments to incorporate commas and two decimal places.

- #### Data Modelling:
During the modelling stage, I established a data relationship to facilitate the analysis and generation of insights aligned with the business concerns and needs of Imaginary Inc.
To commence this process, I created a dedicated table for the dataset, designating it as "Bike_Sales." Converting the dataset into a table not only streamlines data management but also enhances interactivity, contributing to an improved overall user experience.
The process of table creation was initiated by selecting the dataset and subsequently utilizing the keyboard shortcut Ctrl + T.

![ ](https://github.com/chigozie-i/Excel-Sales-Performance-Analysis/blob/main/SP%20IMG%2002.png)

Subsequently, to comprehensively address all raised concerns:
Calculation of measures was undertaken. These measures serve to provide insights into sales-related considerations spanning various aspects, including products, regions, market segments, and trend identification, and offer guidance for decisions involving inventory allocation and marketing strategies.
These measures encompass:
1. **Generated Revenue:** A 'Revenue' column was introduced, and revenue calculations were performed by multiplying the values in the 'Order_Quantity' column with those in the 'Unit_Price' column:

    =[@[Order_Quantity]]*[@[Unit_Price]]

3. **Cost of Products Sold:** A new 'Total_Cost' column was generated, and the computation of product costs for ordered items was carried out by multiplying the values in the 'Order_Quantity' column with those in the 'Unit_Cost' column:

    =[@[Order_Quantity]]*[@[Unit_Cost]]

5. **Profit:** A 'Profit' column was introduced, and the profit values were derived by subtracting the 'Total_Cost' column values from the 'Revenue' column values:

    =[@Revenue]-[@[Total_Cost]]

These calculated measures collectively contribute to an enhanced understanding of the data, enabling deeper insights into various operational areas and aiding decision-making processes.

- #### Analysis and Visualization:
During the analysis and visualization stage, I introduced two supplementary worksheets within the Bicycle Dataset workbook and assigned the titles 'Dashboard_Input' and 'Dashboard' accordingly.
The 'Dashboard_Input' sheet incorporates dataset abstractions targeting predefined areas of concern, catering to the analytical process. The visualizations generated will subsequently be replicated onto the 'Dashboard' sheet. This integration of datasets fosters the development of an interactive dashboard.
To initiate this process, I opted to eliminate gridlines from the worksheets. This was undertaken with the intention of enhancing visual clarity and aesthetics, creating a more user-friendly interface. This was achieved by navigating to the Worksheet menu, selecting View, and then deselecting the Gridlines option.

![ ](https://github.com/chigozie-i/Excel-Sales-Performance-Analysis/blob/main/SP%20IMG%2003.png)

#### Analysis of Overall Sales Performance:
To gain insights into the trajectory of business growth, I extracted data pertaining to the overall sales performance across the reviewed years. Stakeholders can utilize this perspective to formulate growth strategies, considering broader macroeconomic and economic factors that influence the business landscape.
To accomplish this, within the 'Dashboard_Input' Sheet, I established a data model displaying the cumulative sales revenue over the specified period. This involved creating two columns: 'Year' and 'Total Revenue'. By employing the following Excel functions, I sourced information from the 'Bicycle_Sales' dataset to populate this table.

For the 'Year' Column:

=SORT(UNIQUE(Bike_Sales[Year]))

For the 'Total Revenue' Column:

=SUMIFS(Bike_Sales[Revenue],Bike_Sales[Year],Dashboard_Input!B5)

Using this data model as a foundation, I generated a line chart illustrating the sales trend, which was subsequently incorporated into the dashboard visualization.

#### Evaluation of Sales Performance by Region:
I assessed sales performance categorized by region, with the intent of aiding stakeholders in identifying regions that exhibit strong performance as well as those that warrant greater attention. Armed with this insightful analysis, Imaginary Inc. gains the ability to strategically allocate resources, refine marketing approaches, or concentrate growth efforts in specific regions.
To realize this objective, I formulated a dynamic data model within the 'Dashboard_Input' Sheet, showcasing cumulative sales revenue for each distinct location. This entailed establishing two columns: 'Country' and 'Revenue'. Additionally, I generated a list to facilitate year-specific visualizations.
Through the utilization of the following Excel functions, I sourced data from the 'Bicycle_Sales' dataset to populate the designated table:

For the 'Country' Column:

=SORT(UNIQUE(Bike_Sales[Country]))

For the 'Revenue' Column:

=SUMIFS(Bike_Sales[Revenue],Bike_Sales[Country],Dashboard_Input!F7, Bike_Sales[Year],Dashboard_Input!$G$4)

![ ](https://github.com/chigozie-i/Excel-Sales-Performance-Analysis/blob/main/SP%20IMG%2004.png) 
![ ](https://github.com/chigozie-i/Excel-Sales-Performance-Analysis/blob/main/SP%20IMG%2005.png)

Leveraging this structured data model, I created an interactive column chart that graphically represents the sales trends for each region. This chart serves as a valuable addition to the dashboard visualization.

#### Analysis of Product Sales:

To facilitate decision-making rooted in product performance, a thorough Product Sales Analysis was conducted. This analysis aimed to scrutinize sales across diverse product categories, spanning various regions and periods. This analytical insight empowers stakeholders to discern the most favoured products, enabling them to strategically fine-tune inventory management and optimize marketing endeavours.
To execute this endeavour, pertinent fields were extracted from the Bicycle_Sales dataset through the application of Excel functions. This methodology was adopted to ensure sustained connectivity and interdependencies, thereby fostering the creation of an interactive dashboard characterized by real-time updates and heightened visibility.

![ ](https://github.com/chigozie-i/Excel-Sales-Performance-Analysis/blob/main/SP%20IMG%2006.png)

For populating the designated table, the 'Product_Category' field was populated with unique and sorted data using the following Excel function:

=SORT(UNIQUE(Bike_Sales[Product_Category]))

Furthermore, the SUMIFS function was leveraged to obtain sales revenue, adhering to specific criteria encompassing year, country, and product category:

=SUMIFS(Bike_Sales[Revenue],Bike_Sales[Product_Category],Dashboard_Input!J9,Bike_Sales[Country],Dashboard_Input!$K$6,Bike_Sales[Year],Dashboard_Input!$K$4)

This analysis culminated in the creation of an interactive doughnut chart that provides an illustrative overview of performance across distinct product categories by year and region.

#### Analysis of Age Groups:

The Age Group Analysis deconstructs sales data according to different age categories, serving the purpose of comprehending the target demographic. This breakdown aids in the customization of marketing initiatives and product offerings, specifically catering to distinct age ranges. The insights gleaned from this analysis equip stakeholders to make informed decisions, encompassing aspects such as product design and strategies for engaging with customers.

![ ](https://github.com/chigozie-i/Excel-Sales-Performance-Analysis/blob/main/SP%20IMG%2007.png)

To compile the designated table, the 'Age Category' field was populated with unique data via the utilization of Excel functions:

=UNIQUE(Bike_Sales[Age_Group])

In addition, the SUMIFS function was employed to extract sales revenue, with consideration for defined criteria:

=SUMIFS(Bike_Sales[Revenue],Bike_Sales[Age_Group],Dashboard_Input!B23,Bike_Sales[Year],Dashboard_Input!$C$20)

To provide a graphical representation of revenue per age group, an interactive bar chart was generated, contributing to a comprehensive understanding of age-related sales patterns.

 #### Exploration of Price Points:

The Price Point Analysis delves into sales from the perspective of different price ranges. By gaining insights into the price intervals that yield the highest sales and revenue, stakeholders acquire the capability to formulate judicious decisions about pricing strategies, potentially including the introduction of premium models.

For the execution of this analysis, a column dedicated to price ranges was introduced, utilizing the Unit Price column as a reference point. The creation of these price ranges was achieved through the implementation of the Excel IF function:

=IF(O3 <= 10, "0-10", IF(O3 <= 50, "11-50", IF(O3 <= 100, "51-100", IF(O3 <= 200, "101-200", IF(O3 <= 500, "201-500", IF(O3 <= 1000, "501-1000", IF(O3 <= 2000, "1001-2000", IF(O3 <= 3000, "2001-3000", "3000+"))))))))

To populate the data model table, I harnessed the UNIQUE and SUMIFS functions. The data generated through these processes served as the foundation for the creation of a funnel chart, facilitating a visual representation of the analysis outcomes.

![ ](https://github.com/chigozie-i/Excel-Sales-Performance-Analysis/blob/main/SP%20IMG%2008.png)

The outcomes of the sales performance analysis were consolidated into a dashboard, furnishing an interactive and visually informative representation of data insights pertinent to the reviewed time.

![ ](https://github.com/chigozie-i/Excel-Sales-Performance-Analysis/blob/main/SP%20IMG%2009.png)

## CONCLUSION

During this project, a comprehensive analysis of various dimensions of sales performance within Imaginary Inc. was conducted. The insights garnered from the analysis shed light on critical aspects of the business, empowering stakeholders to make informed decisions and formulate strategic plans. Each analysis provided unique perspectives, contributing to a well-rounded understanding of the company's operations.

The evaluation of overall sales performance unveiled the trajectory of business growth over the past years. This historical context, combined with considerations of economic and macroeconomic influences, offers a solid foundation for future growth strategies.
Sales performance by region offered valuable insights into regional strengths and areas warranting attention. This knowledge equips Imaginary Inc. with the ability to allocate resources effectively, design targeted marketing campaigns, and optimize regional growth efforts.

The analysis of product sales provided a deeper understanding of product popularity across regions and periods. This information is pivotal for product design enhancements and customer engagement strategies, ensuring the alignment of offerings with customer preferences.
Price point analysis illuminated sales patterns across different price ranges, facilitating pricing strategies and the potential introduction of premium models. 

This understanding aids in maximizing revenue and catering to varying customer segments.
The breakdown of sales by age group enabled a grasp of the target demographic, thereby refining marketing campaigns and product offerings to cater to specific age ranges.

## RECOMMENDATION

Based on the findings of the analyses, several recommendations can be offered to enhance Imaginary Inc.'s operations and growth:
1. **Strategic Growth Planning:** Utilize the insights from the overall sales performance analysis to formulate data-driven growth plans, accounting for historical trends and external economic factors.
2. **Regional Focus:** Leverage the sales performance by region analysis to allocate resources strategically, develop tailored marketing strategies, and prioritize expansion efforts in underperforming regions.
3. **Product Enhancement:** Capitalize on the product sales analysis to fine-tune product offerings, optimizing their alignment with customer preferences and regional demands.
4. **Pricing Strategy:** Utilize the price point analysis to devise dynamic pricing strategies that capitalize on sales trends across different price ranges, potentially exploring premium offerings.
5. **Targeted Marketing:** Leverage the insights from the age group analysis to tailor marketing campaigns to specific age segments, ensuring maximum impact and engagement.
6. **Continual Monitoring:** Establish a system for ongoing data analysis and visualization, fostering real-time decision-making and adaptability to market changes.
Incorporating these recommendations into Imaginary Inc.'s business strategy will harness the power of data-driven insights, leading to improved operational efficiency, enhanced customer satisfaction, and sustained growth in a competitive market landscape.

## DISCLAIMER
The information and insights provided within this project are based solely on the dataset used. The assumptions are aligned with typical business objectives. This analysis offers a broad overview of my proficiency in conducting analytical procedures on data. It's important to note that Imaginary Inc. is a fictitious entity. This project exemplifies the potential application of data analysis in assessing sales performance. This analysis is intended to provide a high-level understanding of the methodology used for sales analysis, recognizing that individual business circumstances vary.



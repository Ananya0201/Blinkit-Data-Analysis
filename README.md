# Blinkit Analysis dashboard:

### Dashboard Link : https://app.powerbi.com/groups/me/reports/a8a47452-a1d0-466b-9c7b-03894874ac48/ReportSection?experience=power-bi

## Process for preparing the project:

1. Understanding Business requirement.

2.Data Walkthrough

3.Data connection

4.Data cleaning

5.Data modelling

6.Data processing

7.Dax calculations

8.Dashboard layout

9.Chart development

10.dashboard/report development

11.Insights generation/Recommendations

## Understanding Business requirement:
To conduct a comprehensive analysis of blinkit sales performance, customer satisfaction and inventory distribution to identify key insights and opportunities for optimization using various KPIs and visualisation in Power Bi.
### KPI Requirement:
Total sales: The overall revenue generated from all items sold

Avg Sales: The avg revenue per sale

Number of Items: the count of different items sold

Average rating: The average customer rating for items sold

### Chart requirements:
KPI's usually give an overview on how the business is performing on a higher level, but to deep dive in the data and to see at specific level how a particular part of the business is performing, we will have to prepare or build charts to draw insights so that business decisions can be made at the departmental level.

#### 1.Total sales by fat content:
Objective : analyze the impact of fat content on total sales.

Additional KPI metrics: Assess how other KPIs(Average sales, number of items, avg rating) vary with fat content.

Chart type: Donut Chart

#### 2.Total sales by item type:
Objective: Identify the performance of different item types in terms of total sales.

Additional KPI Metrics:Assess how other KPIs(Average sales, number of items, avg rating) vary with fat content.

Chart type: Bar chart

#### 3. Fat content by outlet for total sales:
Objective: Compare total sales across different outlets segmented by fat content.

Additional KPI Metrics: Assess how other KPIs(Average sales, number of items, avg rating) vary with fat content.

Chart Type: Stacked Column Chart

#### 4.Total Sales by Outlet :
Objective: Evaluate how the age or type of outlet establishment influences total sales.

Chart type: Line chart.

#### 5.Sales by outlet size:
Objective: Analyze the correlation between outlet size and total sales

Chart type: donut/pie

#### 6.Sales by outlet location:
Objective: assess the geographic distribution of sales across different locations.

Chart type: Funnel map


#### 7.All metrics by outlet type:
Objective: Provide a comprehensive view of all key metrics(Average sales, number of items, avg rating)

Chart type: Matrix card

### ❖	Business Objective Statement:
The business objective of this study aims to uncover significant relationships, trends and patterns. To identify how the key metrics are contributing to the total sales turnover and  to suggest prioritized critical recommendations and performance improvements on the same.
 

#### ❖	Overview : 
The dataset contains feature vectors for 8523 data points. The data is curated to avoid bias in order to derive genuine results. The dataset consists of a total of 12 columns out of which - 5 are numerical and 7 categorical attributes.

#### ❖	Explanation: 
The dataset includes the following fields:

●	Item Fat Content : The fat content in a particular product that the customer is buying.

●	Item Identifier : Required for the business to identify different products. 

●	Item Type : Type of product to be sold(eg: fruits, frozen items, snacks,etc).

●	Outlet Establishment Year : Year when the outlet was setup.

●	Outlet Identifier : Like item identifier , required for the business to identify each outlet. 

●	Outlet Location Type : Location of the outlet(cities)

●	Outlet Size : Size of the outlet whether Big , small , medium.

●	Outlet Type : Type of outlet - Supermarket or Grocery Store. Supermarket is the storage unit used by the business for the goods. Grocery stores are tie-up with Blinkit to provide the goods for delivery in locations where the supermarket is not serviceable.

●	Item Visibility: Visibility of an item when a user is viewing the app.

●	Item Weight: Weight of an item based on which delivery charges is decided.

●	Sales: Sales of that particular order

●	Rating: Given by the customer for the particular order.

### Steps followed 

- Step 1 : Load dataset into Power BI Desktop, dataset is an xlxs file type.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns, errors & empty values were present except column named "Item Weight" which had 1436 empty rows. 
- Step 5 : Since the "item weight" column doesnt contribute significantly in the kpi requirement, hence the column was not considered.
- Step 6 : Visual filters (Slicers) were added for four fields named "Outlet Location", "Outlet Size", "Item Type" & "Item fat content".
- Step 7 : Four card visuals were added to the canvas, representing Total Sales, Avg Sales,Average rating & number of items.

In our dataset, Some parameters were empty, representing those parameters are not applicable for KPI requirement.

- Step 8 : In the report view, under the insert tab, two text boxes were added to the canvas, in one of them name of the Company (BLINKIT) is mentioned & in the other one company's tagline was written.
- Step 9 : In the report view, under the insert tab, using shapes option from elements group a rectangle was inserted & the filter(Slicers) was added to the rectangle along with Company name and Tagline.
- Step 10 : New measure was created to calculate Total Sales.
  Following DAX expression was written for the same,

       Total Sales = SUM('BlinkIT Grocery Data'[Sales])
A card visual was used to represent this.
 
 Snap of Total Sales

 ![Screenshot 2024-09-07 002601](https://github.com/user-attachments/assets/b5330e21-2454-4e1f-8547-9523a4a7feda)

- Step 11 : New measure was created to calculate Avg Sales.
  Following DAX expression was written for the same,

       Avg Sales = AVERAGE('BlinkIT Grocery Data'[Sales])
A card visual was used to represent this.
 
 Snap of Avg Sales

 ![Screenshot 2024-09-07 003105](https://github.com/user-attachments/assets/b745aead-49e1-4725-a4d6-241263daa465)

- Step 12 : New measure was created to calculate Avg Rating.
  Following DAX expression was written for the same,

       Avg Rating = AVERAGE('BlinkIT Grocery Data'[Rating])
A card visual was used to represent this.
 
 Snap of Avg Rating

 ![Screenshot 2024-09-07 003304](https://github.com/user-attachments/assets/50da0fd5-0776-49ce-b996-635dde35c885)

- Step 13 : New measure was created to calculate Number of items.
  Following DAX expression was written for the same,

       No of items = COUNTROWS('BlinkIT Grocery Data')
A card visual was used to represent this.
 
 Snap of Number of items
 ![Screenshot 2024-09-07 003516](https://github.com/user-attachments/assets/21019176-613d-4f22-9041-39e9699295b5)

- Step 14 : The report was then published to Power BI Service after doing the required computations as per the business requirement.

#### Report Snapshot (Power BI DESKTOP)

![Screenshot 2024-09-07 003708](https://github.com/user-attachments/assets/b155ea84-b98f-4fd2-bc2b-7ca500fede27)

### ❖	Insights:
A single page report was created on Power BI Desktop & it was then published to Power BI Service.
1. The Total Sales is around 1.20 million and the average sales per order is around $141. The average rating from customers is 3.9 and the number of items sold is 8523 which gives an idea of the transaction volume over the period for which the data is analysed.

#### Recommendation: 
The average sales suggests that mid-range products are likely driving a significant portion of the revenue. The average rating leaves room for improvement in services/products. The no of items sold should be increased and offering variety in mid range products is likely to drive up sales.

2. The Number of items sold is higher for the products with low fat content in all locations- Tier 1, 2 & 3. Fruits and vegetable have the highest sales followed closely by snack and household items. Although the avg sales value is highest for household items. 2/3rd of the sales is from low fat content items. The rating on an avg is same for all the items and is consistent throughout all the locations.
#### Recommendation: 
Since 2/3rd of the sales is from LF items - the LF items can be stocked having variety to drive up business. Weekend/Time based promotions and discounts for loyal customers on the highest selling items with higher avg value per order is likely to drive up sales.

3. The maximum number of outlets were established in 2018 and there was a peak in sales observed. The sales from the Medium and low Outlet is at par and the sales from high outlets is 1/3rd of the total sales.On further breakdown, it is noted that the items stocked in inventory is comparatively less for the High outlets than small and medium. The item Visibility for both small and high outlet is similar but since the inventory is less, the sales generated from the high outle is only 20% of the total sales.

#### Recommendation: 
Since both LF items and regular items have demand at par with each other, the items stocked for LF and regular should be similar and in higher volume for the High outlet to optimize revenue generation.
 


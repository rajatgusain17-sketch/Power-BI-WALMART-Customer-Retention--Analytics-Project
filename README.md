# Retail Customer Retention Analytics – Walmart
## Project Overview
This project focuses on analyzing customer retention patterns for Walmart using Power BI.
The objective was to transform raw retail data into actionable business insights that help identify churn patterns, understand customer behavior, evaluate loyalty program effectiveness, and improve retention strategies.

The dashboard was designed with a business-focused approach to support data-driven decision-making across customer engagement, promotions, store performance, and customer lifetime value analysis.

---


## Business Problem
Walmart operates across multiple physical stores and online channels, generating large volumes of customer and transaction data.

However, the existing reporting lacked analytical depth to answer important business questions such as:

•Why are customers churning?   
•Which customers are most valuable?        
•Which customer segments are at risk?        
•Are promotions improving retention?                     
•Which channels and store types are underperforming?             
•How effective is the loyalty program?          

This project solves these challenges by building an interactive multi-page Power BI dashboard focused on retention analytics.

---



## Objectives
•Analyze customer churn and retention patterns            
•Identify loyal, repeat, and high-value customers          
•Evaluate the impact of promotions and loyalty programs              
•Analyze store and channel performance             
•Perform Customer Lifetime Value (CLV) analysis             
•Provide actionable business recommendations     

---



## Datasets Used   
### 1. Customer Demographics
Contains customer profile information.

#### Columns:

•Customer_ID           
•Age             
•Gender            
•Region              
•Income_Level          
•Membership_Since         
•Preferred_Channel           
### 2. Customer Transactions       
Contains transaction-level purchase history.

#### Columns:

•Transaction_ID     
•Customer_ID          
•Store_ID               
•Product_Category            
•Transaction_Date       
•Amount             
•Promotion_Applied     
### 3. Store Locations         
Contains store-related information.

#### Columns:      

•Store_ID         
•Store_Type      
•Region           
•Opening_Year         
### 4. Loyalty Program              
Contains loyalty tier and points information.

#### Columns:

•Customer_ID          
•Loyalty_Tier        
•Points_Earned            
•Points_Redeemed            
### 5. Churn Labelled Customers  
Contains churn-related information.

#### Columns:      

•Customer_ID           
•Last_Purchase_Date           
•Churn_Flag           
•Churn_Reason             

---



## Tools & Technologies         
•Power BI       
•Power Query                     
•DAX (Data Analysis Expressions)           
•Data Modeling                    
•Interactive Dashboard Design     

---



## Data Cleaning & Modeling          
The following preprocessing steps were performed:

•Handled missing values       
•Removed duplicate records          
•Corrected data types            
•Created calculated columns               
•Built relationships between datasets      

---


## Data Model Relationships
•Customer → Transactions     
•Customer → Loyalty Program       
•Customer → Churn Data            
•Transactions → Store Locations          
A star schema approach was followed for efficient filtering and reporting.


---




# Key DAX Calculations
## Membership Duration
```Membership_Duration = DATEDIFF(Customer_Demographics[Membership_Since],TODAY(),YEAR)```            

## Churn Rate %
```Churn Rate % = DIVIDE([Churned Customers],[Total Customers]) * 100```

## Customer Lifetime Value (CLV)
```CLV = DIVIDE(SUM(Customer_Transactions[Amount]),AVERAGE(Customer_Demographics[Membership_Duration]))```


---



# Dashboard Pages
## Page 1 – Executive Overview    
This page provides a high-level business summary using KPI cards and funnel analysis.

### KPIs Included
•Total Customers       
•Repeat Customers      
•Churn Rate                    
•Customer Lifetime Value (CLV)            
### Insights            
•Overall retention performance           
•Customer conversion flow           
•Churn overview        
## Page 2 – Loyalty & Promotion Impact          
This page analyzes the effectiveness of promotions and loyalty programs.     

### Visuals Included           
•Promotion Usage %           
•Avg Purchase by Promotion       
•Churn by Loyalty Tier         
•Points Earned vs Redeemed        
### Insights        
•Promotion impact on purchase behavior        
•Loyalty engagement analysis               
•Redemption inefficiencies              
## Page 3 – Store & Channel Insights        
This page focuses on store and channel performance.    

### Visuals Included        
•Avg Transaction by Store Type          
•Churn by Store Type       
•Channel Performance         
•Store Opening Year vs Retention      
### Insights  
•Underperforming channels       
•Store-level retention patterns         
•Correlation between store age and churn   
## Page 4 – Customer Segmentation        
This page analyzes customer purchase behavior and segmentation.

### Segments        
•Low (0–3 purchases)   
•Mid (4–8 purchases)     
•High (9+ purchases)     
### Visuals Included          
•Segment Distribution     
•Avg Purchase Frequency            
•Product Category Preferences      
•Age Group Analysis       
### Insights          
•High-value customer behavior      
•Repeat purchase trends        
•Product preference patterns       
## Page 5 – CLV Analysis      
This page focuses on Customer Lifetime Value analysis.

### Visuals Included      
•CLV vs Days Since Last Purchase       
•CLV by Region       
•CLV by Loyalty Tier         
•CLV Segment Distribution            
### Insights            
•High-value but inactive customers        
•Regional CLV trends                       
•Retention prioritization opportunities


---


# Key Business Insights       
•Customer churn varies significantly across regions and channels         
•Mid-tier customers show strong growth potential         
•Online channels demonstrate relatively higher churn         
•Loyalty point redemption is lower than points earned            
•High CLV customers require proactive retention strategies   

---


# Recommendations       
## 1. Prioritize Mid-Tier Customers    
Mid-tier customers have high conversion potential and should be targeted through personalized campaigns and loyalty incentives.

---


## 2. Improve Online Channel Experience   
The online channel shows relatively higher churn and requires improvements in customer experience, delivery reliability, and engagement.

---

 
## 3. Enhance Loyalty Program Engagement
Simplifying the redemption process and offering more personalized rewards can significantly improve customer engagement and retention.

---



# Learning Outcomes 
Through this project, I gained practical experience in:

•Business-focused dashboard development     
•Customer retention analytics      
•Data modeling in Power BI       
•DAX calculations      
•Customer segmentation         
•CLV analysis                                            
•Translating data into actionable business insights  

---


# Conclusion 
This project demonstrates how Power BI can be used to solve real-world retail business problems through data-driven analysis and visualization.

The dashboard provides a complete analytical view of customer behavior, retention patterns, loyalty engagement, and business performance, helping organizations make informed strategic decisions.


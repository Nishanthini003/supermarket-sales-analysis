****** 🛒 Supermarket Sales Analysis Using Power BI******

This project is a **Power BI dashboard** that analyzes and visualizes key insights from a supermarket sales dataset. It was created as part of a group assignment (Group 9) and demonstrates the ability to perform data cleaning, transformation, and interactive dashboard development using Power BI.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

 📁 File

Group9-SuperMarket.pbix — Power BI project file containing all visuals, DAX measures, and report pages.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

 📊 Key Features

- 🔍 **Sales Analysis** by product, branch, customer type, gender, and payment method.
- 💰 **Revenue & Profit Tracking** using custom DAX measures.
- 📅 **Time-based Trends**: Sales over days and months.
- 📌 **KPIs**: Total sales, average rating, gross income, quantity sold.
- 🎛️ **Slicers & Filters**: Region-wise, category-wise, and customer-type filtering.
- 📈 **Interactive Visuals**: Bar charts, pie charts, line graphs, and card KPIs.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

 🛠 Tools Used

- **Power BI Desktop**
- **DAX (Data Analysis Expressions)****
- **Power Query**
- Excel (.csv) as data source

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

## *DAX (Data Analysis Expressions)****
**LOSS**
- LOSS% = [TOTAL LOSS RATE]/[TOTAL QUANTITY SOLD]*100
- Max Loss Rate = MAX('loss'[Loss Rate (%)])
- Min Loss Rate = MIN('loss'[Loss Rate (%)])
- TOTAL LOSS IN RUPEES = [TOTAL LOSS RATE]*[TOTAL QUANTITY SOLD]*[TOTAL UNIT SELLING PRICE]
- TOTAL LOSS RATE = SUM(loss[Loss Rate (%)])

**PRICE**
 - AVERAGE SELLING PRICE = [TOTAL UNIT SELLING PRICE]/[TOTAL QUANTITY SOLD]
 - Profit = [Revenue] - [Total Wholesale Cost]
 - Profit % = DIVIDE([Profit], [Revenue], 0) * 100
 - Revenue = SUMX('Price', 'Price'[Total Quantity Sold] * 'Price'[Total Unit Selling Price])
 - TOTAL AMOUNT = [TOTAL QUANTITY SOLD]*[TOTAL UNIT SELLING PRICE]
 - TOTAL QUANTITY SOLD = SUM('price'[Quantity Sold (kilo)])
 - TOTAL UNIT SELLING PRICE = SUM('price'[Unit Selling Price (RMB/kg)])

**Product**
 - Category Count = DISTINCTCOUNT('Product'[Category Code])

**wholesale**
 - Average Wholesale Price = AVERAGE('wholesale'[Wholesale Price (RMB/kg)])
 - COST = [TOTAL WHOLESALE PRICE]*[TOTAL QUANTITY SOLD]
 - Total Wholesale Cost = SUMX('Price', 'price'[TOTAL QUANTITY SOLD] * ('wholesale'[Average Wholesale Price]))
 - TOTAL WHOLESALE PRICE = SUM(wholesale[Wholesale Price (RMB/kg)])


--------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🧠 Insights

- Branch C had the highest revenue and customer satisfaction.
- Female customers slightly outspent male customers on average.
- E-wallet and Cash were the most preferred payment methods.
- Health and Food categories were top-performing.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

 📌 Contact

For queries or feedback, feel free to reach out:  
📧 nishanthiniram23@gmail.com  

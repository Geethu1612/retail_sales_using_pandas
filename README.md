🛒 Retail Sales Data Analysis
📌 Objective
Analyze retail sales data to uncover trends, patterns, and insights using Python and Pandas, and visualize the results through charts.

🛠 Tools & Technologies
    Python

    Pandas (data manipulation)

    Matplotlib(visualization)

    Jupyter Notebook / Google Colab

📂 Dataset
We used a Retail Sales Dataset containing the following columns:

    Transaction ID – Unique identifier for each transaction

    Date – Date of the purchase

    Customer ID – Unique ID of each customer

    Gender – Gender of the customer

    Age – Age of the customer

    Product Category – Category of the purchased product

    Quantity – Number of units purchased

    Price per Unit – Price of a single unit

    Total Amount – Total transaction value (Quantity × Price per Unit)

👉 Steps Performed
1. Load CSV File using Pandas
    import pandas as pd
    df = pd.read_csv("retail_sales.csv")

2. Data Cleaning & Exploration

    Checked for missing values.
    Reviewed dataset shape & info.
    Basic statistics with df.describe(). & df.info()
    
    df.describe() -> provides a statistical summary of a DataFrame or Series
    df.info() -> used to obtain a concise summary of a DataFrame.

3. Data Analysis
 Total sales by Product category
   ⚡ sales_by_category = df.groupby('Product Category')['Total Amount'].sum()

 Orders By Gender
    ⚡orders_by_gender = df.groupby('Gender')['Transaction ID'].count()

 Top-selling prodeucts by quantity
     ⚡top_products = df.groupby('Product Category')['Quantity'].sum()

4. Data Visualization
    Bar charts for sales & orders distribution
    Pie charts for product category share
    Line charts for sales trends over time

    ⚡sales_by_category.plot(kind='bar', color='skyblue')
    plt.title('Total Sales by Product Category')
    plt.ylabel('Total Sales Amount')
    plt.show()

📊 Key Insights
Identified top-selling product categories.
Found customer purchasing trends by gender.
Observed seasonal/monthly sales patterns.

![alt text](image.png)
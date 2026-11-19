# Retail Sales & Returns Analysis (Python)

A data analysis project on the sales and returns of a retail business with 4 stores in the UAE. The project combines 5 CSV files, calculates the key sales and return numbers, and shows the results with charts.

## Objectives

- Combine customers, products, stores, sales and returns data into one dataset
- Find total sales, average purchase value, top products, top customers and the best cities, stores and categories
- Calculate the return rate, total refund amount and the main reasons for returns
- Present the results with charts and write down the key insights

## Dataset

The data covers about one year of sales (Oct 2024 - Oct 2025) and has 5 CSV files:

| File | Rows | Columns |
|---|---|---|
| `Customers.csv` | 200 | CustomerID, Name, Gender, Age, City, SignupDate |
| `products.csv` | 8 | ProductID, ProductName, Category, Price |
| `stores.csv` | 4 | StoreID, StoreName, City, Manager |
| `sales.csv` | 2,000 | SaleID, Date, ProductID, CustomerID, StoreID, Quantity, PaymentMode |
| `returns.csv` | 140 | ReturnID, SaleID, ReturnDate, Reason, RefundAmount |

## Tools Used

- Python
- pandas
- matplotlib
- seaborn
- Jupyter Notebook

## Steps

1. Loaded the 5 CSV files with pandas
2. Merged sales with products, customers and stores (left joins)
3. Converted `SignupDate` to date format and checked for missing values
4. Created a new column `TotalAmount = Quantity x Price`
5. Analysed sales by product, customer, city, gender, category and store
6. Merged the returns data and calculated the refund amount, return rate and return reasons
7. Created charts and wrote the insights

## Key Findings

### Sales
- Total sales are **2,215,122** and the average purchase per transaction is **1,107.56**.
- Top 3 products are **Luxury Bag** (392,944), **Classic Watch** (375,747) and **Perfume Set** (351,000). Together they make up about 51% of sales.
- **Accessories** is the top category (about 35% of sales) and **Electronics** is the lowest (about 7%).
- **Ajman** (621,401) and **Dubai** (610,892) are the top cities. Abu Dhabi and Sharjah are each about 22%.
- Female customers account for 51.6% of sales and male customers for 48.4%.
- Monthly sales stay between about 167,000 and 209,000, with a peak in April 2025.

### Returns
- **140 of 2,000 sales** were returned, so the **return rate is 7.00%**.
- Total refunds are **170,327** (about 7.7% of sales).
- **Perfume** has the highest return rate (7.95%) and **Electronics** the lowest (5.06%).
- Return reasons are almost equal: Changed Mind (49), Wrong Item (49) and Defective (42).

## Recommendations

- Check order picking and packing to reduce **Wrong Item** returns.
- Look at why **Electronics** sells much less than the other categories.
- Keep the stock of the top 3 products high, because they bring in about half of the revenue.

## Project Structure

```
retail-sales-analysis/
|-- retail_sales_analysis.ipynb
|-- Customers.csv
|-- products.csv
|-- stores.csv
|-- sales.csv
|-- returns.csv
|-- README.md
```

## How to Run

1. Download or clone this repository.
2. Install the libraries: `pip install pandas matplotlib seaborn jupyter`
3. Keep the notebook and the 5 CSV files in the same folder.
4. Open `retail_sales_analysis.ipynb` in Jupyter Notebook and click **Run All**.

## Author

Nithika

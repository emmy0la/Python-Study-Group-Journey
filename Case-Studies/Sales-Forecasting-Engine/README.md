# Sales Forecasting Engine For BrightMart Retail Ltd.

A Python case study that turns weekly retail sales data into actionable business insights.

![Python](https://img.shields.io/badge/Python-3.13-blue.svg)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen.svg)

## Project Overview

What happens when a retail manager has to review weekly sales, forecast future demand, check inventory levels, and make marketing decisions, all using manual calculations?

That is the business problem behind this project.

For my first industry-focused case study in the Python Study Group, I stepped into the role of a Junior Python Developer working with the sales team at a fictional retail company, BrightMart Retail Ltd.

The goal was simple: build a Sales Forecasting Engine that takes basic weekly sales information and transforms it into meaningful business insights.

Using only the Python fundamentals covered in Lessons 1 to 5, the program calculates revenue, forecasts next week's sales, updates inventory, evaluates sales performance, and applies business rules to support decisions around restocking, promotion, and demand.

This project helped me move from learning Python syntax to thinking about how code can solve practical business problems.

---

## The Business Scenario

BrightMart Retail Ltd. is a growing supermarket chain.

Every Monday, the sales team reviews the previous week's performance and prepares for the week ahead.

The team needs answers to questions such as:

* How much revenue did we generate?
* Are we on track to meet our sales target?
* How many units might we sell next week?
* How much revenue could we expect?
* Do we need to restock?
* Is the product available for promotion?
* Is demand likely to be high?

Previously, these calculations were performed manually.

My task was to automate the analysis with Python and present the results in a clear, professional sales report.

---

## What the Project Does

The Sales Forecasting Engine processes weekly product information and calculates:

* Weekly revenue
* Forecasted sales based on expected growth
* Forecasted revenue
* Updated inventory levels
* Sales target achievement
* Restocking requirements
* Promotion eligibility
* High-demand forecasts

The project also includes an optional multi-product analysis that compares two products and supports management decisions about revenue, inventory, demand, and marketing priorities.

---

## Project Data

The primary product analyzed is a Wireless Mouse.

| Metric               |          Value |
| -------------------- | -------------: |
| Product              | Wireless Mouse |
| Selling Price        |        ₦12,500 |
| Units Sold           |            180 |
| Weekly Sales Target  |            200 |
| Forecast Growth Rate |            15% |
| Initial Stock        |      250 Units |
| Minimum Stock Level  |      120 Units |
| Product Available    |           True |

The Bonus Challenge introduces a second product, a Bluetooth Speaker, to demonstrate how the same business logic can be applied to compare multiple products.

---

## How the Engine Works

The project follows a simple business workflow:

```text
Sales Data
    ↓
Revenue Calculation
    ↓
Sales Forecast
    ↓
Revenue Forecast
    ↓
Inventory Update
    ↓
Business Rule Evaluation
    ↓
Sales Forecast Report
    ↓
Business Insights
```

The program first stores the business data in variables.

It then performs the required calculations.

Finally, it evaluates the results against predefined business rules and presents the findings in a structured report.

This follows a simple principle:

> Calculate first. Evaluate next. Communicate the result clearly.

---

## Key Python Concepts Demonstrated

This project was intentionally built using only the Python concepts covered in Lessons 1 to 5.

| Python Concept       | How It Was Applied                                  |
| -------------------- | --------------------------------------------------- |
| Variables            | Stored product, sales, inventory, and business data |
| Data Types           | Used strings, integers, floats, and Booleans        |
| Arithmetic Operators | Calculated revenue and sales forecasts              |
| Assignment Operators | Updated inventory using `-=`                        |
| Comparison Operators | Evaluated sales targets and stock levels            |
| Logical Operators    | Combined business rules for promotion and demand    |
| Formatted Output     | Generated a readable business report                |

The goal was to demonstrate that even basic Python concepts can be combined to solve meaningful business problems.

---

## Core Implementation

### 1. Creating the Business Variables

The project begins by converting the business information provided by the sales manager into meaningful Python variables.
The variables were created using appropriate data types and descriptive names.

![image alt](https://github.com/emmy0la/SALES-FORECASTING-ENGINE-FOR-BRIGHTMART-RETAIL-LTD./blob/95368bfd0b0441e2c129654fe2c92a37b4e31b22/Images/01-variable-initialization.png)

### 2. Weekly Revenue

The weekly revenue is calculated by multiplying the selling price by the number of units sold.

```python
weekly_revenue = selling_price * units_sold
```

For the Wireless Mouse:

```text
₦12,500 × 180 = ₦2,250,000
```
![image alt](https://github.com/emmy0la/SALES-FORECASTING-ENGINE-FOR-BRIGHTMART-RETAIL-LTD./blob/d592bca97615fd392a90254f1e850cb9d2333e99/Images/02-weekly-revenue.png)

### 3. Sales Forecast

The next week's sales are forecast using the expected 15% growth rate.

```python
forecast_sales = int(
    units_sold + (units_sold * forecast_growth_rate / 100)
)
```

The result is:

```text
Forecast Sales = 207 Units
```
![image alt](https://github.com/emmy0la/SALES-FORECASTING-ENGINE-FOR-BRIGHTMART-RETAIL-LTD./blob/d592bca97615fd392a90254f1e850cb9d2333e99/Images/03-sales-forecast.png)

### 4. Revenue Forecast

The expected revenue for the following week is calculated using the forecasted sales.

```python
forecast_revenue = forecast_sales * selling_price
```

The result is:

```text
Forecast Revenue = ₦2,587,500
```
![image alt](https://github.com/emmy0la/SALES-FORECASTING-ENGINE-FOR-BRIGHTMART-RETAIL-LTD./blob/d592bca97615fd392a90254f1e850cb9d2333e99/Images/04-forecast-revenue.png)

### 5. Inventory Update

The program updates the inventory after accounting for units sold.

```python
current_stock -= units_sold
```

The stock changes from:

```text
250 Units → 70 Units
```
![image alt](https://github.com/emmy0la/SALES-FORECASTING-ENGINE-FOR-BRIGHTMART-RETAIL-LTD./blob/d592bca97615fd392a90254f1e850cb9d2333e99/Images/05-inventory-update.png)

### 6. Business Rules

The program uses comparison and logical operators to evaluate business conditions.

For example, sales target achievement:

```python
sales_target_achieved = units_sold >= weekly_sales_target
```

Promotion eligibility:

```python
promotion_eligible = (
    product_available and sales_target_achieved
)
```

High-demand forecast:

```python
high_demand_forecast = (
    forecast_sales > 200 or
    forecast_revenue > 2500000
)
```
![image alt](https://github.com/emmy0la/SALES-FORECASTING-ENGINE-FOR-BRIGHTMART-RETAIL-LTD./blob/d592bca97615fd392a90254f1e850cb9d2333e99/Images/06-business-rules.png)

These rules allow the program to translate business requirements into simple, executable Python logic.

---

## Results

### Wireless Mouse

| Metric                |     Result |
| --------------------- | ---------: |
| Weekly Revenue        | ₦2,250,000 |
| Forecast Sales        |  207 Units |
| Forecast Revenue      | ₦2,587,500 |
| Updated Stock         |   70 Units |
| Sales Target Achieved |      False |
| Restocking Required   |       True |
| Product Available     |       True |
| Promotion Eligible    |      False |
| High Demand Forecast  |       True |

![image alt](https://github.com/emmy0la/SALES-FORECASTING-ENGINE-FOR-BRIGHTMART-RETAIL-LTD./blob/441304b09083fc7456ff6b06b090b7d50c1ca40a/Images/07-product-1-sales-report.png)


### Bluetooth Speaker

The optional Bonus Challenge introduces a second product.

| Metric                |     Result |
| --------------------- | ---------: |
| Weekly Revenue        | ₦3,325,000 |
| Forecast Sales        |  114 Units |
| Forecast Revenue      | ₦3,990,000 |
| Updated Stock         |   45 Units |
| Sales Target Achieved |      False |
| Restocking Required   |       True |
| Product Available     |       True |
| Promotion Eligible    |      False |
| High Demand Forecast  |       True |

![image alt](https://github.com/emmy0la/SALES-FORECASTING-ENGINE-FOR-BRIGHTMART-RETAIL-LTD./blob/441304b09083fc7456ff6b06b090b7d50c1ca40a/Images/08-product-2-sales-report.png)
---

## Business Insights

The analysis produced several useful observations.
![image alt](https://github.com/emmy0la/SALES-FORECASTING-ENGINE-FOR-BRIGHTMART-RETAIL-LTD./blob/441304b09083fc7456ff6b06b090b7d50c1ca40a/Images/09-product-comparison.png)


### 1. The Bluetooth Speaker generated more weekly revenue

```text
Bluetooth Speaker: ₦3,325,000
Wireless Mouse:    ₦2,250,000
```

The Bluetooth Speaker generated ₦1,075,000 more revenue during the week.

### 2. The Bluetooth Speaker also has the higher forecasted revenue

```text
Bluetooth Speaker: ₦3,990,000
Wireless Mouse:    ₦2,587,500
```

Based on the forecast assumptions, the Bluetooth Speaker is expected to generate higher revenue next week.

### 3. Both products require restocking

The Wireless Mouse has 70 units remaining against a minimum stock level of 120 units.

The Bluetooth Speaker has 45 units remaining against a minimum stock level of 80 units.

Both products have fallen below their minimum stock thresholds.

### 4. Both products show high demand under the defined business rule

The high-demand rule is triggered when either forecasted sales exceed 200 units or forecasted revenue exceeds ₦2,500,000.

The Wireless Mouse qualifies through both conditions.

The Bluetooth Speaker qualifies through its forecasted revenue of ₦3,990,000.

### 5. The Bluetooth Speaker is the stronger marketing priority

Based on the project assumptions, the Bluetooth Speaker combines:

* Higher weekly revenue
* Higher forecasted revenue
* High forecast demand

Therefore, management could consider prioritizing it in the next marketing campaign, while ensuring adequate stock is available.

---

## What I Learned

This project helped me understand that writing Python code is only one part of solving a business problem.

The bigger challenge is translating a business requirement into a logical sequence of operations.

I practiced how to:

* Break a business problem into smaller tasks
* Identify the data required for each calculation
* Choose appropriate variable names
* Select the correct Python operators
* Translate business rules into Boolean logic
* Update data using assignment operators
* Present technical results in a business-friendly format
* Use Python to support data-driven decision-making

The project also reinforced an important lesson for me as someone building skills in both Python and data analytics:

> Good programming starts with understanding the problem before writing the code.

---

## Project Constraints

This project was intentionally limited to Python fundamentals from Lessons 1 to 5.

### Concepts Used

* Variables
* Data Types
* Arithmetic Operators
* Assignment Operators
* Comparison Operators
* Logical Operators
* `print()` statements
* Basic output formatting

### Concepts Not Used

The following were intentionally excluded:

* `if` statements
* `for` and `while` loops
* Functions
* Lists
* Tuples
* Dictionaries
* Classes
* File handling
* Exception handling

These restrictions were part of the project requirements and helped reinforce the fundamentals before progressing to more advanced Python concepts.

---

## Repository Structure

```text
sales-forecasting-engine/
│
├── Sales Forecasting Engine.ipynb
├── README.md
│
└── images/
    ├── 01-variable-initialization.png
    ├── 02-weekly-revenue.png
    ├── 03-sales-forecast.png
    ├── 04-forecast-revenue.png
    ├── 05-inventory-update.png
    ├── 06-business-rules.png
    ├── 07-product-1-sales-report.png
    ├── 08-product-2-sales-report.png
    └── 09-product-comparison
```

The Jupyter Notebook contains the complete implementation, calculations, business logic, and output.

---

## Getting Started

### Prerequisites

You need:

* Python 3.x
* Jupyter Notebook or JupyterLab

No external Python libraries are required.

### Run the Project

Clone the repository:

```bash
git clone https://github.com/emmy0la/SALES-FORECASTING-ENGINE-FOR-BRIGHTMART-RETAIL-LTD
```

Navigate to the project folder:

```bash
cd SALES-FORECASTING-ENGINE-FOR-BRIGHTMART-RETAIL-LTD
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
Sales Forecasting Engine.ipynb
```

Run the notebook cells sequentially to reproduce the analysis and results.

---

## Future Improvements

This project intentionally focuses on Python fundamentals. With more advanced Python knowledge, the Sales Forecasting Engine could be extended to:

* Process multiple products automatically
* Accept user input dynamically
* Use conditional statements for automated recommendations
* Use loops to analyze larger product catalogs
* Store product data in lists or dictionaries
* Build reusable functions for calculations
* Read sales data from CSV or Excel files
* Use Pandas for structured data analysis
* Visualize sales trends with Matplotlib
* Build a more advanced forecasting model using historical sales data
* Create an interactive dashboard for management reporting

These improvements would move the project from a fundamental Python exercise toward a more complete business analytics application.

---

## Acknowledgments

This project was completed as part of the Python Study Group organized by SmartBizCrux Technologies.

Special thanks to Coach Timothy for designing an industry-focused learning experience that encourages learners to move beyond syntax and think about how programming can solve real business problems.

---

## Connect

I'm Emmanuel Olawumi, a Data Analyst and tech professional interested in Python, data analytics, business intelligence, digital transformation, and using data to solve real-world business problems.

I'm currently building my Python and data analytics portfolio through practical projects and continuous learning.

If you're interested in data, Python, analytics, or technology, feel free to connect with me and follow my journey.

https://www.linkedin.com/in/emmanuelolawumi/

---

## Project Status

Completed

Built as part of Python Study Group Case Study Project #3.

---

<div align="center">

If you found this project interesting, feel free to explore the repository and share your feedback.

Built with Python and a problem-solving mindset.

</div>

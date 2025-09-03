# E-Commerce Sales Performance Dashboard | Power BI Project

![E-Commerce Dashboard Banner](https://i.imgur.com/your-banner-image-url.png) This repository contains the details and key components of an interactive E-Commerce Sales Performance Dashboard built using Power BI. The project analyzes over 50,000 transaction records to provide actionable insights into customer behavior, product performance, and seasonal trends.

---

## 📊 Dashboard Preview

Here is a glimpse of the main dashboard page. The full report includes drill-through pages for detailed customer and product analysis.


*(It is highly recommended to replace the tag above with a screenshot or an animated GIF of your actual dashboard to showcase its interactivity.)*

---

## ✨ Key Features & Analysis

* **Real-Time Filtering:** The dashboard is fully interactive, allowing users to filter data by year, product category, and other dimensions to get real-time insights.
* **Advanced DAX Calculations:** Implemented complex DAX measures to calculate key business metrics, including:
    * Customer Lifetime Value (CLV)
    * Customer Retention Rate
    * Year-over-Year (YoY) Sales Growth
* **Customer Segmentation:** Utilized RFM (Recency, Frequency, Monetary) analysis to segment customers into actionable groups like "Champions," "Loyal Customers," and "At-Risk."
* **Interactive User Experience:** Enhanced the dashboard with drill-through pages for deep-dive analysis and custom tooltips for rich, contextual information on hover.
* **Data Modeling:** Built on a robust star schema data model to ensure performance and scalability.

---

## 🛠️ Technologies Used

* **Power BI:** For data visualization, modeling, and dashboard creation.
* **DAX (Data Analysis Expressions):** For creating custom measures and calculated columns.
* **Power Query:** For data extraction, transformation, and loading (ETL).
* **SQL:** (Mentioned if you used it for initial data extraction).
* **Data Modeling:** Star Schema design and implementation.

---

## 🚀 How to Use

1.  **Download the files:**
    * Download the `.pbix` file to view the full, interactive report in Power BI Desktop.
    * The sample data used for this project can be found here: `[Link to your sample data CSV file]`
2.  **Explore the Dashboard:** Open the `.pbix` file in Power BI Desktop. Interact with the slicers, charts, and drill-through features to explore the data.

---

## 💡 DAX Measures Showcase

Here are a few examples of the advanced DAX measures used in this project:

### Customer Lifetime Value (CLV)

This measure calculates the predicted total revenue a business can expect from a single customer account.

```dax
Customer Lifetime Value =
VAR AvgPurchaseFrequency = DIVIDE([Total Orders], [Total Customers])
VAR AvgPurchaseValue = DIVIDE([Total Sales], [Total Orders])
VAR CustomerLifetime = 365 / (1 - [Customer Retention Rate]) // Simplified lifetime in days
RETURN
    AvgPurchaseValue * AvgPurchaseFrequency * CustomerLifetime
```

### YoY Sales Growth

This measure calculates the percentage change in sales compared to the same period in the previous year.

```dax
YoY Sales Growth % =
VAR SalesCurrentYear = [Total Sales]
VAR SalesPreviousYear = CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Calendar'[Date]))
RETURN
    DIVIDE(SalesCurrentYear - SalesPreviousYear, SalesPreviousYear)
```

---

## 📞 Contact

Your Name – [pratham.r.108@gmail.com](mailto:pratham.r.108@gmail.com)

LinkedIn: [https://www.linkedin.com/in/pratham-r-348b60262/](https://www.linkedin.com/in/pratham-r-348b60262/)

Project Link: [https://github.com/yourusername/your-repo-name](https://github.com/yourusername/your-repo-name)

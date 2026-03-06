# Online Retail – RFM Customer Segmentation

End-to-end RFM analysis on the UCI Online Retail dataset (541,909 transactions) to segment customers and recommend targeted marketing strategies.

## Objective
Transform raw transactional data into actionable customer segments using Recency, Frequency, Monetary (RFM) scoring, and provide segment-specific marketing recommendations.

## Dataset
- Source: https://www.kaggle.com/datasets/ulrikthygepedersen/online-retail-dataset  
- Transactions: 541,909  
- Unique customers (after cleaning): 5,338  

## Tech Stack
- Python 3  
- Pandas  
- Matplotlib & Seaborn (visualizations)  

## Project Steps

1. **Data Cleaning**  
   - Filtered invalid Quantity & UnitPrice  
   - Removed rows missing CustomerID  
   - Parsed dates and aggregated per customer  

2. **RFM Calculation**  
   - Recency: days since last purchase  
   - Frequency: count of invoices  
   - Monetary: total revenue contributed  

3. **Scoring & Segmentation**  
   - Quantile-based scoring (1–5)  
   - Business-rule segments: Champions, Loyal, At Risk, Potential Loyalists, New, Lost, Other  

4. **Key Outputs**  
   - Segment distribution (2,283 Potential Loyalists, 1,018 At Risk, 306 Champions)  
   - Tailored marketing playbook for each segment  

## Main Findings
- Largest group: Potential Loyalists (recent but not yet frequent)  
- High-value risk: 1,018 At Risk customers needing urgent re-engagement  
- Elite group: only 306 true Champions — protect and grow  

cd online-retail-rfm
pip install -r requirements.txt
jupyter notebook "Online_Retail_RFM_Analysis.ipynb"

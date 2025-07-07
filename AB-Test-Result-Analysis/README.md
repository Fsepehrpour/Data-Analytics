# AB Test Analysis

This project analyzes an A/B test conducted by an e-commerce company to determine whether a newly designed landing page improves user conversion rates compared to the current page.

---

## Datasets

### **AB Test Dataset** (`ab_data.csv`)
- **Rows:** 294,480  
- **Columns:**
  - `user_id`: Unique identifier for each user
  - `timestamp`: Time of the experiment
  - `group`: Indicates whether the user was in the control or treatment group
  - `landing_page`: Indicates whether the user saw the old or new page
  - `converted`: 1 if the user converted (e.g., made a purchase), 0 otherwise

### **Country Dataset** (`countries.csv`)
- **Rows:** 290,586  
- **Columns:**
  - `user_id`
  - `country`: Country of the user

📎 **Link to the data:**  
https://www.kaggle.com/datasets/putdejudomthai/ecommerce-ab-testing-2022-dataset1

---

## Objective

To determine whether the new landing page leads to a statistically significant increase in conversion rate, and based on the results:
- **Implement** the new page,
- **Reject** the new page, or
- **Run the experiment longer**

---

## Methodology

### Steps:
1. **Cleaned and merged** the datasets.
2. **Removed mismatches** where control users saw the new page or treatment users saw the old page.
3. **Removed duplicate user entries** to avoid biased results.
4. **Merged** the user data with country information.
5. **Calculated conversion rates** for control and treatment groups.
6. **Conducted a two-proportion z-test** to determine statistical significance.
7. **Interpreted the results** and made recommendations.

---

## Conversion Rate Summary

| Group      | Landing Page | Users   | Conversions | Conversion Rate |
|------------|--------------|---------|-------------|------------------|
| Control    | Old Page     | 145,274 | 17,489      | **12.04%**       |
| Treatment  | New Page     | 145,312 | 17,264      | **11.88%**       |

---

## Two-Proportion Z-Test

### **Hypotheses:**
- **Null hypothesis (H₀):** There is no difference in conversion rates between control and treatment groups.
- **Alternative hypothesis (H₁):** There is a difference in conversion rates.

### **Test Results:**
- **Z-statistic:** 1.31  
- **P-value:** 0.189  

---

## Conclusion

Since the p-value (0.189) is greater than the typical significance level (0.05), we **fail to reject the null hypothesis**.  
This means the difference in conversion rates is **not statistically significant**.

### Recommendation:
The new landing page **does not significantly improve conversions**, and there's no strong evidence to support its implementation. The business may consider:
- Keeping the current page,
- Testing further design changes, or
- Running a longer experiment with a larger sample.

---

## Project Structure
```
AB-Test-Analysis
│
├── data
│   ├── ab_data.csv
│   └── countries.csv
│
├── AB-Test-Analysis.ipynb
└── README.md
```


---

## Tools & Libraries Used
- Python (Pandas, Matplotlib, Statsmodels)
- Jupyter Notebook
- A/B Testing, Hypothesis Testing, Z-Test

---

## License

This project is licensed under the MIT License. Feel free to use, modify, and distribute it.

---

## Contact

Feel free to contact via:
[LinkedIn](https://www.linkedin.com/in/fatemeh-sepehrpour-012982ba/)
Email:fatemeh.sepehrpour@proton.me


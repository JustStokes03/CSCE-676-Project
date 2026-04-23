# Online Retail II — Data Mining and Analysis Project

This project analyzes the Online Retail II dataset to understand customer purchasing behavior using both unordered frequent itemset mining and ordered sequential pattern mining. Because the dataset exhibits bursty, time‑clustered transactions and a sparse co‑occurrence matrix, the goal is to determine whether temporal structure reveals insights that unordered itemsets cannot 

👉 **Main deliverable:** [main_notebook.ipynb](main_notebook.ipynb)
🎥 **Project video:** https://youtu.be/SMOb3fE1g6M

---

## Research Question

Do sequential patterns reveal temporal or ordering structure that is missed by unordered frequent itemsets, particularly given the bursty transaction timing and sparse co-occurrence matrix?

---

## Data

**Dataset:** Online Retail II  
**Source:** UCI Machine Learning Repository  
https://archive.ics.uci.edu/

**Description:**  
A large‑scale transactional dataset containing invoice‑level retail purchases from a UK‑based online store.

**Preprocessing steps performed:**
- Removed rows with missing Invoice, StockCode, Quantity, or Customer ID  
- Removed negative quantities  
- Removed invoices starting with “C” (cancellations)  
- Converted InvoiceDate to datetime  
- Sorted by Customer ID and InvoiceDate  
- Built:
  - **baskets**: invoice → unique StockCodes  
  - **sequences**: customer → ordered list of baskets

---

## Reproducibility

This project was developed in **Google Colab**.

To reproduce the environment:

1. Open the repository in Colab  
2. Upload or open `requirements.txt`  
3. Install dependencies:

---
## Repository Structure

```
.
├── main_notebook.ipynb
├── Checkpoint_1.ipynb
├── Checkpoint_2.ipynb
├── requirements.txt
├── README.md
└── data/
```

---
## Key Dependencies and Versions

- pandas==2.2.2
- numpy==2.0.2
- matplotlib==3.10.0
- mlxtend==0.23.4
- prefixspan==0.5.2

---

## Results Summary

Sequential pattern mining uncovers temporal behavior — especially repeated purchases and multi‑step sequences — that unordered itemsets cannot represent.

---

## Author

**Jake**  
Graduate Student — Data Mining and Analysis  
Texas A&M University

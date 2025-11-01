# Flight Delay Prediction

## Project Overview

This project aims to build a **machine learning model (base model)** to predict the likelihood of flight delays based on weather and flight data. The project simulates a real-world business scenario where a travel booking website wants to improve customer experience by alerting users about possible delays **before** they book their flights.

By leveraging historical flight performance data from the **Bureau of Transportation Statistics (BTS)**, the goal is to train and evaluate predictive models that estimate whether a flight will be delayed at major U.S. airports.



## About the Dataset

The dataset, collected by the **Office of Airline Information (BTS)**, contains records of **domestic flights from 2014 to 2018** operated by major U.S. air carriers (each representing at least 1% of domestic passenger revenue).

It includes:

- Scheduled and actual departure/arrival times
- Origin and destination airports
- Airline carrier
- Flight distance
- Delay status and duration

The dataset spans **60 compressed monthly CSV files** covering five years of data.

The dataset can be downloaded via this [link](https://ucstaff-my.sharepoint.com/:f:/g/personal/ibrahim_radwan_canberra_edu_au/EhWeqeQsh-9Mr1fneZc9_0sBOBzEdXngvxFJtAlIa-eAgA?e=8ukWwa).
To view what are the features in the dataset, one can use this [link](https://www.transtats.bts.gov/Fields.asp?gnoyr_VQ=FGJ)


## Objective from Step 1-4

The main objective is to:

- Develop a **predictive model (base model)** that determines the likelihood of flight delays.
- Evaluate model performance using metrics such as **accuracy**, **precision**, **recall**, **F1-score**, and **ROC-AUC**.
- Analyse the results to see what can be improved


## Results Summary

The baseline **Logistic Regression model** achieved consistent performance across training, validation, and test datasets, showing no signs of overfitting.  
However, overall performance indicates that the model struggles with class imbalance.

| Metric        | Training | Validation | Test   |
| ------------- | -------- | ---------- | ------ |
| **Accuracy**  | 0.5903   | 0.5888     | 0.5889 |
| **Precision** | 0.2809   | 0.2792     | 0.2803 |
| **Recall**    | 0.6100   | 0.6064     | 0.6115 |
| **F1-Score**  | 0.3846   | 0.3824     | 0.3844 |
| **ROC-AUC**   | 0.6341   | 0.6321     | 0.6334 |

**Interpretation:**

- The model generalizes well across all datasets (no overfitting observed).
- **Low precision (about 28%)** and **moderate recall (around 61%)** suggest the model produces many false positives while missing some actual delays.
- This provides a **useful baseline**, but further improvement is needed through **feature engineering** and **advanced models** such as Random Forest.


## How to run

1. **Clone this project**

```bash
   git clone https://github.com/manilesrun/final_project_u3273786.git
   cd final_project_u3273786
```

2. **Download and prepare the dataset**

- One needs to download the dataset via the link provided above.
- After downloading, create a folder named **`datasets`** in the project directory and place all the **ZIP files** into this folder.

3. **Install requirements**

- Open the `requirements.txt` file and use **pip** to install all the listed dependencies.

4. **Usage**
   - Launch Jupyter Notebook:
     ```bash
     jupyter notebook
     ```
   - Open the notebook file named **`onpremises (1).ipynb`** and run all cells sequentially to reproduce the results.

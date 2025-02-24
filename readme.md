# Credit Risk Modeling Project

Welcome to the **Credit Risk Modeling** project! This repository contains Jupyter notebooks and related resources for end-to-end credit risk modeling, including data preparation, Probability of Default (PD) modeling, Loss Given Default (LGD) & Exposure at Default (EAD) estimation, and model monitoring.

---

## Repository Structure

```
k-jaswanth-kumar-ccrm/
├── Credit_Risk_Data_Prep.ipynb
├── Credit_Risk_LGD_and_EAD.ipynb
├── Credit_Risk_PD_Model.ipynb
└── Credit_Risk_PD_Monitoring.ipynb
```

Below is a brief description of each notebook:

1. **Credit_Risk_Data_Prep.ipynb**  
   - **Purpose**: Preprocesses raw loan data, handles missing values, encodes categorical variables, and engineers new features essential for modeling.  
   - **Key Steps**:
     - Reading the raw dataset (`loan_data_2007_2014.csv`).
     - Handling warnings and mixed data types.
     - Exploratory Data Analysis (EDA) to understand distributions, missing data, etc.
     - Cleaning and feature engineering (e.g., `emp_length_int`, `term_int`, date transformations, creation of dummy variables).
     - Preparing a final dataset suitable for subsequent modeling steps.

2. **Credit_Risk_LGD_and_EAD.ipynb**  
   - **Purpose**: Provides methods to estimate Loss Given Default (LGD) and Exposure at Default (EAD).  
   - **Key Steps** (high-level, as the full code is not displayed in this snippet):
     - Data analysis to segment defaulted vs. non-defaulted accounts.
     - Methods for calculating and modeling LGD.
     - Techniques for EAD estimations (e.g., utilization, credit exposure thresholds).
     - (Potentially includes) stress testing scenarios or simulations.

3. **Credit_Risk_PD_Model.ipynb**  
   - **Purpose**: Builds a Probability of Default (PD) model using the preprocessed dataset.  
   - **Key Steps**:
     - Splitting data into training and test sets.
     - Feature selection, Weight of Evidence (WoE) calculations, Information Value (IV) checks.
     - Model training (likely logistic regression or another classifier).
     - Performance evaluation (e.g., AUC, confusion matrix, etc.).
     - Documentation of model outputs and insights.

4. **Credit_Risk_PD_Monitoring.ipynb**  
   - **Purpose**: Demonstrates how to monitor the PD model over time.  
   - **Key Steps**:
     - Setting up monitoring metrics (e.g., population stability index (PSI), drift analysis).
     - Tracking model performance and stability in production.
     - Generating alerts or thresholds if model performance deviates.

---

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/k-jaswanth-kumar-ccrm.git
cd k-jaswanth-kumar-ccrm
```

### 2. Set Up a Virtual Environment (Optional but Recommended)

Create and activate a virtual environment using [conda] or [venv] to avoid dependency conflicts:

```bash
# Using conda
conda create -n credit-risk python=3.9
conda activate credit-risk
```

### 3. Install Dependencies

Install the libraries required to run the notebooks. Typically, these may include:

- pandas  
- numpy  
- scikit-learn  
- matplotlib  
- seaborn  
- jupyter

You can install them via:

```bash
pip install -r requirements.txt
```

*(If a `requirements.txt` file is not provided, please ensure you install the above libraries manually.)*

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open each notebook in your browser to run the code and explore results.

---

## Usage

1. **Data Ingestion**  
   - Ensure you have the dataset (`loan_data_2007_2014.csv`) in the correct folder (e.g., `Dataset/` or adjust paths as needed inside the notebook).

2. **Run the Notebooks in Order**  
   - **`Credit_Risk_Data_Prep.ipynb`** →  
     Prepare/clean the data and produce the final dataset for modeling.
   - **`Credit_Risk_PD_Model.ipynb`** →  
     Train, evaluate, and interpret the PD model using the preprocessed dataset.
   - **`Credit_Risk_LGD_and_EAD.ipynb`** →  
     Estimate LGD & EAD, often run after you have clarity on default definitions and data segments.
   - **`Credit_Risk_PD_Monitoring.ipynb`** →  
     Illustrate how to monitor the deployed PD model over time.

3. **Adjust Hyperparameters & Scenarios**  
   - Feel free to modify hyperparameters, feature engineering, or threshold logic in the notebooks to suit your project’s needs.

---

## Folder/Notebook Details

- **`Dataset/`**  
  Contains or expects the raw data file `loan_data_2007_2014.csv`. *(Not included in the repository if file size or license constraints apply.)*  
- **`Credit_Risk_Data_Prep.ipynb`**  
  Detailed data exploration and preprocessing methods.  
- **`Credit_Risk_LGD_and_EAD.ipynb`**  
  Illustration and formulas for LGD and EAD.  
- **`Credit_Risk_PD_Model.ipynb`**  
  Main model building with logistic regression or similar technique, along with WoE and IV.  
- **`Credit_Risk_PD_Monitoring.ipynb`**  
  Sets up monitoring frameworks to track model performance in production.

---

## Contributing

Contributions, suggestions, and improvements to this project are welcome. To contribute:

1. **Fork** the project.
2. **Create** a new branch (`git checkout -b feature/your-feature`).
3. **Commit** your changes (`git commit -am 'Add new feature'`).
4. **Push** to your branch (`git push origin feature/your-feature`).
5. **Create** a new Pull Request.

---

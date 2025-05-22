# Digital Twin WWTP Data Science Project

A student–researcher collaboration under the **Data Science Lectoraat** at HZ University of Applied Sciences. Our mission is to build a **digital twin** of the Waste Water Treatment Plant (WWTP) to help stakeholders operate more efficiently and anticipate unforeseen events, following the CRISP-DM framework.

---

## Repository Structure

```
.
├── main_notebook.ipynb    # Comprehensive Jupyter notebook covering all phases
├── requirements.txt       # Python dependencies
├── .gitignore             # Excludes raw data files and outputs
├── README.md              # This file
└── LICENSE                # MIT License
```

> **Note:** No raw data files are stored in this repository.  
> Please download the `Complete_2023.csv` dataset from the project portal (or contact the data owner), create a `data/` directory at the root of this repo, and place the file there before running the notebook.

---

## Project Overview

- **Business Goal:**  
  Help policymakers understand and control the WWTP’s chemical processes under varying inflow and weather conditions.

- **Technical Focus:**  
  Model **Phase 2 chemical transformations**, with a particular emphasis on **nitrate** levels, to predict both water-quality indicators and equipment states (e.g., blower positions).

- **Approach:**  
  Follow the **CRISP-DM** lifecycle:
  1. **Business Understanding** – define objectives with stakeholders  
  2. **Data Understanding & Preparation** – exploratory data analysis, missing-value handling, feature engineering  
  3. **Modeling** – regression and tree-based models targeting nitrate prediction  
  4. **Evaluation & Deployment** – interpret results, validate models, recommend integration steps

---

## main_notebook.ipynb

A single, self-contained Jupyter notebook that walks through:

1. **Data Loading & EDA**  
   - Summary statistics, distributions, outlier detection, autocorrelation checks  
2. **Preprocessing**  
   - Imputation of missing values, scaling, encoding, lag-feature engineering for time series  
3. **Modeling**  
   - Linear models (Ridge, Lasso) and ensembles (Random Forest, Gradient Boosting) focused on nitrate level prediction  
4. **Evaluation**  
   - MAE, RMSE, R² metrics, residual analysis, feature‐importance interpretation  
5. **Conclusions & Next Steps**  
   - Actionable insights for WWTP control and suggestions for further refinement  

---

## Getting Started

1. **Clone the repository**  
   ```bash
   git clone https://github.com/your-username/dtw-wwtp-ds.git
   cd dtw-wwtp-ds
   ```

2. **Set up a Python environment**  
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```

3. **Download the data**  
   - Obtain `Complete_2023.csv` from the project portal  
   - Create a `data/` directory in the repo root and place the file there  

4. **Launch the notebook**  
   ```bash
   jupyter lab main_notebook.ipynb
   ```

---

## Contributing

1. Fork the repository  
2. Create a feature branch  
   ```bash
   git checkout -b feature/YourFeature
   ```
3. Make your changes and document them in the notebook  
4. Commit and push  
   ```bash
   git commit -m "Add feature"
   git push origin feature/YourFeature
   ```
5. Open a Pull Request  

Please document all analysis choices and assumptions clearly in the notebook.


## License

This project is licensed under the [MIT License](LICENSE).

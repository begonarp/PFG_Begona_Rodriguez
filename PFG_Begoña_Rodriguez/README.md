# Cement Industry Production Forecasting in Spain

This project analyzes and forecasts industrial production in the cement sector across Spain's autonomous communities. It combines economic and environmental variables to train several predictive models and assess their performance regionally and through the years.

## Project Structure

PFG_Begoña_Rodriguez/
├── Notebooks/                      
│   ├── Modelling_Production.ipynb
│   └── Production_Calculation.ipynb
├── Data/                           
│   ├── Initial_Dataframes/                    
│   │   ├── emissions.xlsx
│   │   ├── factories.xlsx
│   │   └── production.xlsx
│   └── Final_Dataframes/                      
│       ├──Errors/                
│       │   ├── ARIMA/         
│       │   │   ├── errores_arima_df.xlsx
│       │   │   ├── errors_arima_years.xlsx
│       │   │   └── errors_arima.xlsx
│       │   ├── Naive1/
│       │   │   ├── errores_naive_mean_pib_df.xlsx
│       │   │   ├── errors_naive1_years.xlsx
│       │   │   └── errors_n1.xlsx
│       │   ├── Naive2/
│       │   │   ├── errores_naive_tendency_pib_df.xlsx
│       │   │   ├── errors_n2.xlsx
│       │   │   └── errors_naive2_years.xlsx
│       │   ├── NN/
│       │   │   ├── errores_nn_pib_df.xlsx
│       │   │   ├── errors_nn_years.xlsx
│       │   │   └── rerrors_nn.xlsx
│       │   └── LinearRegression/          
│       │       ├── errores_regresion_gdp_df.xlsx
│       │       ├── errores_regression_df.xlsx
│       │       ├── errors_lr_df.xlsx
│       │       ├── errors_lr_gdp_df.xlsx
│       │       ├── errors_lr_years_gdp_df.xlsx
│       │       └── errors_lr_years_no_gdp.xlsx
│       └── Modelled/              
│           ├── ccaa_final.xlsx
│           └── gdp_ccaa.xlsx
│
├── README.md
└── .gitignore

## Models Used

	1.Naïve Mean Model

	2.Rolling Average (3 years)

	3. Linear Regression with GDP

	4. Neural Network (PyTorch)

	5. ARIMA with Leave-One-Out Cross Validation

## Metrics to assess performance

	1. MedAPE
	
	2. RMSE

## Execution Notice

While all code and datasets are available in this repository, **it is strongly recommended to run the project in [Google Colab](https://colab.research.google.com/)** due to:

- Integration with Google Drive for file access
- Compatibility with libraries such as `gdown`, `google.colab`, and `pydrive2` used in the notebooks
- Preinstalled environments that simplify execution of packages like `pmdarima`, `statsmodels`, or `scikit-posthocs`

Running locally (e.g., in Visual Studio Code or Jupyter) **may require manual installation and adjustment of packages** and code to handle local file paths.

## Requirements (for local execution)

If you still prefer to run locally, install the required packages:

```bash
pip install numpy pandas matplotlib seaborn torch scikit-learn statsmodels pmdarima scikit-posthocs tqdm


### Machine Learning Model for Predicting MIL-101(Cr) Synthesis Outcomes

#### Overview
The machine learning model predicts the outcome of MIL-101(Cr) synthesis based on input variables, which include the type of nucleating agent, the amount of nucleating agent, the amount of solubilizing agent (GdmCl), and the synthesis temperature. The reaction involves using chromium nitrate ((CrN)3O3) and BDC (terephthalic acid) in a 1:1 ratio, and the reaction time is assumed to be as long as necessary (up to one week). The output variable is the synthesis result, categorized as either successful MIL-101(Cr) synthesis or synthesis failure (no product or amorphous product)
All model training is based on the dataset of MIL-101(Cr) synthesis conditions and outcomes (`MIL_101_Cr_data.csv`).

#### How to Use the Program
There are two ways to use the program:

1. **Using Anaconda and Jupyter Notebook:**
   - **Install Anaconda** and set up a Python virtual environment.
     - Example: `conda create -n env_name`
   - **Activate the environment:**
     - Example: `conda activate env_name`
   - **Install the required packages:** notebook, numpy, pandas, scikit-learn, and catboost.
     - Example: `conda install numpy pandas`
   - Launch Jupyter Notebook from Anaconda, download, and unzip the provided zip file, and upload it to Jupyter Notebook. Then, open and run the `Jupyter_pre.ipynb` file.

2. **Using the Executable File:**
   - If you prefer not to install Anaconda or find the above method challenging, you can unzip the provided file and run the `app.exe` file to easily change conditions and predict the outcome of MIL-101(Cr) synthesis. Ensure that the model file `CatBoost_model.joblib` is in the same directory as the executable program during execution.

#### Important Notes
- For optimal prediction results, it is recommended to adjust the synthesis conditions within the fowing ranges:
  - `{n-cry:0-5; n-GdmCl:0-40; V-H20:0-50; emperature:100-220}`
  
- If you wish to retrain the model, simply replace or add data to the dataset file (`MIL_101_Cr_data.csv`), select the desired model for retraining, save the model, and update the model used in the `Jupyter_pre.ipynb` file accordingly.
.

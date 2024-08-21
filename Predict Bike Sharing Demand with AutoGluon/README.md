## Predict Bike Sharing Demand with AutoGluon

**Project Overview**:  
This project aims to predict bike-sharing demand using the AutoGluon library. It is part of the Kaggle competition, where the goal is to train several models and optimize their performance using Tabular Prediction on the provided dataset. The problem of predicting bike-sharing demand is relevant to many businesses, including Uber, Lyft, and DoorDash, as it helps prepare for service spikes and enhances customer experience.

### Objective:
To demonstrate the ability to use AutoGluon for training and optimizing machine learning models to predict bike-sharing demand and achieve a rank in the Kaggle competition.

### Key Files

1. **`notebook.ipynb`**:  
   A Jupyter notebook that walks through the entire process of loading data, training models with AutoGluon, and evaluating the results. The notebook includes:
   - Data Loading and Preprocessing
   - Model Training with AutoGluon
   - Hyperparameter Tuning
   - Model Evaluation
   - Submission to Kaggle

2. **`data/`**:  
   A directory containing the dataset files used in the competition. Ensure to download and place the data files from Kaggle into this folder.

3. **`submission.csv`**:  
   The final submission file for the Kaggle competition, generated from the best-performing model.

4. **`report.md`**:  
   A markdown file summarizing your findings, insights, and optimizations during the project. This report can be shared publicly on Kaggle or your personal page as a showcase of your work.

### Setup Instructions

To replicate this project, follow these steps:

1. **Clone the repository**:  
   ```
   git clone <repository_url>
   ```
   
2. **Install dependencies**:  
   Ensure you have Python and the required packages installed. Use the following command to install dependencies:
   ```
   pip install -r requirements.txt
   ```

3. **Download the dataset**:  
   Download the dataset from the [Bike Sharing Demand Kaggle competition](https://www.kaggle.com/c/bike-sharing-demand) and place it in the `data/` directory.

4. **Run the Jupyter Notebook**:  
   Open `notebook.ipynb` in Jupyter and follow the steps to train and evaluate your models.

5. **Submit to Kaggle**:  
   After generating predictions, use the `submission.csv` file to submit your results to the Kaggle competition.

### Results

The results of your predictions, including your ranking on Kaggle, can be found in the `report.md` file. This file also contains any optimizations and insights gained during the project.

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

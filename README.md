# Parameter Optimization using SVM
### Submitted by: CHELSI
### Group: 3CS6
### Roll No: 102117161

This project demonstrates the parameter optimization using Support Vector Machine (SVM).
### Dataset
https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success      
Student Dropout & Academic Success Prediction dataset having 4424 instances and 37 features.

### Methodology
1. **Data Preprocessing:**        
A. The dataset is loaded from a CSV file.      
B. Column names are standardized by removing leading/trailing whitespaces, converting to lowercase, and replacing spaces with underscores.      
C. Missing values are checked and handled if present.      
2. **Label Encoding:**  The target variable is encoded using LabelEncoder to convert categorical labels into numeric format.      
3. **Feature Scaling:** Standardization is applied to the feature variables using StandardScaler to bring them onto the same scale.      
4. **Model Training and Evaluation:** The dataset is split into training and testing sets using a 70-30 split and this process is repeated 10 times with different random states to generate multiple samples for cross-validation.    
For each sample, SVM models with different kernels (linear, poly, rbf, sigmoid) are trained with randomly chosen hyperparameters (kernel, C and gamma) using a custom fitness function based on accuracy score.  
The best performing model (with the highest accuracy) for each sample is recorded along with its hyperparameters.
A DataFrame (result) is created to store the results (sample number, best accuracy, best kernel, best C value, best gamma value).    
Finally, the model with the best accuracy across all samples is selected and its learning curve is plotted to visualize the convergence of accuracy with respect to the number of training iterations.      
5. **Observations:**      
Best Accuracy score is obtained as 0.54 for sample 7 and parameters: Kernel= Linear, C=2.95, Gemma=0.43      
![image](https://github.com/cdr0101/Parameter-Optimisation/assets/117757108/15ad55a9-3bf4-4449-8b93-b9f640357e31)

![image](https://github.com/cdr0101/Parameter-Optimisation/assets/117757108/0cecf887-0ecf-46d9-8d52-e76cf8f16bf1)


## Files Included

- `predict_student_dropout&academic_success.csv`: CSV file containing the dataset.
- `parameterOptimization.ipynb`: Colab Notebook containing the code.
- `README.md`: This README file providing an overview of the project.

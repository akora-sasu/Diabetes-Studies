# Diabetes-Studies
# Unravelling the Diabetes Triggers Among Adults in the United States of America
# 1 Introduction
Diabetes is a widespread metabolic disorder that disrupts the body's ability to manage blood sugar. It can lead to complications such as heart disease, vision loss, lower limb amputation, and kidney disease. Strategies such as losing weight, eating healthily, and being active can help mitigate the harms of this disease. According to the Centers for Disease Control and Prevention, as of 2018, 34.2 million Americans have diabetes and 88 million have prediabetes. The total costs of diagnosed diabetes, undiagnosed diabetes, and prediabetes approach $400 billion annually. 
# 2 Data 
The data is obtained from the Behavioral Risk Factor Surveillance System (BRFSS) survey conducted by the CDC in 2015. The clean dataset has 70,692 survey responses with a 50-50 split between respondents with no diabetes and those with prediabetes or diabetes. The target variable "Diabetes_binary" has 2 classes, and the dataset has 21 feature variables.

Figure 1: Plot of histograms for all features
![image](https://github.com/user-attachments/assets/b4fb6442-16ad-440a-a816-09de456606fc)

Figure 2: Principal component analysis for features and target parameters
![image](https://github.com/user-attachments/assets/5348d115-47e6-44d3-92ce-8c0fc8cc5caf)

# 3 Methods 
The overlap observed in our PCA suggests a limited linear separability of our cohorts(diabetic or not). using a linear model (such as Logistic Regression) might struggle to accurately classify the data. As such, a more complex model that can capture non-linear relationships or interactions between features is typically better suited.

Random Forest which is an ensemble of decision trees that mitigates the overfitting problem of a single tree by averaging predictions from multiple trees is used. This is because is robust to overfitting, handles non-linear data, and works well with categorical and numerical features.

Cons: It is less interpretable than a single decision tree and can be computationally intensive.

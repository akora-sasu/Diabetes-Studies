# Diabetes-Studies
# Unravelling the Diabetes Triggers Among Adults in the United States of America
# 1 Introduction
Diabetes is a widespread metabolic disorder that disrupts the body's ability to manage blood sugar. It can lead to complications such as heart disease, vision loss, lower limb amputation, and kidney disease. Strategies such as losing weight, eating healthily, and being active can help mitigate the harms of this disease. According to the Centers for Disease Control and Prevention, as of 2018, 34.2 million Americans have diabetes and 88 million have prediabetes. The total costs of diagnosed diabetes, undiagnosed diabetes, and prediabetes approach $400 billion annually. 
# 2 Data 
The data is obtained from the Behavioral Risk Factor Surveillance System (BRFSS) survey conducted by the CDC in 2015. The clean dataset has 70,692 survey responses with a 50-50 split between respondents with no diabetes and those with prediabetes or diabetes. The target variable "Diabetes_binary" has 2 classes, and the dataset has 21 feature variables.

## Figure 1: Plot of histograms for all features
![image](https://github.com/user-attachments/assets/b4fb6442-16ad-440a-a816-09de456606fc)

## Figure 2: Principal component analysis for features and target parameters
![image](https://github.com/user-attachments/assets/dd356616-b4b2-4dd2-83ce-f66eed95cde5)

# 3 Methods 
The overlap observed in our PCA suggests a limited linear separability of our cohorts(diabetic or not). using a linear model (such as Logistic Regression) might struggle to classify the data accurately. As such, a more complex model that can capture non-linear relationships or interactions between features is typically better suited.

Random Forest is an ensemble of decision trees that mitigates the overfitting problem of a single tree by averaging predictions from multiple trees. This is because it is robust to overfitting, handles non-linear data, and works well with categorical and numerical features. One disadvantage of the model is that it is less interpretable than a single decision tree and can be computationally intensive.
# 4 Insights 
## Table 1: Model performance matrix
![image](https://github.com/user-attachments/assets/294abd79-6a33-46bd-ba87-5654b859727c)
The Random Forest model achieved a 74% accuracy, showing reasonable predictive power. The classification report shows a balanced f1-score of 0.74 for both diabetic and non-diabetic cases, indicating consistent performance across both classes with no significant bias 

## •	Feature Importance and PDP Analysis:
## Figure3: Features and their contribution to diabetes incidences 
![image](https://github.com/user-attachments/assets/ed3419c6-5b78-42e5-8372-8e7863087384)

The model identified key predictors of diabetes (see Figure 3), and Partial Dependence Plots (PDP) helped understand their impact on diabetes risk (see Figure 4).
The PDPs provided insights into how changes in the top ten most important features affect diabetes risk, revealing complex non-linear relationships with certain health indicators, and underscoring the complexity of the disease predictors.

## Figure 4: Partial dependence plots (PDP) of the top 10 important features
![image](https://github.com/user-attachments/assets/edf4c6ea-2037-4a43-b4c9-c335798d7c1a)

# 5. Recommendations
#     Public Health Initiatives:
Targeted public health initiatives should address the major predictors of diabetes, focusing on modifiable risk factors like weight management, diet, and physical activity to reduce the incidence of diabetes.
#     Refinement of Predictive Models:
The current model performs well, but refining it and exploring additional features could improve its predictive accuracy. Adding more detailed health data, like genetic markers or long-term lifestyle factors, may enhance the model's ability to predict diabetes onset.
#     Personalized Interventions:
The non-linear relationships observed in the PDPs suggest that personalized interventions could be more effective than one-size-fits-all approaches. Healthcare providers should consider individual patient data when crafting prevention and treatment strategies, ensuring that interventions are tailored to the specific risk profile of each individual.

# 5. Conclusion
This analysis offers valuable insights into the factors driving diabetes risk and highlights the potential for data-driven public health strategies. By leveraging machine learning, we can better understand diabetes complexities and take proactive steps to address it at individual and population levels. 


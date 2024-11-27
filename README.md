# Machine-learning-project-
Analysis of Risky Alcohol Consumption Among Canadian High School Students
The Canadian Student Tobacco, Alcohol, and Drugs Survey (CSTADS), conducted by Health Canada and CCI Research Inc. from 2021 to 2022, examines the behaviors and risk factors associated with substance use among Canadian high school students. The dataset, publicly available through Canada’s Open Data repository, includes anonymized responses from ~60,000 students. Key areas of focus include alcohol, tobacco, cannabis use, and experiences with bullying, both as victims and perpetrators.

**Objective**
The goal of this analysis is to:
  Assess the accuracy of machine learning models in predicting high-risk alcohol consumption among high school students.
  Identify the strongest predictors of high-risk behavior from categories such as bullying, demographics, and substance use.

**Research Methodology**
  Target Variable: The primary variable, ALC_050, measures the frequency of consuming 5+ alcoholic drinks in a single sitting over the past year. Responses were transformed into binary classes:
  Low Risk: Responses indicating "never" or "less than once a month."
  High Risk: Responses indicating "once a month or more."

**Feature Categories:**
  Demographics,
  Victimization of bullying,
  Perpetration of bullying,
  Tobacco use,
  Cannabis use,

**Machine Learning Models:**
  Logistic Regression,
  Decision Tree Classifier.

**Preprocessing Steps:**
  Invalid or missing responses were removed using a custom DropNull function.
  Features were organized into predefined categories, cleaned, and transformed using drugfeatures.py for easy modular analysis.

**Evaluation Metrics**:
  Accuracy scores,
  Confusion matrices,
  Classification reports,
  Results.

**Initial Model Performance**:
  Logistic Regression and Decision Tree Classifier achieved 75% accuracy with bullying-related features, while substance use features performed poorly (accuracy < 70%).
  Demographic variables performed moderately well, with accuracies ranging from 72% to 74%.

**Principal Component Analysis (PCA):**
  PCA was applied to reduce feature dimensions.
  PCA improved feature clarity but had minimal impact on model accuracy. However, it showed slight reductions in performance for substance use feature sets.

**Revised Binary Classes:**
  Adjusting the binary threshold for high-risk behavior (e.g., redefining "high risk" to exclude infrequent consumption) improved accuracy:
  Bullying-related features: 85% accuracy
  Demographics: 83% accuracy
  Substance use features continued to perform poorly, suggesting weaker correlations.
  Discussion

**Key Findings:**
  Bullying-related variables (both victimization and perpetration) consistently outperformed other feature sets as predictors of high-risk drinking.
  Demographic factors also showed moderate predictive power.
  Substance use variables (tobacco and cannabis) were weak predictors, suggesting that their correlation to alcohol misuse is less direct in this dataset.

**Impact of Preprocessing:**
  Feature selection and preprocessing decisions significantly influenced accuracy.
  Model performance was more dependent on selecting meaningful predictors than on the choice of machine learning model.

**Practical Implications:**
  Insights from bullying and demographic predictors could inform targeted interventions and policy decisions for addressing high-risk alcohol consumption among youth.

**Conclusion**

This analysis highlights the importance of:
  Selecting appropriate features during the preprocessing phase.
  Adjusting target variable definitions to reduce bias.
  Recognizing the limitations of certain predictors (e.g., substance use) in complex behavioral analyses.
  By focusing on bullying and demographic variables, machine learning models can achieve higher accuracy in predicting risky alcohol consumption, providing valuable insights for stakeholders working to address youth substance abuse.

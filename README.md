# email-analysis
Objective: This notebook analyzes email campaign data to evaluate performance and apply uplift modeling to improve click-through rates (CTR).

Dataset Overview:
email_table: Metadata about sent emails
email_opened_table: Records of email opens
link_clicked_table: Records of link clicks

Key Metrics Calculated:
Open Rate and CTR (baseline performance)
Model Performance Metrics (classification report & ROC AUC)
Simulated CTR Improvements using a predictive model
Uplift Modeling results by user segments

Modeling Approach:
Logistic Regression to predict clicks
Uplift Tree Classifier (from causalml) to estimate differential treatment effect

Important Notes:
control_name='0' must be passed as a string
treatment column values must be strings ('0' or '1')
Ensure the uplift_score used for segmentation is 1D ([:,1] for treatment effect)

Potential Enhancements:
Add hyperparameter tuning
Use other uplift models like UpliftRandomForestClassifier
Run A/B simulations on different email segments

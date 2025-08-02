NSAP Scheme Classification Model
This project aims to build and deploy a multi-class classification model that predicts the appropriate National Social Assistance Programme (NSAP) scheme for applicants based on their demographic and socio-economic data. The model will assist government agencies in automating and streamlining the scheme allocation process, ensuring that eligible beneficiaries receive timely support.

Problem Statement
The National Social Assistance Program (NSAP) by the Government of India provides financial aid to vulnerable groups (elderly, widows, persons with disabilities) from Below Poverty Line (BPL) households. Manually verifying applications and assigning schemes is error-prone and slow. This project builds an AI model to automate and optimize this process.

Dataset
Dataset Source: AI Kosh - NSAP Pension Data

Contains district-wise demographic and socio-economic details.

Target variable: NSAP Scheme Type.

Key Features: Age, Gender, Disability Status, Marital Status, BPL Status, District, etc.

Technology Stack
Component	Technology
Cloud Platform	IBM Cloud Lite
Notebook Environment	IBM Watson Studio (Lite Plan)
Model Training	Python (Scikit-learn / TensorFlow / AutoAI)
Data Storage	IBM Cloud Object Storage
Model Deployment	IBM Watson Machine Learning (Lite Plan)
API Service	IBM Cloud Functions (Lite Plan)

nsap-scheme-classification/
├── data/
│   └── nsap_dataset.csv
├── notebooks/
│   └── NSAP_Model_Development.ipynb
├── deployment/
│   └── NSAP_API_Deployment.ipynb
├── README.md
└── requirements.txt
Steps to Run the Project
1. Set up IBM Cloud Lite Account
Sign up at IBM Cloud.

Create a Watson Studio Lite instance.

Create a Cloud Object Storage Lite instance.

Create a Watson Machine Learning Lite instance.

2. Upload Dataset to Cloud Object Storage
Go to IBM Cloud Console → Cloud Object Storage → Buckets → Create Bucket.

Upload the NSAP dataset to the bucket.

3. Model Development in Watson Studio
Launch Watson Studio.

Create a new Project and attach Cloud Object Storage.

Create a Notebook and select Python 3.x environment.

Load the dataset from Cloud Object Storage.

Perform Data Cleaning, Feature Engineering, and Exploratory Data Analysis (EDA).

Train a Multi-class Classification Model (e.g., Random Forest, XGBoost, or AutoAI experiment).

Evaluate model using accuracy, F1-score, and confusion matrix.

4. Deploy Model with Watson Machine Learning
Save the trained model to Watson Machine Learning Repository.

Create a Deployment Space and deploy the model as a Web Service Endpoint (REST API).

5. Create API Service with IBM Cloud Functions
Set up an IBM Cloud Functions Action that calls the WML API to get predictions.

Secure the API with IAM API keys or token authentication.

6. Test API and Integrate
Send sample input data via REST API calls.

Receive predicted NSAP scheme in the response.

Requirements
Create a requirements.txt with the following:

nginx
Copy
Edit
pandas
scikit-learn
numpy
ibm-watson-machine-learning
requests
matplotlib
seaborn
Evaluation Metrics
Accuracy

Precision / Recall per Class (Scheme)

Macro / Weighted F1-Score

Confusion Matrix Visualization

IBM Cloud Free Tier Limits Considerations
Lite plans have resource limitations (5GB storage, capped API calls per month).

Ensure dataset size and API calls are optimized for Lite usage.

AutoAI runs are limited; manual training preferred if exceeded.

Future Enhancements
Add more granular features like income level, family size.

Incorporate a feedback loop where incorrect predictions can be corrected and model retrained.

Build a user-friendly frontend (optional) using IBM Cloud Foundry or static site.

Authors
[Mouna M]

# WeatherWizard-DS

**Note:** This is an ongoing project.

## Table of Contents

- [Summary](#summary)
- [Overview](#overview)
- [Directory Structure](#directory-structure)
- [Files Description](#files-description)
- [Project Workflow](#project-workflow)
  - [1. Imports](#1-imports)
  - [2. Dataset Generation](#2-dataset-generation)
  - [3. Feature Engineering](#3-feature-engineering)
  - [4. Feature Split](#4-feature-split)
  - [5. Model Setup](#5-model-setup)
  - [6. Model Registry](#6-model-registry)
  - [7. Deployment](#7-deployment)
  - [8. Invocation](#8-invocation)
- [AWS Services Used](#aws-services-used)
- [Future Work](#future-work)
- [License](#license)
- [Contributing](#contributing)
- [Contact](#contact)

## Summary

WeatherWizard-DS is a data science project focused on leveraging AWS services to predict current weather conditions based on user-provided geographical coordinates and the current time. The project utilizes a variety of AWS services, including SageMaker for model training and deployment, S3 for data storage, CloudFront for distribution, and DynamoDB and API Gateway for additional functionalities. The goal is to create an accurate and scalable weather prediction system.

## Overview

WeatherWizard-DS integrates several AWS components to deliver a weather prediction model that is trained on synthetic data. It involves generating a dataset, engineering features, training a model, and deploying it as a serverless endpoint for real-time predictions.

## Directory Structure

.\WeatherWizard-DS

├── .ipynb_checkpoints/

├── Feature_Engineering.ipynb

├── LICENSE

├── README.md

├── test.csv

└── train.csv

## Files Description

- `Feature_Engineering.ipynb`: Jupyter Notebook for feature engineering, transforming raw data into features suitable for model training.
- `LICENSE`: License file for the repository.
- `README.md`: This file, containing information about the project.
- `test.csv`: CSV file containing test data.
- `train.csv`: CSV file containing training data.

## Project Workflow

### 1. Imports

Imports necessary libraries and modules for data processing, model training, and interaction with AWS services.

### 2. Dataset Generation

Generates a synthetic dataset with weather conditions and geographical coordinates. The dataset is used to train and evaluate the weather prediction model.

### 3. Feature Engineering

Transforms the dataset by converting UNIX timestamps to human-readable date and time features, and performs feature extraction.

### 4. Feature Split

Splits the dataset into training and testing sets, and saves them as CSV files. Uploads these files to an S3 bucket for use in model training.

### 5. Model Setup

Configures and trains an XGBoost model using AWS SageMaker. The training data is sourced from the S3 bucket, and the trained model is saved back to S3.

### 6. Model Registry

Registers the trained model in the SageMaker Model Registry and approves the model for deployment.

### 7. Deployment

Deploys the model as a serverless endpoint using AWS SageMaker. Configures the endpoint for real-time inference.

### 8. Invocation

Demonstrates how to invoke the deployed model endpoint to get weather predictions based on new input data. Includes example code for making predictions and interpreting the results.

## AWS Services Used

- **S3**: Storage for dataset and model artifacts.
- **SageMaker**: Training and deploying the machine learning model.
- **CloudFront**: Distribution of model and data.
- **DynamoDB**: Storing and querying metadata or additional information (not yet implemented in the provided code).
- **API Gateway**: Providing a REST API for accessing the model endpoint (not yet implemented in the provided code).

## Future Work

- Implement API Gateway integration for model endpoint access.
- Add DynamoDB for storing additional data or metadata.
- Enhance feature engineering and model tuning for better accuracy.
- Improve error handling and logging in the deployment and invocation stages.

## License

This project is licensed under the [MIT License](LICENSE).

## Contributing

Contributions to this project are welcome. Please submit a pull request or open an issue if you have suggestions or improvements.

## Contact

For any questions or inquiries, please reach out to [your contact information].
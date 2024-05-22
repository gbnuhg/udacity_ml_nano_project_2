# Operationalizing Machine Learning
## Table of Contents
- Overview
- Process
- Architectural Diagram
- How to Improve
- Screenshots

## Overview of the Project
This project consists of using Azure to configure a machine learning model that will be deployed in the cloud and then consumed. Following that, we will create, publish, and consume the pipeline that we will create. We deployed a Docker UI to view the Swagger REST API documentation and consume the endpoints.

We are again taking a look at the Bank Marketing Training data. With this data, we are creating an AutoML job and then deploying the best classification model to predict whether a customer signed up through the marketing campaign. Once deployed, we enabled application insights before consuming and deploying the model using Swagger. Using the endpoint.py script provided with the correct payload, we got a valid response before jumping over to the Jupyter Notebook to create, publish and consume the pipeline.

## Process
### Step 1 (optional) was skipped
### Step 2: Automated ML Experiment
The project started with an AutoML run. I uploaded the bank marketing dataset, created the experiment and computer cluster, and ran a classification experiment.

Image Below: Bank Training Dataset shown in AutoML
![Dataset](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/119867c7-0530-4c20-84d1-e5e19d13acac)

Image Below: AutoML Job Completion for Bank Marketing Data
![AutoML Complete](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/8c3eabda-3444-420b-904d-87aadaab292e)

### Step 3: Deploy the Best Model
Through this, I identified the best model as the VotingEnsemble. Next, I deployed this model to the web.

Image Below: Voting Ensemble shown as the best model.
![Best Model](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/6da20626-8822-4188-ad83-509720deeeae)

### Step 4:  
After deployment, I enabled authentication by running logs.py to view the logs.

Image Below: Enabled Application Insights
![Application Insight Enabled](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/84647784-3c73-4c78-aa10-7db212786bf5)

Image Below: Logs after running logs.py
![Logs](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/96d9ed90-b6f2-4ed2-a0e9-919c8658290a)

### Step 5: Swagger Deployment

Once this ran correctly, I downloaded the swagger.json file and added it to the Swagger folder within the Udacity starter folder. I ran swagger.sh and serve.py to initiate swagger on the local host and then to open my model on port 8000.

Image Below: Local Host on port 8000 once Swagger was initiated
![Local Host](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/62e3882d-b7f4-4916-a8f6-b80e769ab3dd) 

### Step 6: Consume Model Endpoints
Then I updated the scoring_uri and the key in the code that I pulled from the Consume section of ML Studio. The endpoint result from my test is below.

Image Below: Valid endpoint.py result when run in Git Bash

![Endpoint Result](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/19c7cfb9-4552-46d7-ae54-aaa496066279)

### Step 7: Create, Publish, and Consume a Pipeline
Next, I uploaded the aml-exercise-pipelines-with-automated-machine-learning-step.ipynb file to Notebook within ML Studio. I updated the variables to match my ML Studio credentials, uploaded the config.json to the notebook folder, and ran through all the cells. The pipeline was created in Azure ML Studio and it ran to completion. Below I've noted a screenshot from my Jupyter Notebook (which is also attached), the Pipeline Endpoints, and the Published Pipeline Overview. Additional information is above each image.

Image Below: Jupyter Notebook showing the RunDetails Widget
![RunDetailsWidgetJupyter](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/296feda0-7cb9-4ed1-bed6-e730cfa7c3a9)

Image Below: Pipeline Endpoints showing a finished deployment
![Pipeline Endpoints](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/630a3a24-13a6-4155-a8b2-0e7a9bbc26dd)

Image Below: Published Pipeline Overview from the valid pipeline deployment for the Bank Marketing data
![Published Pipeline Overview](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/67649a8c-da14-4a1b-a01d-78abba4ed5da)

Image Below: Bank Rest Endpoint Showing The Bank Marketing Data in the Graph
![Pipeline Bank Rest Endpoint](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/36fd4efd-e4a6-4296-a5e0-96ff983834ea)

Image Below: List of Completed Pipelines
![Completed Pipeline Overview](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/57009d9e-9cf6-4f02-af12-e6246e9f0759)

## Architectural Diagram
The image shows a diagram of the architecture for the ML process.

Image Below: ML Workflow pulled from the Udacity Course Walkthrough
![ML Workflow](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/f120b9c9-f987-4724-8ba6-511d038fb1fc)

## Improvement
- Try different/more metrics besides AUC_weighted to see if another option performs better with the dataset or subsequent datasets. 
- As populations age, their tendencies change. As I move forward, it would be nice to get additional data or compare the data that I have to another segment of time. I could draw inferences between the timelines or see how the population changes over time.
- Alter the exit criteria for a longer duration to attempt more models when choosing the best model.

## Screenshots & Video Link
- Video Link: https://youtu.be/zdtfn_jKgqI
- Screenshots in the accompanying folder

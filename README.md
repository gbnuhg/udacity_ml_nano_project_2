# Operationalizing Machine Learning
## Table of Contents
- Overview
- Architectural Diagram
- How to Improve
- Screenshots

## Overview of the Project
The project started with an AutoML run. I uploaded the bank marketing dataset, created the experiment and computer cluster, and ran a classification experiment.

![Dataset](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/119867c7-0530-4c20-84d1-e5e19d13acac)

![AutoML Complete](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/8c3eabda-3444-420b-904d-87aadaab292e)

Through this, I identified the best model as the VotingEnsemble.

![Best Model](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/6da20626-8822-4188-ad83-509720deeeae)

Next, I deployed this model, but not before enabling authentication and choosing the ACI option. I ran logs.py to view the logs and enable application insights.

![Logs](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/96d9ed90-b6f2-4ed2-a0e9-919c8658290a)

![Application Insight Enabled](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/84647784-3c73-4c78-aa10-7db212786bf5)

Once this ran correctly, I downloaded the swagger.json file and added it to the Swagger folder within the Udacity starter folder. I ran swagger.sh and serve.py to initiate swagger on the local host and then to open my model on port 8000.

![Local Host](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/62e3882d-b7f4-4916-a8f6-b80e769ab3dd)

Then I updated the scoring_uri and the key in the code that I pulled from the Consume section of ML Studio. The endpoint result from my test is below.

![Endpoint Result](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/19c7cfb9-4552-46d7-ae54-aaa496066279)

Next, I uploaded the aml-exercise-pipelines-with-automated-machine-learning-step.ipynb file to Notebook within ML Studio. I updated the variables to match my ML Studio credentials, uploaded the config.json to the notebook folder, and ran through all the cells. The pipeline was created in Azure ML Studio and it was completed.
![AutoML Bank Marketing CSV](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/93f455d6-e35c-4977-8b09-21433657572e)
![Completed Pipeline Overview](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/403af44f-7c2d-4f90-80ab-336debf89d14)
![Pipeline Completed](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/8b1c6b20-0286-403c-b047-4ce405c99ade)
![Pipeline Endpoint](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/91bf2aaa-9751-40ac-9103-650c04957128)
![Pipeline Bank Rest Endpoint](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/b1a99fb5-58b6-4992-8afb-8c030973ca3b)

## Architectural Diagram
The image shows a diagram of the architecture for the ML process

![ML Workflow](https://github.com/gbnuhg/udacity_ml_nano_project_2/assets/132493261/f120b9c9-f987-4724-8ba6-511d038fb1fc)

## Improvement
- Try different/more metrics besides AUC_weighted to see if another option performs better with the dataset or subsequent datasets. 
- As populations age, their tendencies change. As I move forward, it would be nice to get additional data or compare the data that I have to another segment of time. I could draw inferences between the timelines or see how the population changes over time.
- Alter the exit criteria for a longer duration to attempt more models when choosing the best model.

## Screenshots & Video Link
- Video Link: https://youtu.be/hjP8bwpimLI
- Screenshots in the accompanying folder and above overview

+++
title = "1. Architecture"
date = 2019-11-18T17:11:28+11:00
weight =4
+++

### Solution Architecture

The diagram is an architectural overview of the AWS services that you will be using for this workshop.

![](/images/module-medical-document-processing-and-classification/architecture-v2.png)


For this workshop, you will learn how to build a data pipeline that will:
1. Upload the electronic medcial record to S3
2. Extract textual data from PDF records using Amazon Textract
3. Extract medical information from text using Amazon Comprehend Medical
4. Prepare a dataset using the meddical data which will be used to train our machine learning model

Once you have implemented your data pipeline, you will learn how to use SageMaker to:
1. Perform data exploration
2. Train a classification machine learning (ML) model
3. Improve the ML model using SageMaker Hyperparameter Optimization
4. Deploy your ML model
5. Run inference on your deployed model

### Next Steps
Click [here](../demo/) to setup your notebook.

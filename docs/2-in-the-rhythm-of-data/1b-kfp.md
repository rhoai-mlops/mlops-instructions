## Kubeflow Pipelines (KfP)

KfP is a powerful framework designed for building, deploying, and managing machine learning workflows on Kubernetes. It provides a robust set of tools for creating reusable and modular pipelines that can easily handle complex machine learning tasks, from data ingestion to model training and evaluation. KfP supports advanced features such as versioning, metadata tracking, and resource management, allowing teams to monitor and optimize their workflows effectively. By leveraging the scalability and orchestration capabilities of Kubernetes, KfP enables organizations to deploy production-ready machine learning solutions that can adapt to evolving data and model requirements seamlessly.

We will treat KfP as our production-grade training pipeline. It will be the pipeline that gets triggered when there is an update in the source code of the model, when there is fresh data we can use to train the model further, when there is an alert that the model is behaving unusual. Therefore, you will find the pipeline definition under `4-prod_datascience` folder. 

If you look at the files under this folder, they are mainly the steps that we have in the Notebooks we executed previously. The steps are broken down into individual functions and files to have better modularity, easy to update and maintain them. Also the functions have better error handling and reporting. 

![kfp.png](./images/kfp.png)

Normally, we are not going to trigger this pipeline manually but just to test the functionality and view the output, let's go to Terminal and initiate a pipeline by running the below command:

```bash

```


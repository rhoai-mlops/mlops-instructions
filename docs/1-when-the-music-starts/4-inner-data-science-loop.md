## Inner Data Science Loop

Just like in traditional software development world, here the inner loop represents the iterative process of building, testing, and refining machine learning models.

This inner loop is essential in data science as well because it allows for continuous improvement and optimization of machine learning models. The main stages we usually see in building ML models are as below:

- Data Preparation: Gathering, cleaning, and transforming data into a suitable format for model training.
- Model Development: Selecting and implementing appropriate machine learning algorithms.
- Model Training: Feeding the prepared data into the model and adjusting its parameters to learn patterns and relationships.
- Model Evaluation: Assessing the model's performance using metrics like accuracy, precision, recall, and F1-score.
- Model Refinement: Iterating on the previous steps to improve the model's accuracy and generalization capabilities.

Let's get some experience on these stages by following the steps in notebooks we cloned to our workbench. It all starts with getting familiar with the dataset at hand, so we'll start with `jukebox/data-processing/data_exploration.ipynb` notebook.

TODO: update screenshot

![jupyter_notebook.png](./images/jupyter_notebook.png)

At the end, what we will have is a working model we can serve from OpenShift AI. 

Now make your way to the Notebook and when you have a model saved in the `models` bucket, come back here to follow the next steps 😁

TODO: add screenshot from minio

### Model Serving


## Model Registry

A model registry is a centralized metadata repository for managing machine learning models. It serves as a hub for storing information such as version, author, and model location.

We are using Kubeflow model registry as a canonical data source by storing model version, training data reference, experiment results and so on. Here are some reasons to use a registry (_from Kubeflow website_):

- Track models available on storage: once the model is stored, it can then be tracked in the Kubeflow Model Registry for managing its lifecycle. The Model Registry can catalog, list, index, share, record, organize this information. This allows the Data Scientist to compare different versions and revert to previous versions if needed.

- Track and compare performance: View key metrics like accuracy, recall, and precision for each model version. This helps identify the best-performing model for deployment.

- Create lineage: Capture the relationships between data, code, and models. This enables the Data Scientist to understand the origin of each model and reproduce specific experiments.

- Collaborate: Share models and experiment details with the MLOps Engineer for deployment preparation. This ensures a seamless transition from training to production.

1. An instance of the registry is available in your dev environment as well. 

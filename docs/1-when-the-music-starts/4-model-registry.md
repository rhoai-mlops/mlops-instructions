## Model Registry

A model registry is a centralized metadata repository for managing machine learning models. It serves as a hub for storing information such as version, author, model location and so on.

### Kubeflow Model Registry

Kubeflow model registry provides a central index for ML model developers to index and manage models, versions, and ML artifacts metadata. Here are some reasons to use a registry (_from Kubeflow website_):

- Track models available on storage: once the model is stored, it can then be tracked in the Kubeflow Model Registry for managing its lifecycle. The Model Registry can catalog, list, index, share, record, organize this information. This allows the Data Scientist to compare different versions and revert to previous versions if needed.

- Track and compare performance: View key metrics like accuracy, recall, and precision for each model version. This helps identify the best-performing model for deployment.

- Create lineage: Capture the relationships between data, code, and models. This enables the Data Scientist to understand the origin of each model and reproduce specific experiments.

- Collaborate: Share models and experiment details with the MLOps Engineer for deployment preparation. This ensures a seamless transition from training to production.

1. An instance of the registry is available in your dev environment as well. 


 🪄🪄🪄 Now that we got to know the essential tools to start our journey, let's dive into our dataset! 🪄🪄🪄
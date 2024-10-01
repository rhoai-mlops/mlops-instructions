## Inner Data Science Loop

Just like in traditional software development world, here the inner loop represents the iterative process of building, testing, and refining machine learning models.

This inner loop is essential in data science as well because it allows for continuous improvement and optimization of machine learning models. The main stages we usually see in building ML models are as below:

- Data Preparation: Gathering, cleaning, and transforming data into a suitable format for model training.
- Model Development: Selecting and implementing appropriate machine learning algorithms.
- Model Training: Feeding the prepared data into the model and adjusting its parameters to learn patterns and relationships.
- Model Evaluation: Assessing the model's performance using metrics like accuracy, precision, recall, and F1-score.
- Model Refinement: Iterating on the previous steps to improve the model's accuracy and generalization capabilities.

Let's get some experience on these stages by following the steps in notebooks we cloned to our workbench. It all starts with getting familiar with the dataset at hand, so we'll start with `jukebox/2-data_exploration/1-data_exploration.ipynb` notebook.


![jupyter_notebook.png](./images/jupyter_notebook.png)

At the end, what we will have is a working model we can serve from OpenShift AI. 

Now make your way to the Notebook and when you have a model saved in the `models` bucket, come back here to follow the next steps 😁

![model_in_bucket.png](./images/model_in_bucket.png)


### Model Serving



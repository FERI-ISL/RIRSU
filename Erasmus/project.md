# Project assignment
> The project assignement will cover the following topics:
>   - Data pre-processing
>       - Data transformation
>       - Data engineering
>   - Machine learning algorithms
>   - Building simple intelligent solutions (web application)

## Required knowledge
* Basic data engineering knowledge
* Intermediate knowledge of machine learning
* Knowledge of Python programming language
* Knowledge of building basic REST API services
* Knowledge of building basic front-end applications

## Deadline
- The project has to be finished until end of January 2025
- You will receive the exact date in advance
- You will have to present and explain your implemented solution to me in person
  - Based on this you will receive points for practical part of the course (max. 50), which represents half of your final grade

## Project description
**Topic:** Detection of fraud warranty claims

>_You will be working on a problem of detecting the possible fraud when some buyer tries to fraudly claim a warranty for some product which he/she bought previously._

You will be given a dataset containing few thousands warranty claims data which has been labeled as fraud or not. On those data you will conduct data pre-processing transformations. After data pre-preprocessing you will build predictive model and serialized it so it can be used later on. You will build predictive REST API service which would receive data of a warranty claim. The received data has to be transformed in exactly the same manner as before the training the predictive model. The service has to load, previously serialized predictive model and based on the received data has to conduct the predicting whether the warraty claim is fraud or not (value of probability between 0.0 and 1.0), Finally, you will have to build a simple front-end interface with a form for inserting warranty claim data. On form submit, the inserted data has to be sent to previously build REST API service which will return the probability that the insert claim is fraud (value between 0.0 and 1.0). If the received value is below (0.5) you display the success message on the front-end, otherwise the error message is displayed saying that the inserted claim is probably fraud.


## Dataset
Description of dataset features:
- Area: The area where the consumer resides.
- Consumer_profile: The type of consumer.
- Product_category: The category of the product.
- Product_type: The type of product.
- AC_1001_Issue: Issue code for AC type 1001.
- AC_1002_Issue: Issue code for AC type 1002.
- AC_1003_Issue: Issue code for AC type 1003.
- TV_2001_Issue: Issue code for TV type 2001.
- TV_2002_Issue: Issue code for TV type 2002.
- TV_2003_Issue: Issue code for TV type 2003.
- Claim_Value: The value of the warranty claim.
- Service_Centre: The service center code.
- Product_Age: The age of the product in months.
- Purchased_from: Purchased from manufacturer or dealer. 
- Call_details: Call time.
- Purpose: Type of purpose (claim/complaint).
- Fraud: Target value
- ID: identification number.

[Here is the link to dataset preview.](https://embed.deepnote.com/2884a9be-fa17-4020-bda5-454a7d229c77/5238504de55e4c009fb14aa52cfda47c/296cbbd647d542f79323cec2a69db496)

## Project milestones
Bellow are defined crutial milestones on your journey to complete this project assignment. It is advised (not mandatory) that when each milestone is reached you check with the teaching assistant whether you are on the right track. 

### 1. Milestone - Data pre-processing

- Load the dataset into [Pandas DataFrame](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html) 
- Remove the columns which are not needed (i.e. ID column)
- Check if any feature (column) has missing values
  - If there are missing values, fill them with mean value of corresponding feature (column)
- Check whether the numeric features are normally distributed
  - If specficic feature values are normally distributted you should conduct [standardization](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html#sklearn.preprocessing.StandardScaler)
  - Otherwise the specific feature values should be [normalized](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.MinMaxScaler.html#sklearn.preprocessing.MinMaxScaler)
- The categorical features should be [one-hot encoded](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.OneHotEncoder.html#sklearn.preprocessing.OneHotEncoder)

### 2. Milestone - Training and evaluating machine learning models
- Split the dataset into X (input features) and y (target feature - "Fraud")
- Using the [5-Fold cross-validation ](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.cross_validate.html) evaluate different [classification algorithms](https://scikit-learn.org/stable/supervised_learning.html).
- Evaluate the algorithms using the following metrics: Accuracy, F1-score, and AUC ([help](https://scikit-learn.org/stable/auto_examples/model_selection/plot_multi_metric_evaluation.html#sphx-glr-auto-examples-model-selection-plot-multi-metric-evaluation-py))
- Conduct the comparison between evaluated machine learning algorithms in form of charts for each of before mentioned evaluation metrics.

> You should train and evaluate at least 5 different classification algorithms with various parameter settings to find the best performing one, which you will use in your intelligent web application.

### 3. Milestone - Pipelines
- For the process of filling missing values, standardizing/normalizing numeric features and one-hot encoding categorical features (1. Milestone) use [sklearn pipelines](https://scikit-learn.org/stable/modules/generated/sklearn.pipeline.Pipeline.html) instead on manually manipulating the data.
- Recreate in the previous phase best achieved predictive model and train it on the complete dataset using sklearn pipelines.
    ![Pipeline Demo](images/complete_pipeline.png)
- Serialize complete pipeline with [pickle](https://docs.python.org/3/library/pickle.html) or with some similar library.

### 4. Milestone - Predictive REST API
- Integrate the trained predictive model into simple REST API service.
- The service has to receive all the necessary input features in form of JSON document.
- Those received features are then passed to loaded predictive model in order to predict the probability of warranty claim being fraud or not.
- Predicted probability value for received data is returned as a JSON response.
- You can use any of the Python web frameworks to make the task of implementation easier.
  - [Useful resource](https://www.datacamp.com/tutorial/machine-learning-models-api-python).
- Finally, developed REST API service should be packaged into Docker image (optional for higher grades).

### 5. Milestone - Front-end
- Using any JavaScript and/or CSS framework build simple front-end application.
- Application should feature form for inserting all warranty claim informations.
- When submitting the inserted form data, the data has to be sent to previously build predictive REST API service.
- The response of the predictive REST API service is displayed on the front-end:
  - Predictive service will return the value between 0.0 and 1.0.
  - In case the received value is <0.5 notification of successfull warranty claim submission is displayed
  - In case the received value is >=0.5 notification of fraud warranty claim submission is displayed.
- Finally, developed front-end application should be packaged into Docker image (optional for higher grades).
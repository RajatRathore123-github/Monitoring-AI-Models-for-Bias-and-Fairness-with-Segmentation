
# Monitoring AI Models For Bias and Fairness with segmentation

Monitoring AI models for bias and fairness with segmentation is a technique used to identify and address potential unfairness in machine learning models. Here's a breakdown of the key aspects:

Bias in AI Models:

• AI models can inherit biases from the data they are trained on, leading to discriminatory outcomes.

• This can happen due to historical biases in the data itself, or even reflect unconscious biases of the developers.

Fairness Monitoring:

• The goal is to ensure the model performs consistently and fairly across different subgroups within the data.

• This is crucial for ethical AI development and to avoid unintended consequences.

Segmentation:

• Segmentation involves dividing the data used by the model into different subgroups based on relevant characteristics.

• These characteristics could be things like gender, race, age, income, etc., depending on the specific use case.

## Getting Started

I have made this project on Google Collab using Iris dataset. The Iris dataset was used in R.A. Fisher's classic 1936 paper, The Use of Multiple Measurements in Taxonomic Problems, and can also be found on the UCI Machine Learning Repository.

It includes three iris species with 50 samples each as well as some properties about each flower. One flower species is linearly separable from the other two, but the other two are not linearly separable from each other.

The columns in this dataset are:

• `Id`

• `SepalLengthCm`

• `SepalWidthCm`

• `PetalLengthCm`

• `PetalWidthCm`

• `Species`

I have used Whylabs here for monitoring and tracing the Bias and Fairness of the Model.

## Why Whylabs:

WhyLabs.ai is an AI observability platform that prevents data & model performance degradation by allowing you to monitor your data and machine learning models in production.

## Environment Variables

To run this project, you will need to add the following environment variables to your notebook as `os.environ`

 Setting authentication & project keys:

`os.environ["WHYLABS_DEFAULT_ORG_ID"] = 'ORG_ID'`

`os.environ["WHYLABS_API_KEY"] = 'API_KEY'`

`os.environ["WHYLABS_DEFAULT_DATASET_ID"] = 'model_name'`


## Screenshots

![](/Florida_verginica_metric.png)

Florida has more bias towards Verginica.

![](/Florida_median_metric.png)

Florida has a median conflicting with the combined data as well as each from Washington and Missouri.


## Usage/Examples

Creating profiles with Whylogs

```python
profile1 = why.log(X_batch_1)

profile_view1 = profile1.view()
profile_view1.to_pandas()

```


## FAQ

#### Why their is the need for bias detection?

Bias detection in machine learning (ML) models is crucial for ensuring fair and responsible AI.

Biased models can discriminate against certain groups, leading to unfair outcomes. For instance, a loan approval model trained on biased data might disadvantage applicants from certain ethnicities. Bias detection helps identify and mitigate such issues.

#### How to verify if model is biased?

Examining the Data:
• Data Source and Collection:  Investigate the origin of your data. Was it collected in a fair and unbiased way?  Look for imbalances or missing data points that could skew the model's learning.

• Data Analysis: Analyze the data itself for potential biases. Are certain groups over-represented or under-represented? Are there any unexpected trends or outliers that could indicate bias?

• Feature Selection: Consider the features used to train the model. Could some features be inherently biased or correlated with sensitive attributes like race or gender?

Evaluating Model Performance:
• Fairness Metrics:  There are statistical metrics designed to detect bias in model outputs.  




## Authors

- [@Rajat Rathore](https://github.com/RajatRathore123-github)


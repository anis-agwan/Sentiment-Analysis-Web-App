# Sentiment-Analysis-Web-App

### Using PyTorch and SageMaker

#### Step 1: Downloading the data
As in the XGBoost in SageMaker notebook, we will be using the [IMDb dataset]

#### Step 2: Preparing and Processing the data
Also, as in the XGBoost notebook, we will be doing some initial data processing. The first few steps are the same as in the XGBoost example. To begin with, we will read in each of the reviews and combine them into a single input structure. Then, we will split the dataset into a training set and a testing set.

#### Step 3: Upload the data to S3
As in the XGBoost notebook, we will need to upload the training dataset to S3 in order for our training code to access it. For now we will save it locally and we will upload to S3 later on.

#### Step 4: Build and Train the PyTorch Model
In the XGBoost notebook we discussed what a model is in the SageMaker framework. In particular, a model comprises three objects
Model Artifacts,
Training Code, and
Inference Code


#### Step 5: Testing the model
As mentioned at the top of this notebook, we will be testing this model by first deploying it and then sending the testing data to the deployed endpoint. We will do this so that we can make sure that the deployed model is working correctly.

#### Step 6: Deploy the model for testing
Now that we have trained our model, we would like to test it to see how it performs. Currently our model takes input of the form review_length, review[500] where review[500] is a sequence of 500 integers which describe the words present in the review, encoded using word_dict. Fortunately for us, SageMaker provides built-in inference code for models with simple inputs such as this.

#### Step 7 - Use the model for testing
Once deployed, we can read in the test data and send it off to our deployed model to get some results. Once we collect all of the results we can determine how accurate our model is.


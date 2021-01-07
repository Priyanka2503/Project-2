# Operationalizing Machine Learning - Pipeline Automation
In this project we are deploying two machine learning models.One using Azure UI and second using Jupyter notebook in SDK. This project uses Bank Marketing Dataset. The link for the dataset is https://automlsamplenotebookdata.blob.core.windows.net/automl-sample-notebook-data/bankmarketing_train.csv .By both the methods I tried to get the best model required.First I had trained the model and then deployed it by Azure Container Instance(ACI).The best model created was deployed as a webservice that can be utilised from anywhere that can communicate via HTTP.Then the REST Endpoint is created.Endpoint is the location from which APIs can access the resources they need to carry out their function

## Architectural Diagram
![Image](https://user-images.githubusercontent.com/75804779/103789839-75e8a800-5066-11eb-8728-69dc09ecbd71.png)

## Key Steps
As shown in Architectural Diagram, I had implemented those steps.The screenshots of those are attached herewith.

First I explored the dataset.
![Screenshot (362)](https://user-images.githubusercontent.com/75804779/103796845-ba2b7680-506d-11eb-9afb-efe99d75b512.png)

Then I created and the dataset from local files.
![Screenshot (361)](https://user-images.githubusercontent.com/75804779/103796292-075b1880-506d-11eb-8115-9fe4e8357455.png)

![Screenshot (413)](https://user-images.githubusercontent.com/75804779/103922473-ce3caa00-5139-11eb-9e92-4327ecaa3854.png)

After that I trained the AutoML model.In this AutoML trained model using several models and found their respective accuracies.Here, I had run the experiment using Classification Technique.
![Screenshot (366)](https://user-images.githubusercontent.com/75804779/103799638-5c992900-5071-11eb-8fca-d1b718685587.png)

![Screenshot (369)](https://user-images.githubusercontent.com/75804779/103800116-fd87e400-5071-11eb-8222-b36b5cb6433f.png)

![Screenshot (367)](https://user-images.githubusercontent.com/75804779/103800209-1db7a300-5072-11eb-9c68-29ce52bef645.png)

Now the AutoML run is completed.Some of the models along with their accuracies are shown in the figure.
![Screenshot (365)](https://user-images.githubusercontent.com/75804779/103799594-50ad6700-5071-11eb-9994-b5e20412f7de.png)

Here, VotingEnsemble technique has the highest accuracy.Hence it is the best model.
After that I deployed this model with authentication.The Voting Ensemble estimates multiple base models and uses voting to combine the individual predictions to arrive at the final ones.
![Screenshot (374)](https://user-images.githubusercontent.com/75804779/103802591-63c23600-5075-11eb-8492-b6bee9aeff67.png)

After that I enabled Application insights using logs.py file.
![Screenshot (377)](https://user-images.githubusercontent.com/75804779/103803106-20b49280-5076-11eb-83e6-551458af3ec6.png)

![Screenshot (378)](https://user-images.githubusercontent.com/75804779/103803122-27dba080-5076-11eb-95f5-aa33a2da85b6.png)

![Screenshot (372)](https://user-images.githubusercontent.com/75804779/103916384-60d94b00-5132-11eb-8a33-95dce6ba1f26.png)

Then I created Swagger documentation to help interact with the model through the REST API endpoint
![Screenshot (379)](https://user-images.githubusercontent.com/75804779/103804308-e64bf500-5077-11eb-854d-694f5420805a.png)

![Screenshot (380)](https://user-images.githubusercontent.com/75804779/103804339-f49a1100-5077-11eb-86a3-0c723c294e53.png)

Finally I consumed the endpoint of the deployed model.
![Screenshot (382)](https://user-images.githubusercontent.com/75804779/103804718-8c97fa80-5078-11eb-9385-1cf8be9e2b54.png)

Then I benchmarked the deployed model.
![Screenshot (409)](https://user-images.githubusercontent.com/75804779/103898347-cf121380-511a-11eb-8dc8-4d7ba0996812.png)

Now, I did the project using python SDK.I created a pipeline using jupyter notebook.
![Screenshot (401)](https://user-images.githubusercontent.com/75804779/103894727-58bee280-5115-11eb-82eb-24033660165a.png)

![Screenshot (400)](https://user-images.githubusercontent.com/75804779/103894792-6d9b7600-5115-11eb-8a94-3f1071b9ab3c.png)

![Screenshot (402)](https://user-images.githubusercontent.com/75804779/103895637-b6076380-5116-11eb-8ad1-bf82f68d61ac.png)

![Screenshot (410)](https://user-images.githubusercontent.com/75804779/103916797-db09cf80-5132-11eb-823e-73245a237a0b.png)

The pipeline can be seen here.
![Screenshot (403)](https://user-images.githubusercontent.com/75804779/103896379-e4d20980-5117-11eb-8c69-b7146b9922be.png)

After that I created the REST endpoints.
![Screenshot (404)](https://user-images.githubusercontent.com/75804779/103896657-50b47200-5118-11eb-8a4f-d1d063daef8a.png)

Then I enabled RunDetails widgets.
![Screenshot (407)](https://user-images.githubusercontent.com/75804779/103897465-a2113100-5119-11eb-8f30-e6c939af92aa.png)

![Screenshot (406)](https://user-images.githubusercontent.com/75804779/103897325-5bbbd200-5119-11eb-925b-23ab4ce06220.png)

## Screen Recording
Link : https://drive.google.com/file/d/11XSMg5GIUL7qW5fo0NnqSFbhWOF3HwXh/view?usp=sharing

## Future Improvements

1. We can deploy the model using Azure Kubernetes Service(AKS)
2. We can extend the training time

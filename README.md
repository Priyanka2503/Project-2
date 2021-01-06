# Operationalizing Machine Learning - Pipeline Automation
In this project we are deploying two machine learning models.One using Azure UI and second using Jupyter notebook in SDK. This project uses Bank Marketing Dataset. The link for the dataset is https://automlsamplenotebookdata.blob.core.windows.net/automl-sample-notebook-data/bankmarketing_train.csv .By both the methods I tried to get the best model required.

## Architectural Diagram
![Image](https://user-images.githubusercontent.com/75804779/103789839-75e8a800-5066-11eb-8728-69dc09ecbd71.png)

## Key Steps
As shown in Architectural Diagram, I had implemented those steps.The screenshots of those are attached herewith.

First I explored the dataset.
![Screenshot (362)](https://user-images.githubusercontent.com/75804779/103796845-ba2b7680-506d-11eb-9afb-efe99d75b512.png)

Then I created and the dataset from local files.
![Screenshot (361)](https://user-images.githubusercontent.com/75804779/103796292-075b1880-506d-11eb-8115-9fe4e8357455.png)

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

![Screenshot (374)](https://user-images.githubusercontent.com/75804779/103803140-3033db80-5076-11eb-914b-4d86121e1922.png)

Then I created Swagger documentation to help interact with the model through the REST API endpoint
![Screenshot (379)](https://user-images.githubusercontent.com/75804779/103804308-e64bf500-5077-11eb-854d-694f5420805a.png)

![Screenshot (380)](https://user-images.githubusercontent.com/75804779/103804339-f49a1100-5077-11eb-86a3-0c723c294e53.png)

Finally I consumed the endpoint of the deployed model.
![Screenshot (382)](https://user-images.githubusercontent.com/75804779/103804718-8c97fa80-5078-11eb-9385-1cf8be9e2b54.png)

Now, I did the project using python SDK.I created a pipeline using jupyter notebook.

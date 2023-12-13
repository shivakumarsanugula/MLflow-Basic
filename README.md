# MLflow-Basic



## For Dagshub:


MLFLOW_TRACKING_URI=https://dagshub.com/shivakumarsanugula/MLflow-Basic.mlflow \
MLFLOW_TRACKING_USERNAME=shivakumarsanugula \
MLFLOW_TRACKING_PASSWORD=2aeae54d39728e7a12782a69f438912055bf96b1 \
python script.py

```bash

export MLFLOW_TRACKING_URI=https://dagshub.com/shivakumarsanugula/MLflow-Basic.mlflow \

export MLFLOW_TRACKING_USERNAME=shivakumarsanugula 

export MLFLOW_TRACKING_PASSWORD=2aeae54d39728e7a12782a69f438912055bf96b1


```

## MLflow on AWS Setup:
Login to AWS console.
Create IAM user with AdministratorAccess
Export the credentials in your AWS CLI by running "aws configure"
Create a s3 bucket
Create EC2 machine (Ubuntu) & add Security groups 5000 port
Run the following command on EC2 machine

```bash

sudo apt update

sudo apt install python3-pip

sudo pip3 install pipenv

sudo pip3 install virtualenv

mkdir mlflow

cd mlflow

pipenv install mlflow

pipenv install awscli

pipenv install boto3

pipenv shell



## Then set aws credentials
aws configure


#Finally 
mlflow server -h 0.0.0.0 --default-artifact-root s3://mlflow-test-23

#open Public IPv4 DNS to the port 5000


#set uri in your local terminal and in your code 
export MLFLOW_TRACKING_URI= 


```





# MLOPs End-to-End Pipeline

# Machine Learning Dev Ops Guideline I follow in my ML Projects

### 1a. AWS - EC2 ubuntu instance
   Virtual Machine Commands:
   sudo apt update
   sudo apt install python3-pip
   sudo apt install virtualenv
   mkdir mlflow
   cd mlflow
   pipenv install mlflow
   pipenv install awscli
   pipenv install boto3
   pipenv shell
   aws configure
### 1b. AWS - SageMaker
### 1c. AWS - S3- 1c. AWS - ECR
### 1d. GCP Google Cloud Platform (Vertex AI)

## 2. Ubuntu Linux setup
   
## 3. Git

   `git init`

## 4. [`DVC`](https://dvc.org/doc/start) (Data Version Control) 

Split Jupyter Notebook into Python Scripts (Modular Approach):

1. data_ingestion.py 
2. data_preprocessing.py
3. feature_engineering.py
4. model_building.py
5. model_evaluation.py 

6. Output metrics.json

Create  [`dvc.yaml`](./dvc.yaml) (configuration file)

`git init` & `dvc init` , `dvc repro` (this will execute `dvc.yaml`) , `dvc dag` , `dvc metrics show` 

## 5. Experiment Tracking 

   ![`MLflow Metrics`](https://github.com/spha-code/MLflow/blob/main/MLflow_Metrics.png)

   [`MLflow`](https://mlflow.org/) & [`Dagshub`]( https://github.com/DagsHub)

   See here [`MLflow Repo`](https://github.com/spha-code/MLflow)
   
## 6. Docker

   ### 1. Dockerfile

   docker build -t username/app: latest
   docker run -p 8080:8080 username/app: latest
   docker run -d -p 8080:8080 username/app: latest

   ### 2. Docker Hub

   docker login
   docker push username/app: latest

## 7. Jenkins Pipeline
Install Jenkins in AWS EC2 Ubuntu Instance
sudo apt update
sudo apt install openjdk-8-jdk -y
visit: https://pkg.jenkins.io/debian-stable/
sudo systemctl start jenkins
sudo systemctl enable jenkins
sudo systemctl status jenkins
add 8080 port to the security group
sudo cat /var/lib/jenkins/secrets/initialAdminPassword

## 8. Kubernetes in Google Cloud
commands:
- git clone project in Google Cloud
- export PROJECT_ID=eng-hangar-466608-e9 (Google Cloud Project ID)
- docker build -t gcr.io/${PROJECT_ID}/{DOCKER-IMAGE} .
- docker images
- gcloud auth configure-docker gcr.io
- docker push gcr.io/${PROJECT_ID}/{DOCKER-IMAGE}
- gcloud config set compute/zone us-central1
- gcloud container clusters create app-cluster --num-nodes=1
- kubectl create deployment app --image=gcr.io/${PROJECT_ID}/{DOCKER-IMAGE} 
- kubectl expose deployment app --type=LoadBalancer --port 80 --target-port 8080
 ## 9. Grafana (Observability)
- docker run -d -p 3000:3000 --name=grafana grafana/grafana-oss
- admin - admin
- docker run --name prometheus -d -p 127.0.0.1:9090:9090 prom/prometheus

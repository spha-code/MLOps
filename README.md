# MLOPs End-to-End Pipeline
Machine Learning Dev Ops Guideline

## 1a. AWS - EC2 - 1b. AWS - SageMaker - 1c. AWS - S3- 1c. AWS - ECR

or

## 1d. GCP Google Cloud Platform (Vertex AI)

## 2. Ubuntu Linux setup and commands
   
   https://chmod-calculator.com/
   
   touch   vim i - esc - :wq   cat   cp   mv   rm    man ls    htop    
   chmod     tar cf archive.tar test.py test.txt    untar -xvf archive.tar    gzip file.txt    whoami    sudo useradd otheruser    sudo userdel otheruser    date    time    echo "Hello"    head hello.txt    tail hello.txt
   
## 3. Git

   `git init`

   `git commit -m "message"`
   
   `git origin push main`
   
   `git checkout main`
   `git checkout -b newbranch`

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
   
  

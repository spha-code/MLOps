# MLOPs End-to-End Pipeline
Machine Learning Dev Ops Guideline

## 1. AWS - EC2

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

## 4. DVC (Data Version Control)

Split Jupyter Notebook into Python Scripts (Modular Approach):

1. data_ingestion.py 
2. data_preprocessing.py
3. feature_engineering.py
4. model_building.py
5. model_evaluation.py 

Create  [`dvc.yaml`](./dvc.yaml) (configuration file)

`dvc init` , `dvc repro` (this will execute `dvc.yaml`) , `dvc dag` 
   

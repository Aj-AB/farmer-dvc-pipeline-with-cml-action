# DVC pipeline with cml

Github
git init 
git add README.mdgit commit -m "first commit"
git branch -M main
git remote add origin https://github.com/repo
git push -u origin main

Set DVC
dvc init

DVC pipelines
dvc run -n get_data -d get_data.py -o data_raw.csv --no-exec python get_data.py
dvc.yaml
stages:
  get_data:
    cmd: python get_data.py
    deps:
    - get_data.py
    outs:
    - data_raw.csv
  process:
    cmd: python process_data.py
    deps:
    - process_data.py
    - data_raw.csv
    outs:
    - data_processed.csv
  train:
    cmd: python train.py
    deps:
    - train.py
    - data_processed.csv
    outs:
    - by_region.png
    metrics:
    - metrics.json:
        cache: false

Run the 
dvc repro


create .github/workflow/train.yaml

branch to test


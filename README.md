# cml

Github
git init 
git add README.mdgit commit -m "first commit"
git branch -M main
git remote add origin https://github.com/repo
git push -u origin main

Set DVC
dvc init

DVC pipelines
dvc run -n get_data -d get_data.py -o data_raw.csv --no-exec python get_data.py
dvc.yaml

create train.yaml

Run the 
dvc repro


create .github/workflow/train.yaml

branch test
change the model to LinearDiscriminantAnalysis
compare two model logistic and LinearDiscriminantAnalysis

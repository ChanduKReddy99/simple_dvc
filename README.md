# simple_dvc

clone the repo from git
```
git clone https://github.com/<username>/<repo_name>.git
```

create virtual env & activate it
```
conda create -p .venv python=3.7 -y
source activate .venv/
```
create a data folder & get the data in to this folder
```
mkdir data
cp <file path> <data folder name>/
```

initialize the dvc
```
dvc init
```
add the google drive to dvc do that dvc can store the tracked data
```
dvc remote add -d dvc_remote gdrive://<drive path>
```
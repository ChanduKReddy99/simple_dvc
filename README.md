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

install the dvc & dvc[gdrive] for remote storage

```
pip install dvc
pip install dvc[gdrive]
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
commit these changes
```
git commit .dvc/config -m 'configuring remote storage'
```
push the changes and authenticate the remote storage
```
dvc push
```
commit the changes and push to git
```
git add . && git commit -m '1st commit'
git branch -M main
git push -u origin main
```
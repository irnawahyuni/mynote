# quick note for anaconda, python, jupyter notebook, spark
## Installed Anaconda on linux
1. download anaconda file 
> wget https://repo.anaconda.com/archive/Anaconda3-2020.07-Linux-x86_64.sh
2. install file. 
> bash Anaconda3-2020.07-Linux-x86_64.sh


## upgrade anaconda package
>conda upgrade conda
>conda upgrade --all
note: running conda upgrade conda should not be necessary because --all includes the conda package itself

## managing environment
1. create new environtment with specific python version
> conda create -n env_name python=3.8
2. enter new environtment
> conda activate env_name
3. check list of package
> conda list

## check or list environment
> conda env list

## remove environtment
> conda env remove -n env_name

## saving and loading environtment
a useful feature to share environment to others. 
1. saving environment
> conda env export > environment.yaml
2. create new environment from environment file
> conda env create -f environment.yaml



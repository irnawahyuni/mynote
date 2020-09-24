# short note for installation
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
by default, anaconda run on base environment. buat we can create new environment to manage multiproject with different environment
## check or list environment
> conda env list

## create new environment
1. create new environtment with specific python version
> conda create -n env_name python=3.8
2. enter new environtment
> conda activate env_name
3. check list of package
> conda list

## remove environtment
> conda env remove -n env_name

## install package
using conda or pip
> pip install pandas  
> pip install matplotlib
> pip install sklearn


## saving and loading environtment
a useful feature to share environment to others. 
1. saving environment
> conda env export > environment.yaml
2. create new environment from environment file
> conda env create -f environment.yaml

## sharing requirements.txt
creating requiments file to make easier for people to install all the dependencies for your code
1. Generate requirements
> pip freeze > requirements.txt
2. install requirements
> pip install -r requirements.txt


# jupyter notebook
jupyter notebook by default is installed from anaconda in base environment
by default jupyter notebook run on port 8888

1. run jupyter notebook in linux with no browser and specific port
> jupyter-notebook --ip=fullhostname --no-browser --port 8810
To access the notebook, open this file in a browser:
        http://fullhostname:8810/?token=eea035f243b266709c7db768097a52a203d4c84f0eb487b3
or http://127.0.0.1:8810/?token=eea035f243b266709c7db768097a52a203d4c84f0eb487b3

## create tunneling to access jupyter notebook on server or remotely
1. open previous jupyter notebook remotely using localhost and port 8810
>  ssh -N -L 8810:fullhostname:8810 userid@fullhostname
enter password
2. open in local browser
> http://localhost:8810/?token=eea035f243b266709c7db768097a52a203d4c84f0eb487b3

## create new kernel on jupyter notebook
by default installing anaconda, ipykernel was installed
1. if not available, install ipykernel
> pip install ipykernel
2. create new kernel, link new ipykernel with new environement
python -m ipykernel install --user --name=ENV_NAME
3. list kernel
> jupyter kernelspec list
4. remove unwanted kernel
> jupyter kernelspec uninstall kernelname


## Setup

- If not on a unix system, install virtualbox, and setup your VM.

- First off run:

`sudo apt-get update`
`sudo apt-get upgrade`

- Install git ant other tools
`sudo apt-get git`
`sudo apt-get install build-essential python3-dev python3-setuptools python3-tk`

- Install pip
`curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py`

- Install virtualenv
`sudo pip install -U virtualenv

- Create your virtual environment
`virtualenv <env_name>`
`source <env_name>/bin/activate`

- Install ML Tools
`pip install -U numpy scipy`
`pip install -U pandas statsmodels`
`pip install -U scikit-learn`
`pip install -U matplotlib`

- Install ipython and jupyter
`pip install -U ipython jupyter`

- Install tensorflow
`pip install -U ipython jupyter`

- Install pytorch
`pip install -U torch torchvision`

- Test jupyter notebook
`cd <env_name>`
`mkdir project`
`cd project`
`jupyter notebook`

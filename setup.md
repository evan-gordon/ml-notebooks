# Foreword:
Original setup instructions from https://github.com/JoeDumoulin
I do not claim ownership to anything within this file, it was re-uploaded and edited here for future reference.


# CSCD439 - Fall 2017
## Installing Software for Machine Learning

1. Install Virtual Box ( **If you are running ubuntu 16.04 on your system, then you can skip to step 3 below.**)

	go to [VirtualBox Wiki Downloads](https://www.virtualbox.org/wiki/Downloads) and download the version of VBox appropriate for your base operating system.  

	Installation details can be found [here](https://www.virtualbox.org/manual/ch02.html).

2. Install Ubuntu 16.04.  go to [this page](https://www.ubuntu.com/download) and download the ubuntu 16.04 desktop image.

3. Log in and update and upgrade the system.

	```
	sudo apt-get update
	sudo apt-get upgrade
	```
	
4. Install [Guest Additions](https://www.virtualbox.org/manual/ch04.html) in the ubuntu client.
	
5. Install Pip:
	```
	curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
	```

6. Install git and prereqs for virtual environment:

	```
	sudo apt-get git
	sudo apt-get install build-essential python3-dev python3-setuptools python3-tk
	```

7. Install [python virtual environment](https://gist.github.com/FarhadurFahim/73c0fad6350332cef7a653bcd762f08d)

8. Install virtualenv, then create and activate a virtual environment for testing.

	```
	sudo pip install -U virtualenv
	virtualenv <env_name>
	source <env_name>/bin/activate
	```
	
9. Now, in the virtual environment, install pandas, statsmodel, and scikit-learn.

	```
	pip install -U numpy scipy
	pip install -U pandas statsmodels
	pip install -U scikit-learn
	pip install -U matplotlib
	#install natural language tools
	pip install -U nltk
	pip install spacy
	#tensorflow
	pip install --updgrade tensorflow	
	#pytorch
	pip install -U torch torchvision
	#keras
	pip install keras
	```
10. Install ipython and jupyter:

	```
	pip install -U ipython jupyter
	```

11. Test using jupyter notebook.  

	First go to the test folder and create a notebook folder. then run jupyter

	```
	cd <env_name>
	mkdir project
	cd project
	jupyter notebook
	```
	Your browser will open up.  in the browser, you will see this:
	
	![jupyter notebook](https://github.com/JoeDumoulin/CSCD439F17/blob/master/images/2017-09-25T3.32.06PM.png "first page")
	
	Create a new notebook.  On the right of the screen select the 'New' button.
	
	![jupyter notebook](https://github.com/JoeDumoulin/CSCD439F17/blob/master/images/2017-09-25T3.46.32PM.png "select kernel")
	
	Select 'Python 3'.  A new page opens up.  you can type some python into the page and press ctrl-Enter.  the python should execute as in the example below.
	
	![jupyter notebook](https://github.com/JoeDumoulin/CSCD439F17/blob/master/images/2017-09-25T3.52.45PM.png "run python")
	
	Test if matplotlib is working.  Press '+' on the upper left of the screen.  A new code box appears.  copy and paste the following code:
	
	```
	import numpy as np
	import matplotlib.pyplot as plt

	N = 1000
	x = np.linspace(0.0, 10.0, N)
	y = np.random.rand(N)
	plt.title('Uniform Distriibution')
	plt.scatter(x,y)
	plt.show()
	```
	
	 Now run the code (ctrl-Enter) as before.  You should see the following:
	 
	 ![jupyter notebook](https://github.com/JoeDumoulin/CSCD439F17/blob/master/images/2017-09-25T3.59.48PM.png "run python")
	 
	 If you saw the plot, matplotlib is working!
	 
	 
	 

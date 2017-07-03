# Introductory applied machine learning (INFR10069)

# Setting up for DICE

Within this course we will be using Python along with a few open-source libraries (packages). These packages cannot be installed directly, so we will have to create a virtual environment. We are using virtual enviroments to make the installation of packages and retention of correct versions as simple as possible. You can read [here](https://virtualenv.pypa.io/en/stable/) if you want to learn about virtual environments, but this is **not** neccessary for this tutorial.

Now open a terminal and follow these instructions. We are expecting you to enter these commands in **one-by-one**. Waiting for each command to complete will help catch any unexpected warnings and errors. Please read heed any warnings and errors you may encounter. We are on standby in the labs to help if required.

1. Change directory to home and create a virtual enviroment
  * `cd`
  * `virtualenv --distribute virtualenvs/iaml_env`  # Creates a virtual environment called iaml_env

2. Navigate to and activate the virtual enviroment (you will need to activate the virtual environment every time you open a new terminal - this adds the correct python version with all installed packages to your system's `$PATH` environment variable)
  * `cd virtualenvs/iaml_env`
  * `source ./bin/activate`  # Activates the environment, your shell prompt should now change to reflect you are in the `iaml_env` enviornment

3. Install all the python packages we need (once the correct virtual environment is activated, pip install will install packages to the virtual environent - if you're ever unsure which python you are using, type `which python` in the terminal) **WATCH FOR WARNINGS AND ERRORS HERE**. We have split these commands up to encourage you to enter them one-by-one.
   
    * `pip install -U setuptools`  # The -U flag upgrades the current version
    * `pip install -U pip`
    * `pip install yolk`
    * `pip install jupyter`
    * `pip install numpy`
    * `pip install scipy`
    * `pip install matplotlib`
    * `pip install pandas`
    * `pip install statsmodels`
    * `pip install scikit-learn`
    * `pip install seaborn`

You should now have all the required modules installed. Our next step is to make a new directory where we will keep all the lab notebooks, datasets and assignments. Within your terminal:

1. Navigate back to your home directory
    * `cd`
2. Make a new directory and navigate to it
    * `mkdir iaml_2016`
    * `cd iaml_2016`

Now you have two options:

1. We recommend that you directly download a .zip file from https://github.com/agamemnonc/iaml which will contain everything you need and save it in the folder you have just created. You can do this from the terminal by typing:
    * `wget https://github.com/agamemnonc/iaml/archive/master.zip`
    * `unzip master.zip`
2. If **and only if** you are familiar and confident with using Git/GitHub, you can initiliaze a git directory, add the above repo as remote and pull everything into your local directory. Please use this option only if you really know what you are doing. Unfortunately, we won't be able to provide you with Git/Github support if you run into issues with syncing and using version control in general. 

Once you have downloaded the material, you are now ready to start working in the Jupyter environment. First you need to activate the `iaml_env` environment and start a Jupyter Notebook session from within the folder where the material is stored. **Note that you will have to follow this procedure for all labs and assignments.**

1. Navigate home and ensure the `iaml_env` virtualenv is activated
    * `cd`
    * `source virtualenvs/iaml_env/bin/activate` # Activates the environment
2. Enter the directory you downloaded the course material
    * `cd iaml_2016/iaml-master`
3. Start a jupyter notebook
    * `jupyter notebook`
4. This should automatically open your browser
    * Click on `01_Lab_1_Introduction.ipynb` to open it

# Setting up for personal machine (Windows / OS X / Ubuntu)

If you are using a personal machine, you can choose whether to do as above or use the Anaconda distribution (Python version 2.7, choose the appropriate installer according to your operating system). Anaconda is a standard set of packages used in scientific computing which the Anaconda team curate to keep them consistent.

Once the installation is complete, we need to install the Seaborn package which is the only one not included in the distribution. It's also recommended that you set up a virtual environment for this project. This way, if you update anything in your anaconda base install, this virtual environment will remain unchanged. To create a virtual environment called `iaml`, open a Terminal (or Command Prompt window if you are running Windows) and type:

```bash
conda create -n iaml python=2.7 anaconda seaborn=0.7.0
```

Don't forget to activate the virtual environment every time you begin work from a new terminal:

```bash
source activate iaml
```

Once you have finished installed everything, open a terminal (or Command Prompt in Windows), navigate to the folder where you have downloaded the course material and type:

```bash
jupyter notebook
```

Then click on `01_Lab_1_Introduction.ipynb` to open it.

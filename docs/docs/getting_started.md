# Getting Started

To participate in the hands-on tutorials and get started exploring the outputs of the NOC Near-Present Day simulations, you need to choose a platform to perform your analysis. 

Below, we provide instructions for getting started on the National Oceanography Centre's Data Science Platform (**DSP**), [**JASMIN**](https://jasmin.ac.uk) or your personal machine. 

We strongly recommend participants use the **NOC DSP**, given that we have already prepared a shared Python virtual environment which contains all of the required packages for the hackathon.

## **Using the NOC Data Science Platform**

The NOC Data Science Platforms (**DSP**) provide easy access to compute resources including Python, Graphical Processing Units (GPUs) and Unix terminals all from your web browser and without the need to install anything on your computer.

In addition to the local **NOC DSP**, we also have access to a Data Science Platform running on JASMIN (**JASMIN DSP**). This will be used for attendees who do not already have a NOC Linux account.

### Access

=== "NOC DSP"

    You will first need a NOC Southampton Unix account to connect to the **DSP** and then need to apply for **NOC DSP** access.

    Please go to the **NOC DSP** [**Intranet page**](https://nocacuk.sharepoint.com/sites/DigitalOcean/SitePages/Data-Science-Platform.aspx?source=FromArticle#how-do-i-get-access) for details on how to get an account ahead of the Hackathon event.

=== "JASMIN DSP"

    For those attendees without a NOC Linux account, you will be emailed your login credentials to the **JASMIN DSP** following registration.

### Logging In

=== "NOC DSP"

    To login to the **NOC DSP**, connect to [https://notebooks.noc.ac.uk](https://notebooks.noc.ac.uk) and enter your username (without @noc.ac.uk on the end) and Southampton Unix password.

    Next, select the **Default** image, including the Pangeo stack, Matlab, Machine Learning/GPU libraries and the LXDE desktop.

=== "JASMIN DSP"

    To login to the **JASMIN DSP**, connect to [**https://notebooks-ext.noc.ac.uk**](https://notebooks-ext.noc.ac.uk) and enter the username and password sent to you via email ahead of the hackathon.

    Next, select the **Data Science Platform Python Image** image, including the Pangeo stack.

### Downloading Tutorials & Examples

=== "NOC DSP"

    Once you have logged into the **NOC DSP**, you will see the contents of your home directory `/noc/users/{username}` in the lefthand panel.

    Using the **Launcher**, scroll down to **Other** section & open a new **Terminal**, which will open in your home directory.

    Next, let's make a local copy of the `NOC_NPD_Hackathon` GitHub repository containing the tutorials and example Jupyter Notebooks used in the Hackathon.

    ```bash
    git clone https://github.com/NOC-MSM/NOC_NPD_Hackathon.git
    ```

    Once the download is complete, you will see that a new `NOC_NPD_Hackathon` directory has been added to your home directory.

    Inside `NOC_NPD_Hackathon`, you will find:

    * `/docs` - Documentation source files for this [**NPD Hackathon website**](https://noc-msm.github.io/NOC_NPD_Hackathon/)

    * `/tutorials` - Jupyter Notebooks for Tutorials 0-2

    * `/examples` - Jupyter Notebook Examples for Science Themes

=== "JASMIN DSP"

    Once you have logged into either **JASMIN DSP**, you will see the contents of your home directory `/home/{username}` in the lefthand panel.

    Using the **Launcher**, scroll down to **Other** section & open a new **Terminal**, which will open in your home directory.

    Next, let's make a local copy of the `NOC_NPD_Hackathon` GitHub repository containing the tutorials and example Jupyter Notebooks used in the Hackathon.

    ```bash
    git clone https://github.com/NOC-MSM/NOC_NPD_Hackathon.git
    ```

    Once the download is complete, you will see that a new `NOC_NPD_Hackathon` directory has been added to your home directory.

    Inside `NOC_NPD_Hackathon`, you will find:

    * `/docs` - Documentation source files for this [**NPD Hackathon website**](https://noc-msm.github.io/NOC_NPD_Hackathon/)

    * `/tutorials` - Jupyter Notebooks for Tutorials 0-2

    * `/examples` - Jupyter Notebook Examples for Science Themes

!!! note

    Editing any of the tutorial or example notebooks / creating new notebooks in your cloned `NOC_NPD_Hackathon` will not impact the original GitHub repository.

### Configuring Jupyter Kernel

To get started running the tutorial notebooks, you need to set-up a Jupyter Kernel - the computational engine for your Python code.

We have already installed all of the necessary packages for the tutorial notebooks in a shared Conda environment accessible by everyone on both the **NOC** and **JASMIN DSPs**.

??? info "What is Conda?"

    Conda is a package manager which allows users to install software packages into dedicated virtual environments. This enables us to create different virtual environments, including different versions of the same software, for separate projects. 

    Virtual environments can also be shared between users by exporting them to a `.yml` file, which can be used to re-create the environment on another computer.

    Conda is especially suited to scientific software applications since it can handle complex dependencies and pre-compiled binaries (e.g., netCDF4 to read netCDF files)

    There are many different types of Conda package manager available:

    * **Anaconda** - Includes lots of common software, requires paid license.
    * **Miniconda** - Minimal version of Anaconda.
    * **Miniforge** - Minimal Conda package manager using only conda-forge (community) channel, exempt from licensing above.

To install a Jupyter kernel for the `env_nemo_npd` shared Conda environment, run the following command in your terminal (this applies to both the **NOC** and **JASMIN DSPs**):

```bash
/groups/npd-workshop/env_nemo_npd/bin/python -m ipykernel install --user --name env_nemo_npd --display-name "NPD Hackathon (env_nemo_npd)"
```

This will add a new Jupyter kernel called env_nemo_npd to your kernelspec.

Now, when we open a Jupyter Notebook (e.g., `tutorials/tutorial_0_getting_started_with_xarray.ipynb`), we will see a **Select Kernel** drop-down menu and included in the list is `NPD Hackathon (env_nemo_npd)` kernel.

## **Using a Personal Machine**

### Downloading Tutorials & Examples

Let's start by making a local copy of the `NOC_NPD_Hackathon` GitHub repository containing the tutorials and example Jupyter Notebooks used in the Hackathon.

After opening a new **Terminal** window, navigate to the directory into which you would like to clone the NPD Hackathon repository and run the following command:

```bash
git clone https://github.com/NOC-MSM/NOC_NPD_Hackathon.git
```

Once the download is complete, you will see that a new `NOC_NPD_Hackathon` directory has been added to your chosen directory.

Inside `NOC_NPD_Hackathon`, you will find:

* `/docs` - Documentation source files for this [**NPD Hackathon website**](https://noc-msm.github.io/NOC_NPD_Hackathon/)

* `/tutorials` - Jupyter Notebooks for Tutorials 0-2

* `/examples` - Jupyter Notebook Examples for Science Themes

!!! note

    Editing any of the tutorial or example notebooks / creating new notebooks in your cloned `NOC_NPD_Hackathon` will not impact the original GitHub repository.

### Creating the NPD Hackathon Conda Environment

If you do not already have an installation of miniconda or miniforge on your local machine, see the instructions below to install miniforge3:

??? info "Installing Miniforge"

    **Miniforge** is a minimal conda installer that defaults to the **conda-forge** ecosystem. It is lightweight, open-source, and recommended for scientific Python workflows.

    **Download Miniforge**

    Follow instructions at [**https://github.com/conda-forge/miniforge**](https://github.com/conda-forge/miniforge).

    For Unix-like Platforms (macOS, Linux, WSL): 

    ```bash
    wget "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-$(uname)-$(uname -m).sh"
    ```

    **Creating the Base Environment**

    Run the installer by running the following command:

    ```bash
    bash Miniforge3-$(uname)-$(uname -m).sh
    ```

    It is recommended to accept the default location (`~/miniforge3`) and only accept the changes to your `~/bashrc` file if you are happy for the base environment to be activated every time you log in (this is not recommended for JASMIN use).

    **Activating the Base Environment**

    Once you have successfully installed miniforge3, activate your base environment:

    ```bash
    source ~/miniforge3/bin/activate 
    ```

The `NOC_NPD_Hackathon` GitHub repository includes the `environment_npd_hackathon.yml` file required to reproduce the Conda virtual environment needed to run the tutorial and example notebooks.

From your Conda base environment, run the following command to create a new Python virtual environment using the `.yml` file:

```bash
conda env create --name env_nemo_npd --file environment_npd_hackathon.yml
```

This will take a bit of time to install all of the dependencies from the **conda-forge** channel and then **OceanDataStore** and **nemo_cookbook** packages using `pip`.

### Configuring Jupyter Kernel:

Once you have successfully created the `env_nemo_npd` virtual environment, you next need to set-up a Jupyter Kernel - the computational engine for your Python code.

To install a Jupyter kernel for the `env_nemo_npd` shared Conda environment, you first need to activate your `env_nemo_npd` environment from the base environment using:

```bash
conda activate env_nemo_npd
```

Then, run the following command to add a new Jupyter kernel called env_nemo_npd to your kernelspec:

```bash
python -m ipykernel install --user --name env_nemo_npd --display-name "NPD Hackathon (env_nemo_npd)"
```

Now, when we open a Jupyter Notebook (e.g., `tutorials/tutorial_0_getting_started_with_xarray.ipynb`), we will see a **Select Kernel** drop-down menu and included in the list is `NPD Hackathon (env_nemo_npd)` kernel.

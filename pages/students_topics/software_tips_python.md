---
layout: default
title: Python
parent: Software Tips
grand_parent: To my students
nav_order: 1
---

### 1. Maintaining conda environment

Python packages can evolve rapidly with time. It can happen that once you update an package, many of your codes crash. Therefore, it could be wise to maintain some virtual environment that the packages are *frozen* (i.e., you never update them). I usually maintain one of such virtual environment for each project (e.g., when preparing the analyses for one paper) for the sake that the results can be easily reproduced.
{: .fs-2 }

We can create such virtual environments using the [Anaconda](https://www.anaconda.com/) package. For linux users, go to the [Download page](https://www.anaconda.com/products/distribution#Downloads) to download the installer, which is a `.sh` file. You can move it to the directory that you want to install it, and then type
{: .fs-2 }

```
chmod +x installer.sh
./installer.sh
```
{: .fs-1 }

This should be able to complete the installation.
{: .fs-2 }

Then you can create/remove an conda environment by typing
{: .fs-2 }

```
conda create --name environment_name
conda remove --name environment_name --all
```
{: .fs-1 }
and then (de-)activate the environment by typing
{: .fs-2 }
```
conda activate environment_name
conda deactivate
```
{: .fs-1 }
After you activate an environment, you can install/remove a package from that environment by typing
{: .fs-2 }

```
# installing package
pip install packagename

# removing packages
conda remove --name environment_name packagename
```
{: .fs-1 }

To list all the environment you have, type:
{: .fs-2 }
```
# list available environments
conda info --envs

# list all available packages in the current environment
conda list
```
{: .fs-1 }

### 2. Using Jupyter Notebook from a Remote Server

You need to install Jupyter Notebook in the remote sever (e.g., under a conda environment) by typing
{: .fs-2 }

```
pip install jupyter
```
{: .fs-1 }

At the remote server, launch Jupyter notebook by typing
{: .fs-2 }

```
jupyter notebook --no-browser --port=XXXX
```
{: .fs-1 }
Remember to activate the conda environment in the remote server before doing this step.
{: .fs-2 }

Here `XXXX` is a for digit port number, for example, 8080.
In the local computer, setup ssh tunnel by typing
{: .fs-2 }

```
ssh -L XXXX:localhost:XXXX remoteUSRNAME@remoteDOMAIN
```
{: .fs-1 }

Then you can open a web browser in the local computer, and connect to `http://localhost:XXXX/logout` to launch your remote Jupyter Notebook.
{: .fs-2 }

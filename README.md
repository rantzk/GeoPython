# GeoPython
## Repository for how to's, tips, code.
### Documenting installing, using and coding with Geo Python. 
##### 
[Installation: Anaconada, Jupyter, PYQgis](#Installation)  





<a name="Installation"/>
## "How to" installing of GeoPython Environment:
## Anaconda with Jupyter Notebook, PYqgis, Spyder IDE, and more

On win7, 10 64bit (with existing qgis and python installation. Might be easier without)

1.Download and Install Anaconda [Download ](https://www.anaconda.com/distribution/)

2. Test that the Anaconda´s package manage called conda works by [opening a command prompt as a admin user](http://www.howtogeek.com/194041/how-to-open-the-command-prompt-as-administrator-in-windows-8.1/) and running command conda --version

3. Check JUPYTER in anaconda cmd prompt: jupyter notebook

4. Create a fresh environment: conda create --name MyEnv

5. conda activate MyEnv

6. Install packages: (qgis first)

7. conda install qgis --channel conda-forge

8. Run qgis from the Anaconda cmd:
conda activate MyEnv
qgis

9. Now try to open the jupyter notebook from the new env.

10. If it  was open ok  then try to switch to the new env in the "new" menu

11. Test if Pyqgis works:
In python try: from qgis.core import *
import PyQt5.QtCore #should not raise any error

**If its not working see ****[troubleshooting** ](#bookmark=id.7cdhj4v4j7xw)

Optional:

12. Install **Spyder **IDE on the new env with pyqgis: 
conda install -c anaconda spyder
(or try the [kernel ](https://github.com/spyder-ide/spyder/wiki/Working-with-packages-and-environments-in-Spyder#the-modular-approach)only, did not work with import)

And check if it works with qpy by spyder from the new env 

13. Install **git **in the new env: conda install -c anaconda git

    1. git config --global user.name "Ran Tzkhori"

    2. git config --global user.email "email@example.com"

    3. git config --global credential.helper wincred

    4. Create new repo on github web or by: [git init](https://git-scm.com/docs/git-init)

    5. If by web than clone it (after copying the url) : git clone "paste your URL here"

    6. Go to the git: cd "name" and do git status

14. After making changes in files local git:

    7. git commit -m "added notes"

    8. git pull

    9. git push

15. Install** ****[nbextensions** ](https://jupyter-contrib-nbextensions.readthedocs.io/en/latest/install.html)for improving notebook

Troubleshooting:

1. Error in import module in notebook but work in cmd: the only thing that helped was: (and it also enabled opening notebook from the new env.) 

conda activate testenv

*pip install jupyter notebook*

conda install ipython

conda install notebook

python -m ipykernel install --user --name testenv

If did not help then the sources was:
1.

*I was able to solve the problem by installing a jupyter notebook within my new environment.*

*First activate your environment:*

*activate py36** (I called my environment py36)*

*Second install jupyter notebook within that environment:*

*pip install jupyter notebook*

*Then launch our jupyter notebook*

*jupyter notebook*

2. If non help Also other things that might impact it such [as](https://stackoverflow.com/questions/59538207/modulenotfounderror-sklearn-in-jupyter-notebook)

That was related to the path of the python and the system.path on the computer, running some ipykernel install commands.

 



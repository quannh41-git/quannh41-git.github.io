# Create Sphix blog hosting on Github
## Install packages

### *Sphinx*
Install sphinx
```
sudo apt install python3-pip
pip install sphinx
```
If cannot install `sphinx` directly on your physical machine, you can create virtual environment:
- First create a Python 3 virtual environment using the venv module included with Python 3
```
$ python -m venv py3-sphinx
```
- Activate the environment
```
source py3-sphinx/bin/activate
```
- With the virtual environment activated, install Sphinx
```
(py3-sphinx) $ pip install sphinx
```
- Verify that Sphinx is installed
```
(py3-sphinx) $ sphinx-build --help
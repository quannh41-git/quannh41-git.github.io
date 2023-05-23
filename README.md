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
```

## Create Sphix document blog
Create a new directory for your project
```
(py3-sphinx) $ mkdir sphinx
```
Create a starting project for a `Sphinx` documentation project
```
(py3-sphinx) $ cd sphinx
(py3-sphinx) $ sphinx-quickstart
```
Install `sphinx_rtd_theme`
```
$ pip install sphinx-rtd-theme
```
To use the theme in your Sphinx project, you will need to edit your `conf.py` file's `html_theme` setting:
```
html_theme = 'sphinx_rtd_theme'
```
Build project
```
(py3-sphinx) $ make html
```
- The preview blog will appear on directory `sphinx/_build/html/index.html` 
## Deploy to Github
Create `docs` folder to contain the html code
```
$ mkdir docs
```
Copy all files from `sphinx/_build/html/` to `docs`
```
$ cp -r sphinx/_build/html/* docs
```
Push code to github 
```
git push origin master
```
On github repo, choose `Settings\Pages\Build and deployment\Branch\...docs`
## References
- [Set Up Sphinx with Python](https://www.docslikecode.com/learn/01-sphinx-python-rtd/)
- [sphinx_rtd_theme](https://github.com/readthedocs/sphinx_rtd_theme)
- [Youtube - Sphinx Documentation Tool](https://www.youtube.com/watch?v=5s3JvVqwESA)
- [Youtube - Python documentation website with Sphinx and GitHub](https://www.youtube.com/playlist?list=PLzHdTn7Pdxs4QhD7gJMbJQ59g4pLpmNWJ)
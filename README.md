# Learn Flask in a scientific way

This repository contains the code for the mean review collector.

## What is built in this project

We are building a web application that allows researchers to share mean reviews they received on their papers with others:


```bash
sudo apt install python3-pip
sudo apt install libpython3.8-dev # change the version number as per your python

mkdir devops
git clone <source code repo>
python3 -m pip install virtualenv
virtualenv --python=python3 ~/devops/.venv

source ~/devops/.venv/bin/activate  # activates python virtual environment
cd mean-review-collector
pip install -r requirements.txt

flask run



# to run test
pytest --junitxml=test-reports/test-results.xml --cov=app --cov-report=xml --cov-report=html
# pylint checks linting and quality of code
pylint app/ tests/ -r n --msg-template="{path}:{line}: [{msg_id}({symbol}), {obj}] {msg}" | tee pylint.txt


# to build the python app to wheel file
python3 setup.py sdist bdist_wheel
```

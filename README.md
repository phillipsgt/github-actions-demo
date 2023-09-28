![Python application test with Github Actions](https://github.com/noahgift/github-actions-demo/workflows/Python%20application%20test%20with%20Github%20Actions/badge.svg)

# github-actions-demo
This is a repo for building out Github Actions and Tricks.  I test multiple clouds and multiple versions of Python.


[Demo Video of this repo](https://www.youtube.com/watch?v=4gbUYOgALik)

### To use my project you can do this

Create a virtualenv
```python3 -m venv ~/.github-actions-demo```

Source it
```source ~/.github-actions-demo/bin/activate```

### Steps involved in setting up this project

* Create a Github repo (if not already created)
  - Create new AWS Cloud9 environment

```bash
install:
	pip install --upgrade pip &&\
		pip install -r requirements.txt

test:
	python -m pytest -vv test_hello.py


lint:
	pylint --disable=R,C hello.py

all: install lint test
```


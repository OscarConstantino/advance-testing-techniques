# advance-testing-techniques
This is a repo for advance testing

## Setup Project

 1. Create and source virtualenv

```bash
virtualenv ~/.advance-testing
source ~/.advance-testing/bin/activate
```

 2. Create scaffold

```bash
touch Makefile && touch test_hello.py && touch hello.py && requirements.txt
```

 3. Populate `Makefile`

```bash
install:
    pip install --upgrade pip &&\
        pip install -r requirements.txt

test:
    python -m pytest -vv -cov=hello -cov=hellocli test_hello.py

lint:
    pylint --disable=R,C hello.py hellocli.py

all: install lint test

```

### How to debug

1.- print
2.- pdb
3.- testing


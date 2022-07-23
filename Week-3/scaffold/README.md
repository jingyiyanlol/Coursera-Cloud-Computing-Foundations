# Git Clone and Create Scaffold for the Project in CLoud9/ Azure Cloud Shell/ GCP

## Git Clone
* In the bash terminal in Cloud9, type `ssh-keygen -t rsa`. Click ENTER when prompted to provide the filepath and passphrase if there isn't a need to specify them.
* Then type `cat /home/ec2-user/.ssh/id_rsa.pub` to print out the public key string
* Copy the SSH public keys and go back to GitHub > Settings > SSH and GPG Keys. Create a new SSH key by pastng the public key string in the clipboard.
* Go back to Cloud9 and type in bash terminal:
    ```bash
    git clone git@github.com:jingyiyanlol/Coursera-Cloud-Computing-Foundations.git
    ``` 

## Create Scaffold
* Go to the directory of the project
    ```bash
    cd Coursera-Cloud-Computing-Foundations/Week-3/scaffold
    ```
* create the scaffold using touch command
    ```bash
    touch .gitignore
    touch Makefile
    touch hello.py
    touch test_hello.py
    touch requirements.txt
    ```
## Create Virtual Environment
* Create a hidden virtual environment by typing in the bash terminal:
    ```bash
    python3 -m venv ~/.scaffold
    ```
* Activate the virtual environment
    ```bash
    source ~/.scaffold/bin/activate
    ```
* Type `which python` to check if we are indeed using the correct python

## Modify the Makefile
* Open the Makefile and convert it to tabs

    ![conver-makefile-to-tab](https://user-images.githubusercontent.com/92244042/179404570-3f0ed444-f736-4b51-9d72-3119294ab951.png)

* Paste the following into the Makefile and make changes where neccessary
```
install:
	pip install --upgrade pip &&\
		pip install -r requirements.txt
		
format:
	black *.py
	
lint:
	pylint --disable=R, C hello.py
	
test:
	python -m pytest -vv --cov=hello test_hello.py

all: install format lint test
```

## Add some dependencies for the project into requirements.txt
```
pylint
pytest
click
black
pytest-cov
```

## Building Project

1. **Run the Makefile**
    ```bash
    make install
    ```

2. **Write codes into the python scripts and test scripts**
    To run the scripts, type: `python hello.py` or `python test_hello.py`

3. **Check for errors using Lint**
    ```bash
    make lint
    ```

4. **Clean up the formatting**
    ```bash
    make format
    ```

5. **Test the code**
    ```bash
    make test
    ```

6. **Run all**
    ```bash
    make all
    ```

## Push changes to GitHub

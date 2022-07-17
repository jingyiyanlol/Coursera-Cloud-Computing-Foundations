# Git Clone and Create Scaffold for the Project in Cloud9 

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

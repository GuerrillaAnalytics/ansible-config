This project is where I maintain a reproducible setup of my home and work machines using [Ansible](https://www.ansible.com/).

To run the configuration, set up your system as detailed below and then type the following. 'password' is your machine's admin password. 
```
ansible-playbook -i ./hosts  master.yml --extra-vars "ansible_become_pass=<password>"
```
# Motivation
Reproducibility is key to doing traditional science. Results that cannot be reproduced are useless. Data Science is no different. 

# Set up your system
* Install virtualenv as described [here](https://virtualenv.pypa.io/en/latest/installation/) 
* Create and activate a python virtual environment for this project's installations
```
virtualenv --python=python3 .venv
```

* Install ansible.
* Install ansible roles using the requirements file.
```
ansible-galaxy install -r requirements.yml
```

* Install project Python requirements inside your virtualenv
```
pip install -r requirements.txt
```

# ansible-config
ansible configuration of work and home machine

To run type:

ansible-playbook -i ./hosts  master.yml --extra-vars "ansible_become_pass=<password>"


# Set up your system
Install virtualenv if not already installed

virtualenv --python=python2.7 .venv

Install all ansible galaxy roles from requirements.yml

ansible-galaxy install -r requirements.yml

# Setup on mac
brew install python2
pip2 install -U virtualenv

# Create a python virtual environment
virtualenv --python=python3 .venv


# Enable the virtual environment
source .venv/bin/activate


# Then anything we intall with pip will be
# inside that virtual environment

pip install -r requirements.txt

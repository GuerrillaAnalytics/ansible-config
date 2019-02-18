# ansible-config
ansible configuration of work and home machine

ansible-playbook -i ./hosts  master.yml --extra-vars "ansible_become_pass=<password>"

# Setup on mac
brew install python2
pip2 install -U virtualenv

# Create a python virtual environment
virtualenv .venv
# Enable the virtual environment
source .venv/bin/activate

# Then anything we intall with pip will be
# inside that virtual environment
pip install ansible
pip install -r requirements.txt



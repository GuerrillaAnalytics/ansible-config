This project is a simple reproducible setup of my home machines using [Ansible](https://www.ansible.com/).

To run the configuration, set up your system as detailed below and then type the following.
```

```
# Motivation
Reproducibility is key to doing traditional science. Reproducibility is also key to doing _Data Science_ well in a way that you can explain your results, iterate quickly and not waste time configuring the complex mix of tools used in Data Science work.

See more about reproducible data science at [Guerrilla Analytics](https://guerrilla-analytics.net).

# Set up your system
* Install virtualenv as described [here](https://virtualenv.pypa.io/en/latest/installation/)
* Create and activate a Python virtual environment for this project's installations
```
virtualenv --python=python3 .venv
```

* Install this project's Python requirements inside your virtualenv
```
pip3 install -r requirements.txt
```

* Install ansible roles using the ansible requirements file.
```
ansible-galaxy install -r requirements.yml
```

* add this line code to ```inventory.ini```.

```
localhost ansible_become_pass=ZZZZ
```
where ZZZZ is the sudo password for your local machine

* encrypt your new inventory.ini file
```
ansible-vault encrypt inventory.ini
```

# Supported tools
* [Docker](https://hub.docker.com/)
* Terminal configuration with useful information and colour coding
* [apt-file](http://manpages.ubuntu.com/manpages/precise/man1/apt-file.1.html)
* [xclip](http://manpages.ubuntu.com/manpages/xenial/man1/xclip.1.html) often useful in scripting

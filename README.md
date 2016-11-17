# ansible-playbook-dolibarr

## Prérequis

 * python 2.7 ou 3.4+
 * python-pip
 * python-virtualenv
 * ansible 2.0+

## Préparation

    # ssh-keygen -t rsa
    # ssh-copy-id -i ~/.ssh/id_rsa.pub root@machine-cible

### Debian

    # apt-get install git python python-pip python-virtualenv python-dev build-essential
    # git clone https://github.com/linkdd/ansible-playbook-dolibarr.git
    # cd ansible-playbook-dolibarr
    # git submodule update --init
    # cd ..
    # virtualenv venv
    # . ./venv/bin/activate
    (venv)# pip install ansible markupsafe

## Configuration

Editer les fichiers suivants :

 * ``hosts`` : pour préciser les machines sur lesquelles installer les différents composants
 * ``group_vars/*/main.yml`` : pour personnaliser la configuration des différents composants
 * ``host_vars/*/main.yml`` : pour personnaliser la configuration des différentes machines

## Lancer le playbook

    (venv)# cd ansible-playbook-dolibarr
    (venv)# ansible-playbook -i hosts site.yml

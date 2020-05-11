Malkova project using Django + Virtualend + Gunicorn + Supervisor

-- Clone project and configure.

-- 1. Configure Virtualenv

- 1.1 Install env:

apt install python3-venv && cd /<dir>/malkova
python3 -m venv env

- 1.2 Active and install packages:

ln -s env/bin/activate && . activate
pip install -r requirements.txt

- 1.3 Export pip packages: 

pip freeze > requirements.txt

-- 2. Configure SUPERVISOR

- 2.1 Install supervisor:

sudo apt install supervisor

- 2.2 Configure supervisor:

sudo su
ln -s <dir>/malkova/config/gunicorn.conf /etc/supervisor/conf.d/gunicorn.conf
supervisorctl update && supervisorctl restart all


Finish \õ/

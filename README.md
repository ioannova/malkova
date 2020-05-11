## Malkova project using Django + Virtualend + Gunicorn + Supervisor

### Clone project and configure.

- Clone project Malkova

```
cd /<dir for project> && git clone git@github.com:ioannova/malkova.git
```

- Install and configure Virtualenv

```
apt install python3-venv && cd /<dir>/malkova
python3 -m venv env
ln -s env/bin/activate && . activate
pip install -r requirements.txt
```
- Exporting new packages installed in env
```
pip freeze > requirements.txt
```

- Install and configure Supervisor
```
sudo su && sudo apt install supervisor
ln -s <dir>/malkova/config/gunicorn.conf /etc/supervisor/conf.d/gunicorn.conf
supervisorctl update && supervisorctl restart all
```

Django is running in address 127.0.0.1:8000 \õ/

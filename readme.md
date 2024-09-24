# How to create a django project

### Step-1
Django - Create Virtual Environment.

```
python -m venv .venv
```
### Step-2
Active Virtual Environment.
```
.venv\Scripts\activate
```

### Step-3
Install django
```
pip install django
```
Django install sucessfully.

### create django project directory
```
# run this command

django-admin startproject projectName
```

***
***

## Run server
Notes :- \
Active virtual environment and go to the project directory.
```
cd directory/name
```
Check if manage.py is available then run this command.
```
python .\manage.py runserver
```
In terminal there is an worning. run this command.

```
python manage.py makemigrations
python manage.py migrate
```

## Create Superuser | Administrator
run this command
```
python manage.py createsuperuser
```
After enter UserName or Password


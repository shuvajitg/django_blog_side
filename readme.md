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
```python
python manage.py createsuperuser
```
After enter UserName or Password

## setup tailwind css goto this site 
https://django-tailwind.readthedocs.io/en/latest/installation.html

### After in settings.py set media path

copy this and pest into your settings.py file
```python
MEDIA_URL = '/media/'
MEDIA_ROOT = os.path.join(BASE_DIR, 'media')
```

### Set static path

Copy this and pest as itis into your urls.py file
```python
from django.conf import settings
from django.conf.urls.static import static

urlpatterns = [
    path('admin/', admin.site.urls),
    #...
    #...
    #...
]+ static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT) # set static url settings
```

## create new app or component 
if you want to create a new app or component you can run this command 
```
python manage.py startapp app_name
```
in this app create a new file urls.py and copy urls.py from your main project and concogur as par your app

After then goto your settings.py file and mention your app

```
INSTALLED_APPS = [
    `#....`,
    `#....`,
    `app_ame`
]
```
then goto your main project url file mention your app url like this

```python
from django.contrib import include

urlpatterns = [
    #.......
    
    path('app_name/', include('app_name.urls') ),
    
]
```

mention your app in settings.py 

```python
TEMPLATES = [
    {
        'DIRS': [os.path.join(BASE_DIR, 'templates')],
        
    },
]
```
'DIRS': [os.path.join(BASE_DIR, 'templates')],\
``after this settings you can create template in all app``

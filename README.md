# pythonproject_celery
Projto django implementado com celery e deploy no heroku-baseado no pythonpro - Renzo Nuccitell
Example Django project using Celery
pythonpro/celery.py

#pythonpro/
This is a project in itself, created using django-admin.py startproject pythonpro, and then the settings module (pythonpro/settings.py) was modified to add appdemo to INSTALLED_APPS

proj/celery.py
This module contains the Celery application instance for this project, we take configuration from Django settings and use autodiscover_tasks to find task modules inside all packages listed in INSTALLED_APPS.

appdemo/
Example generic app. This is decoupled from the rest of the project by using the @shared_task decorator. This decorator returns a proxy that always points to the currently active Celery instance.



# pythonproject_celery
Projto django implementado com celery e deploy no heroku-baseado no pythonpro - Renzo Nuccitell
Example Django project using Celery
pythonpro/celery.py

<h2>#pythonpro/</h2>
This is a project in itself, created using django-admin.py startproject pythonpro, and then the settings module (<span style="background-color: pythonpro/settings.py</span>) was modified to add appdemo to INSTALLED_APPS

<h2>pythonpro/celery.py</h2>
This module contains the Celery application instance for this project, we take configuration from Django settings and use autodiscover_tasks to find task modules inside all packages listed in <mark>INSTALLED_APPS</mark>.

<h2>appdemo/</h2>
Example generic app. This is decoupled from the rest of the project by using the @shared_task decorator. This decorator returns a proxy that always points to the currently active Celery instance.

<



# pythonproject_celery
Projto django implementado com celery e deploy no heroku-baseado no pythonpro - Renzo Nuccitell
Example Django project using Celery
pythonpro/celery.py

<h2>#pythonpro/</h2>
<p>This is a project in itself, created using <span style="border: 1px solid black">django-admin.py startproject pythonpro</span>, and then the settings module (<span style="background-color: pythonpro/settings.py</span>) was modified to add appdemo to INSTALLED_APPS</p>

<h2>pythonpro/celery.py</h2>
This module contains the Celery application instance for this project, we take configuration from Django settings and use autodiscover_tasks to find task modules inside all packages listed in <span style="border: 1px solid black">INSTALLED_APPS</span>.

<h2>appdemo/</h2>
Example generic app. This is decoupled from the rest of the project by using the @shared_task decorator. This decorator returns a proxy that always points to the currently active Celery instance.

<h2>Installing requirements</h2>
<i>The settings file assumes that rabbitmq-server is running on localhost using the default ports. More information here</i>:
<a href="url">http://docs.celeryproject.org/en/latest/getting-started/brokers/rabbitmq.html </a>

In addition, some Python requirements must also be satisfied:
<div style="border: 1px solid black">$ pip install -r requirements.txt</div>

<h2>Starting the worker</h2>
<div style="border: 1px solid black">$ celery -A proj worker -l INFO</div>

<h2>Running a task</h2>
$ python ./manage.py shell

>>> from demoapp.tasks import add, mul, xsum

>>> res = add.delay(2,3)

>>> res.get()
5





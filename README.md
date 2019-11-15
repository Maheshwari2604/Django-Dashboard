# Django-Dashboard

Under Process
Installation

pip install django-jet
or

easy_install django-jet

####

Edit in Settings.py file:

INSTALLED_APPS = ( ... 'jet', 'django.contrib.admin', ... )

TEMPLATES = [ { 'BACKEND': 'django.template.backends.django.DjangoTemplates', 'DIRS': [], 'APP_DIRS': True, 'OPTIONS': { 'context_processors': [ ... 'django.template.context_processors.request', ... ], }, }, ]

from django.conf import global_settings

TEMPLATE_CONTEXT_PROCESSORS = global_settings.TEMPLATE_CONTEXT_PROCESSORS + ( 'django.core.context_processors.request', )
Add URL-pattern

urlpatterns = patterns( '', url(r'^jet/', include('jet.urls', 'jet')), # Django JET URLS url(r'^admin/', include(admin.site.urls)), ... )
Create database tables:

python manage.py migrate jet
or

python manage.py syncdb
Collect static if you are in production environment:

python manage.py collectstatic

Further Installtion Process you will get on this link:

https://jet.readthedocs.io/en/latest/getting_started.html

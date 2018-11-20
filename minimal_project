import os
import sys
from django.conf import settings
from django.core.wsgi import get_wsgi_application

DEBUG = os.environ.get('DEBUG', 'on') == 'on'
SECRET_KEY = os.environ.get('SECRET_KEY', os.urandom(32))
ALLOWED_HOST = os.environ.get('ALLOWED_HOSTS', 'localhost').split(',')


settings.configure(
    DEBUG = DEBUG,
    SECRET_KEY = 'THISASECRETKEY',
    ROOT_URLCONF = __name__,
    ALLOWED_HOST = ALLOWED_HOST,
    MIDDLEWARE_CLASSES = (
        'django.middleware.common.CommonMiddleware',
        'django.middleware.csrf.CsrfViewMiddleware',
        'django.middleware.clickjacking.XframeOptionsMiddleware',
    ),
)

from django.urls import path
from django.http import HttpResponse

def index(request):
    return HttpResponse('Hello world')


urlpatterns = (
    path('', index),
)

application = get_wsgi_application()

if __name__=="__main__":
    from django.core.management import execute_from_command_line
    execute_from_command_line(sys.argv)
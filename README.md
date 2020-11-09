# firstDjangoProject
Getting started with Django

## Getting started:
1- cd into the folder that contains the Django project (Charef's file).
2- Run the command "pipenv shell" which stands for activating the virtual environment (again, should check if this has to be done each time).
3- In order to exit the virtual environment I have to run "deactivate" and then "exit".
4- Installing Django has to be through pipenv (Should ask Charef why) by running the command "pipenv install django".
5- In order to start a new Django project, I had to type and run "django-admin startproject <Project Name>".

## Starting the Server:
1- cd inside the folder that contains "manage.py" (run dir to make sure I am inside this folder).
2- ctrl + C gets you out of the server.

P.S. Execute the command "pipenv install" to install the virtual environment (I'm not sure if I have to do this each time?)

## The "Hello World" in Django:
1- Run "python manage.py startapp <App Name>".
2- Install the app by adding its name in <Project Name> => settings.py under INSTALED_APPS. This step gives Django the ability to recognize the app.
3- <Project Name> => urls.py to indicate the path of the app. import "include" from "django.urls" library. and write the following line inside urlpatterns:
  path("App-Name/", include('App-Name.urls')),
4- Go to <App Name> => views.py and add:
  from django.http import HttpResponse
  def index(response):
      return httpResponse("<h2>Hello World</h2>")
5- Creat the file urls.py inside the folder <App Name> and write:
  from django.urls import path
  from . import views 
  urlpatterns = [ path('', views.index, name = "index")]

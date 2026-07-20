# Django_Framework_Pentagon_Space

Table of Contents :

1. [Django](./Django)
2. [MVT Architecture](./MVT-Architecture)

# Django 

* **Django :-** Django is a free open source powerful web framework written in python to build applications fastly, scalable and secure websites.

* Django was developed by Adrian Holoraty and Simon Willison on 2003 and open sourced on 2005.
* Django are of two types :-
  
    1.  Django Web Framework - for full stack development.
    2.  Django rest Framework - for backend development.
 
### * *History :-*
  
* Django name came from famous Jazz guitarist named Django Reinhardt who was the favourite musician of Adrian and Simon.
* News Company (Lawrence Journal world (US)).

### * **Framework :-**

* **Framework :-** Framework is a ready made set of tools, functions and rules. It helps to develop applications faster and better without starting from scratch.
* Framework allows us to focus on logics, it will take care of the basic configurations(Database connectivity and security).

* Framework examples:-

  1. Django - Flask for python
  2. spring - springboot for java
  3. Express.js for Javascript/Node.js

* Difference between Django and Flask :-

<table>
  <tr>
    <td>Django</td>
    <td>Flask</td>
  </tr>
  <tr>
    <td>Full Stack web Framework</td>
    <td>Micro web Framework</td>
  </tr>
  <tr>
    <td>More built-in tools</td>
     <td>Few built-in tools</td>
  </tr>
  <tr>
    <td>Used to build Complex applications</td>
    <td>Used for building medium sized applications</td>
  </tr>
  <tr>
    <td>Built-in admin panel</td>
    <td>No Built-in admin panel</td>
  </tr>
  <tr>
    <td>Django supprts dynamic HTML</td>
    <td>No dynamic HTML support</td>
  </tr>
</table>

## MVT Architecture

* **MVT -** Stands fo *Model View Template*.
* Model - refers to *database*
* View - refers to *logics or backend*
* Template - refers to *frontend*

### * Model :-

* Model Represents the database structure and data logic.
* It defines *table*.
* It defines *Fields* (columns in SQL).
* It communicates with database.
* It handles CRUD operations.

### * Views :- 

* View is a business logic layer.
* It handles requests
* It Takes Request from the user, &process, &it returns Response to the user.
* It communicates with model.
* It sends data to the frontend(Template).

### * Template :-

* Template is a presentation layer(HTML).
* It display the data and handles UI.

* Creation of Django folder

cmd >>
  >> python -m venv test

  >> test\scripts\activate

  >> pip install django

  >> django-admin --version

* Creation of Project

  >> django-admin startproject first-project
  
  >> cd first-project
  
  >> python manage.py startapp facebook

* Run Server:-

  >> python manage.py runserver

* Request Response Cycle :-

* Request Response Cycle is a process where client sends a request to the server, Django will process it and returns response.
* Types of Request:

  1. GET - To retrieve Data
  2. POST - Creating a new Data
  3. PUT - To update existing Data
  4. PATCH - To update Partially
  5. DELETE - To delete existing Data.

* Types of Response :

  1. HTTP Response -> It return a plain Text
  2. Render -> It return a HTML Page
  3. Redirect -> It redirects user to different pages.
  4. JSON Response -> It returns JSON Data(useful for APIs)
 
* Returning HTTP Response :-

  views.py

      from django.http import HttpResponse
      def home(request):
          return HttpResponse("Welcome to Home page")
      def about(request):
          return HttpResponse("This is about page")

  urls.py

      from django.urls import path
      from facebook.views import home,about
      urlpatterns=[
          path('admin/',admin.site.urls),
          path('home/',home),
          path('about/',about)
      ]
  

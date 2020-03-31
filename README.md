# Profiles REST API

Profiles REST API course code.

Run and connect to server...in the terminal type...

-vagrant up
-vagrant ssh

...then connect to virtual environment...Link: https://python-guide.readthedocs.io/en/latest/dev/virtualenvs/
-cd /workspace
-cd /vagrant/
-source ~/env/bin/activate

switch off environment...
-deactivate

Create django admin(super user)...
-vagrant ssh
-cd /vagrant
source ~/env/bin/activate
python manage.py createsuperuser
(add email)
(add/create password)


View app...
-python manage.py runserver 0.0.0.0:8000(view on localhost:8000)


Django REST framework Views

APIViews(https://www.django-rest-framework.org/api-guide/views/)- HTTP Methods for functions (GET, PUT, PATCH, DELETE)
  -Perfect for implementing complex logic
  -Calling other APIs
  When to use
  -Need full control over the logic
  -Processing files and redering a synchronous response
  -You are calling other APIs/services
  -Accessing local files or data

ViewSet-uses model operations for functions(List,Create, Retrieve, Update, Partial update, Destroy)
  -Take care of a lot of typical logic for You
  -Perfect for standard database operations
  -Fastest way to make a database interface
  When use...
  -A simple CRUD interface to you database
  -A quick and simple API
  -Little to no customation on the logic
  -Working with standard data structures
  

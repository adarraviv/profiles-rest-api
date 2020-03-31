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
-python manage.py runserver 0.0.0.0:8000(view on localhost:8000 or 127.0.0.1:8000)

Migrate New Profile...
-python manage.py makemigrations
-python manage.py migrate

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


  Profiles APIs

  1. Create new profiles
  2. Listing existing profiles
  3.View specific profiles
  4. Update profile of logged in user
  5. Delete profile

  API URLs

  /api/profile/
      -list all profiles when HTTP GET method is called
      -create new profile when HTTP POST method is called

  /api/profile/<profile_id>/
      -view specific profile details by using HTTP GET
      -update object using HTTP PUT/PATCH
      -remove it completely using HTTP DELETE

Plan Profile feed API
  -Update feed items- Logged in user only
  -Delete feed items- Logged in user only
  -Viewing other profile status updates - All users

  API URLs

  /api/feed/
      -list all feed items
      -GET (list feed items)
      -POST (create feed item for logged in user)

  /api/feed/<feed_item_id>/
      -manage specific feed items
      -GET(get the feed item)
      -PUT / PATCH (update feed item)
      -DELETE (delete feed item)

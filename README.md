# django-rest-angular-mongo

## DRAM for sort

This is a boilerplate and starter project for using the Django Rest Framework with Angular and MongoDB.
It uses all the latest (by the time of this writing) versions of the various requirements.
It's a simple register/login/create-post project to demonstrate the use of Angular with a REST api and
the use of MongoDB from DRF.

It contains a session engine for storing sessions in Mongo and a custom authentication application with an adaptable User model.

Originally copied from [https://github.com/brwr/thinkster-django-angular-boilerplate](https://github.com/brwr/thinkster-django-angular-boilerplate) and
[Building Web Applications with Django and AngularJS](https://thinkster.io/django-angularjs-tutorial), but extended with extra Angular directives and services
to support full CRUD operations on Posts, updated to latest version of Angular, and fixed all bugs.
 
Gulp task for javascript files concatenation and minification.

### mongo_sessions
mongo_sessions is providing the mongodb engine for storing sessions. Copied form mongoengine 0.9 and adapted

### mongo_auth
mongo_auth is providing an abstract User class and MongoDB persistence. The commands createsuperuser and changepassword are implemented.
You need to subclass the AbstractUser class, add customizations and login/logout views. 

### gulpstatic 
The gulpstatic app holds a management command for building static files with gulp first
then calls django's collectstatic ignoring the static/javascripts directory.


## Installation

*NOTE: Requires [virtualenv](http://virtualenv.readthedocs.org/en/latest/),
[virtualenvwrapper](http://virtualenvwrapper.readthedocs.org/en/latest/) and
[Node.js](http://nodejs.org/).*

* Fork this repository.
* `$ git clone https://github.com/sv1jsb/django-angular.git`
* `$ mkvirtualenv djangular`
* `$ cd django-angular`
* `$ pip install -r requirements.txt`
* `$ npm install -g bower`  (as root)
* `$ npm install -g gulp-cli`   (as root)
* `$ npm install`
* `$ bower install`
* `$ python manage.py runserver`
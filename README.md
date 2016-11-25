# cloudinary-django1.10-Example
Cloudinary Django Sample Project
================================

The code has been ported to django 1.10 following the cloudinary-django-sample 

A simple web application that allows you to uploads photos, maintain a database with references to them, list them with their metadata, and display them using various cloud-based transformations.

This sample project depends on [Cloudinary's Python library](https://github.com/cloudinary/pycloudinary). 

## Installation

Run the following commands from your shell.

Project cloning and dependent package installation: 

    git clone git://github.com/cloudinary/cloudinary-django-sample.git    
    cd cloudinary-django-sample
	  #The below lines can also goto requirement.txt
	  pip install django
    pip install cloudinary
	  # For postgres database the backend is postgres...please change database config for postgres in setting.py
	  pip install psycopg2
	
### With virtualenv

We recommend and support the usage of **virtualenv**. All you need to do is create a new virtualenv (if necessary):

    virtualenv venv

And then just activate it:

    source venv/bin/activate
	

Defining Cloudinary's credentials. The CLOUDINARY_URL value is available in the [dashboard of your Cloudinary account](https://cloudinary.com/console). 
If you don't have a Cloudinary account yet, [click here](https://cloudinary.com/users/register/free) to creare your free acount.
     
    export CLOUDINARY_URL=cloudinary://<API-KEY>:<API-SECRET>@<CLOUD-NAME>
    
Creating a local database and running a web server:
      
    python manage.py make migrations photo_album
	python manage.py migrate
    python manage.py runserver localhost:8081

You can now browse to the [following link](http://localhost:8081/) to start exploring the sample.

	http://localhost:8081/
	    
The sample app also supports the Django admin which is available [here](http://localhost:8081/admin):

	http://localhost:8081/admin


Now you can go ahead with the instructions above.


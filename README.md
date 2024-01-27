# Databases - ΕΛΙΔΕΚ DB

The UI of the webapp was inspired by [Christos Hadjichristofi](https://github.com/ChristosHadjichristofi) and [Dimitrios Kyriakidis](https://github.com/DimK19).

## Dependencies

 - [MySQL](https://www.mysql.com/) for Windows
 - [Python](https://www.python.org/downloads/), with the additional libraries:
    - [Flask](https://flask.palletsprojects.com/en/2.0.x/)
    - [Flask-MySQLdb](https://flask-mysqldb.readthedocs.io/en/latest/)
    - [faker](https://faker.readthedocs.io/en/master/) (for data generation)
    - [Flask-WTForms](https://flask-wtf.readthedocs.io/en/1.0.x/)

## What does Flask do

Flask is a micro web framework used to create web applications. It uses [Jinja](https://jinja.palletsprojects.com/en/3.0.x/) as its templating engine, to generate static template files at runtime, and [Werkzeug](https://www.palletsprojects.com/p/werkzeug/) as its WSGI toolkit, to facilitate the communication between web server and application. When writing an app locally, Flask will launch a simple "development" server on which to run it.

## How to Execute SQL Queries with Python and Flask

In order to send queries to a database from a Python program, a connection between it and the databases' server must be established first. That is accomplished by a cursor object from the `Flask-MySQLdb` library, and using the appropriate methods (`execute`, `commit`).

## Flask-WTForms

This package integrates the [WTForms](https://wtforms.readthedocs.io/en/3.0.x/) library with Flask. WTForms is used for secure input (form) validation and form rendering inside the templates. It provides security features such as [CSRF protection](https://en.wikipedia.org/wiki/Cross-site_request_forgery). Each field of a `FlaskForm` class is essentially rendered as the corresponding input tag in HTML.

## Installation Guide

First we download anaconda from here and install it https://repo.anaconda.com/archive/Anaconda3-2022.05-Windows-x86_64.exe.

From the command promt of anaconda using cd we enter the directory of the folder we downloaded from github.

Then we type and run the pip install -r requirements.txt command to install all the necessary packages for the webapp framework and for connecting the base to it.

Then ,and after we have established and confirmed connection using xampp ("run as administrator"), we run the files schema.sql, triggers.sql, views.sql and data.sql in the order listed, indicatively through MySQL wokbench, so that we build our database, with all the tables, triggers and views necessary for its proper functioning, and fill it with data.

We open the whole folder we downloaded from github with an ide, confirm that we have set anaconda3 as python interptreter; to do this we could use Visual Studio Code as ide, opening it from Anaconda Navigator.

Through ide, we put in the __init__.py file the base and user details, attention if you have a password for the root user take out the app.config[MYSQL_PASSWORD] field from comment and type in the password you have set in it.

Finally we run the run.py file and we can open the database in the browser at the address specified by the host (by default: http://localhost:3000). 

## Good Practice

Να μη γράφετε τίποτα με κεφαλαία γράμματα.

## Webapp Screenshots

Landing Page: 

![landing](https://user-images.githubusercontent.com/96352707/172066935-45b3c8c7-42ab-425d-b294-c4683e14519e.jpeg)

Create a Researcher Page:

   ![add_researcher](https://user-images.githubusercontent.com/96352707/172066933-d9c87d29-adfd-4a59-a914-697e3669d07e.png)

Edit a Researcher Module:

   ![edit_researcher](https://user-images.githubusercontent.com/96352707/172066936-59ccdd40-b6b4-4570-8eb8-417b82ebf881.png)




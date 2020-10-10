---
layout: project_page
title: Casting Agency App With Movie And Actors Data
image: flask_movie.jpg
author: Kai Zheng
date: April 2020
technology: "Flask, REST API, Docker, PostgreSQL, Auth0"
github: "https://github.com/kaizhengny/Udacity-FSND-Capstone-Project"
domain: "https://capstone-kaiz.herokuapp.com/"
---

This is a casting agency app with movies and actors data. It is hosted on Heroku with below domain:

**Domain:**  [https://capstone-kaiz.herokuapp.com/](https://capstone-kaiz.herokuapp.com/)

**Dependencies:**
    Run pip install -r requirements.txt to install the dependencies Set the variable FLASK_APP=app.py Run the command "flask run" to start

**App Test:**
    To run the test suite, run "python test_app.py"
    The "capstone-test.pgsql" could be used to set up testing databse

**Roles:**
    Casting Assistant: 
        Can view actors and movies
    Casting Director : 
        All permissions a Casting Assistant has, Add or delete an     actor from the database, Modify actors or movies
    Executive Director: 
        All permissions a Casting Director has, Add or delete a movie from the database

**Auth0:**
    This app use Auth0 for authentication and authorization services. Information for Postman testings are included in capston-kaiz.postman_collection.json file. Authentication tokens and respective permissions for each role are also listed below: 

    Casting Assistant:
        Permission: 
        get:movie, get:actor
        
        Token: ****

    Casting Director
        Permission: 
        get:movie, patch:movie, get:actor, post:actor, patch:actor, delete:actor
        
        Token: ****


    Executive Director
        Permission: 
        get:movie, post:movie, patch:movie, delete:movie, get:actor, post:actor, patch:actor, delete:actor
        
        Token: ****

**API Routes:**

    GET '/movies' -Returns a list of all movies in the database

    GET '/actors' -Returns a list of all actors in the database

    POST '/movies' -Takes a dictionary object in the request body with the following format and creates a new movie: { 'title': String, 'releasedate': String }

    POST '/actors' -Takes a dictionary object in the request body with the following format and creates a new actor: { 'name': String, 'age': Integer, 'gender': String }

    PATCH '/movies/' -Takes an id from the request URL and finds the corresponding movie to update with the provided information in the request body

    PATCH '/actors/' -Takes an id from the request URL and finds the corresponding actor to update with the provided information in the request body

    DELETE '/movies/' -Takes an id from the request URL and finds the corresponding movie to delete

    DELETE '/actors/' -Takes an id from the request URL and finds the corresponding actor to delete

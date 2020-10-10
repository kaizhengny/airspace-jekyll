---
layout: project_page
title: Coffee Shop Menu Application 
image: flask_coffee.jpg
author: Kai Zheng
date: April 2020
technology: "Flask, REST API, PostgreSQL, Auth0"
github: "https://github.com/kaizhengny/Coffe_shop"
domain: "N/A"
---

This is a full stack drink menu application for the Udacity Full-Stack Nanodegree. The application:

**Functions:**

     Display graphics representing the ratios of ingredients in each drink.
     Allow public users to view drink names and graphics.
     Allow the shop baristas to see the recipe information.
     Allow the shop managers to create new drinks and edit existing drinks.

**Dependencies:**
    Run pip install -r requirements.txt to install the dependencies Set the variable FLASK_APP=app.py Run the command "flask run" to start
    
    
**Roles:**

    Barista:
        can get:drinks-detail
    Manager:
        can perform all actions
    Customer:
        can get menu

**API Routes:**

     get:drinks-detail
     post:drinks
     patch:drinks
     delete:drinks






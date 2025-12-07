# EX01 Developing a Simple Webserver
## Date:

## AIM:
To develop a simple webserver to serve html pages and display the list of protocols in TCP/IP Protocol Suite.

## DESIGN STEPS:
### Step 1: 
Clone the problem from GitHub

### Step 2:
Create a new app in Django project

### Step 3:
Enter the code for admin.py and models.py

### Step 4:
Detect changes and create migration files that describe how to modify the database schema

### Step 5:
Execute the migration files and update the database schema to match your Django models

### Step 6:
Create a superuser with full access rights to all models and data through the admin interface.

### Step 7:
Apply the migration files of the created app to the database

### Step 8:
Execute Django admin using localhost and create details for 10 entries

### Step 9:
Start the server script and check for errors.

### Step 10:
Open a browser and navigate to http://127.0.0.1:8000 (or the assigned port).

## PROGRAM:
admin.py
python
from django.contrib import admin
from .models import Product, ProductAdmin

admin.site.register(Product, ProductAdmin)

 models.py
python
from django.db import models
from django.contrib import admin

class Product(models.Model):
    product_id = models.CharField(max_length=20, primary_key=True)
    name = models.CharField(max_length=100)
    category = models.CharField(max_length=50)
    price = models.DecimalField(max_digits=10, decimal_places=2)
    rating = models.FloatField()
    seller = models.CharField(max_length=100)
    stock = models.IntegerField()
    offer = models.CharField(max_length=50, blank=True)
    delivery_date = models.DateField()

class ProductAdmin(admin.ModelAdmin):
    list_display = (
        'product_id',
        'name',
        'category',
        'price',
        'rating',
        'seller',
        'stock',
        'offer',
        'delivery_date',
    )   

## OUTPUT:
<img width="1918" height="974" alt="Screenshot 2025-12-03 170334" src="https://github.com/user-attachments/assets/ed3ba562-adfc-4e79-b6a9-76a03007e550" />

## RESULT:
The program for implementing simple webserver is executed successfully.

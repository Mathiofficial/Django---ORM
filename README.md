# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![](./Diagram.png)

## DESIGN STEPS

### STEP 1:

Creating a table using required details in Django--ORM

### STEP 2:

Upload the python code.

### STEP 3:

Write your own steps

## PROGRAM

from django.contrib import admin
from .models import Student, StudentAdmin

# Register your models here.
admin.site.register(Student, StudentAdmin)

from django.db import models
from django.contrib import admin

# Create your models here.
class Student(models.Model):
    refNum = models.CharField(max_length=10, help_text="Your Ref. Number", primary_key = True)
    name = models.CharField(max_length=100)
    age = models.IntegerField()
    email = models.EmailField()
    dept = models.CharField(max_length=50)

class StudentAdmin(admin.ModelAdmin):
    list_display = ('refNum', 'name', 'age', 'email', 'dept')

## OUTPUT

![](./ORM.png)


## RESULT

Thus the experiment was executed successfullly.
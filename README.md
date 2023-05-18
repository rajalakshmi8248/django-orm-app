# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here

## DESIGN STEPS

### STEP 1:
Create a Django app Go to the app directory In models.py create two classes and save the models.py

### STEP 2:
Go to admins.py and put the two class in admins.py from the models.py and save the file

### STEP 3:
Start the django server then move to admin page.


## PROGRAM
MODELS.PY
```
from django.db import models
from django.contrib import admin

class Student(models.Model):
    referencenumber=models.CharField(primary_key=True,max_length=20,help_text="reference number")
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()
    dept=models.CharField(max_length=5)


class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email','dept')
```
ADMIN.PY
```
from django.contrib import admin
from .models import Student,StudentAdmin
admin.site.register(Student,StudentAdmin)
```

## OUTPUT
![ORM](https://github.com/rajalakshmi8248/django-orm-app/assets/122860827/1c02c76b-284c-4da4-a1c4-6e5c3884587d)


![OUTPUT](./ORM.png)

## RESULT
Thus the program have been executed sucessfully.

# General notes of Django

## Concept

Django is a MVT (Model, View, Template)

So the workflow is the following:

- **url.py**: Where to setup the route and, for each route, the view you want to run
- **view.py**: The view that perform task
    - **permission.py**: The rules for the users
    - **serialize.py**: To "clean" input and check output
- **template.py**
- **model.py**: The model about table

## Model

``` python
from django.db import models

class nameOfModel():
    char_field_example = models.CharField(max_length=30)

    class Meta:
        managed = False # So Django don't create or alter the table

```

For use models you need to performe two steps:
- py manager.py makemigrations
- py manager.py migrate
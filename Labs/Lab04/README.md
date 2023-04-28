# Lab 4: Django and Flask
## From Prof. Lu's GitHub Repo:
### Instructions
1. Study the GitHub [repository](https://github.com/kevinwlu/iot) Lesson 4 labs
2. Install [Django](https://en.wikipedia.org/wiki/Django_(web_framework)) and Django [REST](https://en.wikipedia.org/wiki/Representational_state_transfer) framework  
   On Windows:
   ```sh
   $ python -m pip install setuptools
   $ python -m pip install django
   $ python -m pip install djangorestframework
   $ python -m pip install django-filter
   $ python -m pip install markdown
   $ python -m pip install requests
   ```
3. Use the default database, i.e., [SQLite](https://en.wikipedia.org/wiki/SQLite)
4. Start Django project "stevens," run server, and view app  
   On Windows running Python 3.9:
   ```sh
   $ django-admin startproject stevens
   $ cd stevens
   $ py -3.9 manage.py startapp myapp
   ```
5. Start Django REST project "mycpu," run server, and view app
6. Install [Flask](https://en.wikipedia.org/wiki/Flask_(web_framework)) if no module named 'flask'
7. Run Flask server via hello_world.py and view app
### [Lesson 4: Django and Flask](lesson4/README.md)

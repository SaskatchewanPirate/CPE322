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
   For Windows:
   - Download [precompiled binaries](sqlite-tools-win32-x86-3410200.zip)
   - Extract files to C:\sqlite
   - Edit Environment Variables > Path > New > Enter "C:\sqlite"
4. Start Django project "stevens," run server, and view app  
   On Windows running Python 3.9:
   ```sh
   $ django-admin startproject stevens
   $ cd stevens
   $ py -3.9 manage.py startapp myapp
   $ sqlite3 stevens.db
   sqlite> .quit
   $ cd stevens
   $ nano settings.py
   ```
   - Change `ALLOWED_HOSTS = []` to `ALLOWED_HOSTS = ['*']`
   - Add `'myapp',` to the end of the `INSTALLED_APPS` list
   ```sh
   $ cp ~\iot\lesson4\stevens\urls.py .
   $ cd ..
   $ cd myapp
   $ cp ~\iot\lesson4\stevens\admin.py .
   $ cp ~\iot\lesson4\stevens\models.py .
   $ cp ~\iot\lesson4\stevens\views.py .
   $ mkdir templates
   $ cd templates
   $ mkdir myapp
   $ cd myapp
   $ cp ~\iot\lesson4\stevens\index.html .
   $ nano index.html
   ```
   - Set up a [Google Maps Platform](https://cloud.google.com/maps-platform) account and retrieve the [Javascript API Key](https://developers.google.com/maps/documentation/javascript/get-api-key) 
   <!--AIzaSyDOJzFwPTqL7-rkr8cStANlb4cgyBBknvg-->
   - In the line `<script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY"></script>` replace `YOUR_API_KEY` with the API key you retrieved
   ```sh
   $ cd ..
   $ cd ..
   $ mkdir static
   $ cd static
   $ cp ~\iot\lesson4\static\favicon.ico .
   $ mkdir myapp
   $ cd myapp
   $ cp ~\iot\lesson4\static\*css .
   $ cp ~\iot\lesson4\static\*js .
   $ cd ..
   $ cd ..
   $ cd ..
   $ START HERE
   ```
5. Start Django REST project "mycpu," run server, and view app
6. Install [Flask](https://en.wikipedia.org/wiki/Flask_(web_framework)) if no module named 'flask'
7. Run Flask server via hello_world.py and view app
### [Lesson 4: Django and Flask](lesson4/README.md)

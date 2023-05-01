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
   $ py -3.9 manage.py makemigrations myapp
   $ py -3.9 manage.py migrate
   $ py -3.9 manage.py createsuperuser
   Username (leave blank to use 'USER'):
   Email address: EMAIL_ADDRESS
   Password: PASSWORD
   Password (again): PASSWORD
   Superuser created successfully.
   $ py -3.9 manage.py runserver
   ```
   - Go to http://127.0.0.1:8000/admin
   - Log in using the username and password specified earlier
   - Click temperature data to add date and time in YYYY-MM-DD HH:MM:SS, temperature in Fahrenheit, Latitude 40.7451, and Longitude -74.0255
   - Save and view app at http://127.0.0.1:8000 ([Check here for help if the page didn't load Google Maps correctly](https://churchthemes.com/page-didnt-load-google-maps-correctly))
   - Return to terminal and end the process
   ```sh
   $ ipconfig
   $ py -3.9 manage.py runserver 0.0.0.0:8000
   ```
   - Make note of the IPv4 address
   - On a separate device, visit the site `IPv4_ADDRESS`:8000
5. Start Django REST project "mycpu," run server, and view app
   If still on the same Windows Terminal as earlier:
   ```sh
   $ cd ..
   $ python -m pip install urllib3
   $ django-admin startproject mycpu
   $ cd mycpu
   $ py -3.9 manage.py startapp myapp
   $ cd mycpu
   $ nano settings.py
   ```
   - Change `ALLOWED_HOSTS = []` to `ALLOWED_HOSTS = ['*']`
   - Add `'myapp',` and `'rest_framework',` to the end of the `INSTALLED_APPS` list
   ```sh
   $ cp ~\iot\lesson4\mycpu\urls.py .
   $ cd ..
   $ cd myapp
   $ cp ~\iot\lesson4\mycpu\admin.py .
   $ cp ~\iot\lesson4\mycpu\models.py .
   $ cp ~\iot\lesson4\mycpu\views.py .
   $ cp ~\iot\lesson4\mycpu\serializers.py .
   $ nano views.py
   ```
   - The default username is `'admin'`, change this to your desired username
   - The default password is `'admin'`, change this to your desired password
   ```sh
   $ mkdir templates
   $ cd templates
   $ mkdir myapp
   $ cd myapp
   $ cp ~\iot\lesson4\mycpu\index.html .
   $ nano index.html
   ```
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
   $ cp ~\iot\lesson4\mycpu\controller.py .
   $ nano controller.py
   ```
   - The default username is `'admin'`, change this to your desired username
   - The default password is `'admin'`, change this to your desired password
   - MAKE SURE THIS CORRESPONDS TO THE LOGIN CREDENTIALS IN `views.py`
   ```sh
   $ python -m pip install psutil
   $ py -3.9 manage.py makemigrations myapp
   $ py -3.9 manage.py migrate
   $ py -3.9 manage.py createsuperuser
   ```
   - In the following menu, make sure your username and password match what you had in the Python files (default: `admin`, `admin`)
   ```sh
   Username (leave blank to use 'USER'):
   Email address: EMAIL_ADDRESS
   Password: PASSWORD
   Password (again): PASSWORD
   Superuser created successfully.
   $ py -3.9 manage.py runserver
   ```
   - Go to http://127.0.0.1:8000/admin
   - Log in using the username and password specified earlier
   - Click location data to add location Stevens, Latitude 40.7451, Longitude -74.0255; click Save
   - Go to http://127.0.0.1:8000/dt and in the HTML form post 2022 to the Dt List
   - Go to http://127.0.0.1:8000/cpu and in the HTML form post 20 to the Cpu List
   - Go to http://127.0.0.1:8000/mem and in the HTML form post 20 to the Mem List
   - Open a separate terminal window, leaving the original still running
   ```sh
   $ cd ~\mycpu
   $ py -3.9 controller.py
   ```
   - View app at http://127.0.0.1:8000/home
   - Return to the first terminal and end the process
   ```sh
   $ ipconfig
   $ py -3.9 manage.py runserver 0.0.0.0:8000
   ```
   - Make note of the IPv4 address
   - On a separate device, visit the site `IPv4_ADDRESS`:8000/home/
6. Install [Flask](https://en.wikipedia.org/wiki/Flask_(web_framework)) if no module named 'flask'
   ```sh
   $ python -m pip install flask
   ```
7. Run Flask server via hello_world.py and view app
   If still on the same Windows Terminal as earlier:
   ```sh
   $ cd ~\iot\lesson4
   $ py -3.9 hello_world.py
   ```
   - Go to http://127.0.0.1:5000/
### [Lesson 4: Django and Flask](lesson4/README.md)

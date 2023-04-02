# django-todo
A simple todo app built with django

### Setup
To get this repository, run the following command inside your git enabled terminal
```bash

pip install virtualenv

virtualenv venv
--
venv\Scripts\activate

Install Django

py -m pip install Django

python -m pip install Django
```
Once you have downloaded django, go to the cloned repo directory and run the following command

```bash
$ python manage.py makemigrations
```

This will create all the migrations file (database migrations) required to run this App.

Now, to apply this migrations run the following command
```bash
$ python manage.py migrate
```

One last step and then our todo App will be live. We need to create an admin user to run this App. On the terminal, type the following command and provide username, password and email for the admin user
```bash
$ python manage.py createsuperuser
```

That was pretty simple, right? Now let's make the App live. We just need to start the server now and then we can start using our simple todo App. Start the server by following command

```bash
$ python manage.py runserver
```

Once the server is hosted, head over to http://127.0.0.1:8000/todos for the App.

Cheers and Happy Coding :)

pip freeze > requirements.txt

```

```bash
ubuntu instance
-----------------------------------------
install git, docker , python, django

sudo apt install python3-django

python3 manage.py runserver

python3 manage.py runserver 0.0.0.0:8001

create an image and run the container on 8001 port 
manage security groups to custom tcp to port 8001 
```

vi todoApp/settings.py (Allow-hosts)[*]

```bash
-----------------------------------
create a dockerfile

FROM python:3
RUN pip install django==3.2
COPY . .
RUN python manage.py migrate
CMD ["python3", "manage.py", "runserver","0.0.0.0:8001"]
-----------------------------------
docker build . -t (name)

docker run -d --name (name_container) -p 8001:8001  (name)

```

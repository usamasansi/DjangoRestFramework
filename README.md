# DjangoRestFramework
Project Description:  This repository contains a web application developed using Django REST Framework, a powerful toolkit for building Web APIs in Python. Utilizing Django's robust features along with RESTful principles, the project offers efficient data handling and interaction through RESTful endpoints.
Key Features:

Django Integration: Seamlessly integrates Django's ORM and authentication system for database interaction and user management.
Serializers: Utilizes Django REST Framework serializers to serialize and deserialize complex data types, facilitating API data representation.
Model-View-Serializer (MVS) Architecture: Adopts the MVS architecture pattern for clear separation of concerns and efficient data handling.
Customizable API Endpoints: Allows for easy creation of custom API endpoints to suit specific application requirements.
Automatic API Documentation: Generates interactive API documentation using Django REST Framework's built-in tools, enhancing API usability and developer experience.
Getting Started:

To run the project locally:

Clone this repository.
Install the necessary dependencies using pip install -r requirements.txt.
Configure the Django settings file according to your environment (database settings, secret key, etc.).
Run migrations with python manage.py migrate.
Start the development server with python manage.py runserver.
#Django #restframework #Roadmap using #command #prompt:

#pip #install #django
pip install django


E:\Learning\python\django>django-admin startproject Djangorestframework

E:\Learning\python\django>pip install djangorestframework
Collecting djangorestframework
  Downloading djangorestframework-3.14.0-py3-none-any.whl.metadata (10 kB)
Requirement already satisfied: django>=3.0 in c:\users\dell\appdata\local\programs\python\python312\lib\site-packages (from djangorestframework) (5.0.2)
Requirement already satisfied: pytz in c:\users\dell\appdata\local\programs\python\python312\lib\site-packages (from djangorestframework) (2024.1)
Requirement already satisfied: asgiref<4,>=3.7.0 in c:\users\dell\appdata\local\programs\python\python312\lib\site-packages (from django>=3.0->djangorestframework) (3.7.2)
Requirement already satisfied: sqlparse>=0.3.1 in c:\users\dell\appdata\local\programs\python\python312\lib\site-packages (from django>=3.0->djangorestframework) (0.4.4)
Requirement already satisfied: tzdata in c:\users\dell\appdata\local\programs\python\python312\lib\site-packages (from django>=3.0->djangorestframework) (2024.1)
Using cached djangorestframework-3.14.0-py3-none-any.whl (1.1 MB)
Installing collected packages: djangorestframework
Successfully installed djangorestframework-3.14.0

E:\Learning\python\django>cd djangorestframework

E:\Learning\python\django\Djangorestframework>code .

E:\Learning\python\django\Djangorestframework>python manage.py runserver
Watching for file changes with StatReloader
Performing system checks...

System check identified no issues (0 silenced).

You have 18 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
Run 'python manage.py migrate' to apply them.
February 22, 2024 - 16:32:14
Django version 5.0.2, using settings 'Djangorestframework.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CTRL-BREAK.

![Capture](https://github.com/usamasansi/DjangoRestFramework/assets/97821444/5b6bba31-0c40-40a9-a5ed-e266824470ee)
use this #command to #create #directory or #folder for mode:
python manage.py startapp base
#create #model #Item:
use this command:
python manage.py makemigrations

E:\Learning\python\django\Djangorestframework>#python #manage.py #makemigrations
Migrations for 'base':
  base\migrations\0001_initial.py
    - Create model Item


![image](https://github.com/usamasansi/DjangoRestFramework/assets/97821444/7fb7152a-da94-47d5-a5a9-5eeee69d39e8)
use this command:
python manage.py migrate

E:\Learning\python\django\Djangorestframework>python manage.py migrate
Operations to perform:
  Apply all migrations: admin, auth, base, contenttypes, sessions
Running migrations:
  Applying contenttypes.0001_initial... OK
  Applying auth.0001_initial... OK
  Applying admin.0001_initial... OK
  Applying admin.0002_logentry_remove_auto_add... OK
  Applying admin.0003_logentry_add_action_flag_choices... OK
  Applying contenttypes.0002_remove_content_type_name... OK
  Applying auth.0002_alter_permission_name_max_length... OK
  Applying auth.0003_alter_user_email_max_length... OK
  Applying auth.0004_alter_user_username_opts... OK
  Applying auth.0005_alter_user_last_login_null... OK
  Applying auth.0006_require_contenttypes_0002... OK
  Applying auth.0007_alter_validators_add_error_messages... OK
  Applying auth.0008_alter_user_username_max_length... OK
  Applying auth.0009_alter_user_last_name_max_length... OK
  Applying auth.0010_alter_group_name_max_length... OK
  Applying auth.0011_update_proxy_permissions... OK
  Applying auth.0012_alter_user_first_name_max_length... OK
  Applying base.0001_initial... OK
  Applying sessions.0001_initial... OK


E:\Learning\python\django\Djangorestframework>python manage.py shell
Python 3.12.2 (tags/v3.12.2:6abddd9, Feb  6 2024, 21:26:36) [MSC v.1937 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
(InteractiveConsole)
>>> from base.models import Item
>>> Item.objects.create(name="Item #1")
<Item: Item object (1)>
>>> Item.objects.create(name="Item #2")
<Item: Item object (2)>
>>> Item.objects.create(name="Item #3")
<Item: Item object (3)>
>>> Item.objects.create(name="Item #4")
<Item: Item object (4)>
>>> Item.objects.create(name="Item usama4")
<Item: Item object (5)>
>>> items = Item.object.all()
Traceback (most recent call last):
  File "<console>", line 1, in <module>
AttributeError: type object 'Item' has no attribute 'object'. Did you mean: 'objects'?
>>> items = Item.objects.all()
>>> print(items)

![image](https://github.com/usamasansi/DjangoRestFramework/assets/97821444/951e2e17-8d4c-4415-8a6c-3a2a97203ca4)

#face #error because i missed the "," comma at end of line #code

![image](https://github.com/usamasansi/DjangoRestFramework/assets/97821444/6194719f-a2c1-482c-b1d0-0d85804be8af)


![image](https://github.com/usamasansi/DjangoRestFramework/assets/97821444/f166ba91-6fd3-4a8a-92f8-ed3803d175bc)

to create #requirements.txt file use this commad:
pip freeze > requirements.txt
![image](https://github.com/usamasansi/DjangoRestFramework/assets/97821444/84ee28b4-a314-465e-8449-f31b418062c4)

#output of #Django #restframework :
http://127.0.0.1:8000/
![image](https://github.com/usamasansi/DjangoRestFramework/assets/97821444/599fd71c-6642-4dd7-90e7-6b16a9abfed3)

for #json type of all data:
![image](https://github.com/usamasansi/DjangoRestFramework/assets/97821444/6c041285-b75e-4aad-834a-b21ace110271)
json type of data:
http://127.0.0.1:8000/?format=json
![image](https://github.com/usamasansi/DjangoRestFramework/assets/97821444/6afbc935-e300-44ce-a64f-d110630496a6)

#post your data using this url in local host:
http://127.0.0.1:8000/add/
![image](https://github.com/usamasansi/DjangoRestFramework/assets/97821444/98c4a3d1-5366-4bc6-94bc-01d8f0a1cdd7)
#note: Add data in json form.



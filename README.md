<img src="https://i.ibb.co/nrdvBys/task-manager-cover-picture.jpg" width="100%">


<div align="center">
<h1>Task Manager</h1>
A Python-Django Task Management Web Application with REST API
<br>
<br>

<h3>Project's Short Video link: https://youtu.be/4XTaPGTVto0</h3>

</div>

<br>

## Technology Used

-   **Frontend:** HTML5, CSS3, Bootstrap5
-   **Backend:** Python=3.11.4, Django=4.2.5, djangorestframework==3.14.0
-   **Database:** PostgreSQL
-   **API:** Django-REST-Framework

<br>

## How to Run This Project Step by step


### Clone from GitHub

-   Clone the repository

```bash
git clone https://github.com/MusfiqDehan/task-manager.git
```

-   Go to the project directory

```bash
cd task-manager
```

-   Create a virtual environment

```bash
python -m venv venv
```

-   Activate the virtual environment

```bash
source venv/Scripts/activate
```

-   Install the dependencies or Lib

```bash
pip install -r requirements.txt
```

-   Run the server

```bash
python manage.py runserver
```

-   Open the browser and go to http://127.0.0.1:8000/


<br>

### Setup PostgreSQL Database

-   Install PostgreSQL

```bash
pip install psycopg2
```

-   Login to PostgreSQL

-   Create a database

-   Create a user

-   Grant privileges to the user

-   Exit from PostgreSQL


<br>

### Create environment variables & Config settings.py

-   Open the `settings.py` file from `task_manager` directory

-   Create a file named `.env` in the `task_manager` directory and add the following lines

```bash
SECRET_KEY=your_secret_key
DEBUG=False
DB_ENGINE=django.db.backends.postgresql
DB_NAME=task_manager
DB_USER=task_manager_user
DB_PASSWORD=task_manager_password
DB_HOST=localhost
DB_PORT=5432
```

See the `.env.example` file for reference.

<br>

### Import Data from database.json

-   You will find a file named `database.json` in the root directory

-   Run the following command to import data from `database.json`

```bash
python manage.py loaddata database.json
```

-   Migrate Database

```bash
python manage.py make migrations
```

```bash
python manage.py migrate
```

<br>

### Admin Panel

-   Run the server

```bash
python manage.py runserver
```

-   Open the browser and go to http://127.0.0.1:8000/admin/ for access the admin panel

-   Login with the following credentials:

    -   Username: `admin`
    -   Password: `admin`

-   If these credentials don't work, you can create a superuser by running the following command:

```bash
python manage.py createsuperuser
```

-   Enter the username, email, and password

-   Now you can access the admin panel with the credentials you have just created

<br>

## API Details

-   **Endpoint:** http://127.0.0.1:8000/task-api-view/
-   **Method:** GET, POST
-   **Description:**
    -   Returns all the tasks
-   **Endpoint:** http://127.0.0.1:8000/task-api-view/9/
-   **Method:** GET, PUT, PATCH, DELETE
-   **Description:**
    -   Returns a single task
    -   Updates a single task
    -   Partially updates a single task
    -   Deletes a single task



Getting Started
To run this project you will need to set your environment variables.

1 - Create a new file named .env inside the djcrm folder
2 - Copy all of the variables inside djcrm/.template.env and assign your own values to them
3 - Run export READ_DOT_ENV_FILE=True inside your terminal so that your environment variables file will be read.



Checklist of commands for each time we deploy - found in runserver.sh

1 - Collect static files: python3 manage.py collectstatic --no-input
2 - Most important to make sure all new migrations happen we run: python3 manage.py migrate
3 - Usually would be the 'python3 manage.py runserver', but we are using Gunicorn and Digital Ocean App Platform we point to WSGI file and run: gunicorn --worker-tmp-dir /dev/shm djcrm.wsgi


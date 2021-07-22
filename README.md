Checklist of commands for each time we deploy - found in runserver.sh

1 - Collect static files: python3 manage.py collectstatic --no-input
2 - Most important to make sure all new migrations happen we run: python3 manage.py migrate
3 - Usually would be the 'python3 manage.py runserver', but we are using Gunicorn and Digital Ocean App Platform we point to WSGI file and run: gunicorn --worker-tmp-dir /dev/shm djcrm.wsgi
## Running locally
This app uses pipenv to manage python dependencies, and Docker to manage running the DB.

Set environment variables
```cp backend.env .env```
Add your SurveyMonkey token to the `.env` file to be able to make SurveyMonkey API calls.

Run the DB
```bash
docker-compose build
docker-compose run db
```

Run the Django app:
```bash
pipenv run python manage.py makemigrations
pipenv run python manage.py migrate 
pipenv run python manage.py runserver
```
Then go to `http://127.0.0.1:8000/` to see the app in action.

Adding dependencies:
`pipenv install <dep>` 

Using the admin interface:
```bash
pipenv run python manage.py createsuperuser
```
Then go to `localhost:8000/admin`

TODO: setting up + testing Webhooks
# restdemo
restful services for demo purposes
RestDemo has one restful resource "Snippet".  Snippets can be created, updated, deleted, listed.
Unauthenticated users can only read snippets.
Any authenticated user can read any snippet. But an authenticated user can only update and delete his own snippets.
Snippets are saved in the snippets table in the restdemo schema.
RestDemo relies on a postgres database.
Path to list snippets is http://localhost:8000/snippets
Path to list snippet with id = 1 is http://localhost:8000/snippets/1
Steps to build the project:
1. Install python 3.6.3
2. Install all dependent libraries with pip install.  All libraries are listed in requirements.txt
3. Run the sql statements to configure postgres ( Create roles, users, privilegies, schema ) in setuprestdemo.sql
4. run the command:  python manage.py migrate to build the database.
5. run the command:  python manage.py runserver
6.To run the unit tests run the command python manage.py test --keepdb
7. To run the BDD test run the command python manage.py behave --keepdb


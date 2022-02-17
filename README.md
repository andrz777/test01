Flask Hello World application
=============================

This is the Flask Hello World application shamelessly copied from
http://flask.pocoo.org/docs/quickstart/.

Modified to run in Docker environment.

docker build -t flask-app:v0.1 flask-app/

docker run -d --name test-flask -p 5000:5000 flask-app:v0.1

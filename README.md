# flask-chatterbot

#### A web implementation of [ChatterBot](https://github.com/gunthercox/ChatterBot) using Flask.

## Local Setup:
 1. Ensure that Python, Flask, and ChatterBot are installed.
 2. Run *app.py*
 3. Base URL will be [http://localhost:5000/](http://localhost:5000/)

## Usage example:
*   [/get/how are you?](http://localhost:5000/get/how%20are%20you?)
  *   Browser handles whitespace for you ([/get/how%20are%20you?](http://localhost:5000/get/how%20are%20you?))
  *   Returns raw response (ex: I am good).

## How do I deploy this to a web server?
If you do not have a dedicated server, I highly recommend using [PythonAnywhere](https://www.pythonanywhere.com/) or [Heroku](https://devcenter.heroku.com/articles/getting-started-with-python#introduction) to host your application.

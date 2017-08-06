# flask-chatterbot

#### A web implementation of [ChatterBot](https://github.com/gunthercox/ChatterBot) using Flask.

## Local Setup:
 1. Ensure that Python, Flask, SQLAlchemy, and ChatterBot are installed (either manually, or run `pip install -r requirements.txt`).
 2. Run *app.py*
 3. Base URL will be [http://localhost:5000/](http://localhost:5000/)

## Usage example:
*   [/get/how are you?](http://localhost:5000/get/how%20are%20you?)
  *   Browser handles whitespace for you ([/get/how%20are%20you?](http://localhost:5000/get/how%20are%20you?))
  *   Returns raw response (ex: I am good).

## How do I deploy this to a web server?
If you do not have a dedicated server, I highly recommend using [PythonAnywhere](https://www.pythonanywhere.com/), [AWS](https://aws.amazon.com/getting-started/projects/deploy-python-application/) or [Heroku](https://devcenter.heroku.com/articles/getting-started-with-python#introduction) to host your application.

*IMPORTANT:* If you are deploying on Heroku, you will have to change the database adapter from `chatterbot.storage.SQLStorageAdapter` to `chatterbot.storage.MongoDatabaseAdapter` since SQLite3 isn't supported. To do this simply change the following line:

`english_bot = ChatBot("English Bot", storage_adapter="chatterbot.storage.SQLStorageAdapter")`

... to use the MongoDB adapter:

```
english_bot = ChatBot("English Bot", 
                     storage_adapter = "chatterbot.storage.MongoDatabaseAdapter",
                     database = mongodb_name,
                     database_uri = mongodb_uri)
```
... where `mongodb_name` is the name of the database you wish to connect to and `mongodb_uri` is the URI of a remote instance of MongoDB.
